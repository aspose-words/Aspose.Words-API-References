---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words para .NET
description: Descubre cómo personalizar los nombres de fuentes con el método SetSubstitutes de TableSubstitutionRule. ¡Mejora tu diseño con soluciones tipográficas personalizadas!
type: docs
weight: 80
url: /es/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Anular nombres de fuentes sustitutas para el nombre de fuente original dado.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| originalFontName | String | Nombre de la fuente original. |
| substituteFontNames | String[] | Lista de nombres de fuentes alternativos. |

## Ejemplos

Muestra cómo establecer reglas de sustitución de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Las fuentes de fuentes predeterminadas contienen la primera fuente que utiliza el documento.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

//La segunda fuente, "Amethysta", no está disponible.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

//Podemos configurar una tabla de sustitución de fuentes que determine
// qué fuentes utilizará Aspose.Words como sustitutas de las fuentes no disponibles.
// Establezca dos fuentes de sustitución para "Amethysta": "Arvo" y "Courier New".
// Si el primer sustituto no está disponible, Aspose.Words intenta utilizar el segundo sustituto, y así sucesivamente.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" no está disponible y la regla de sustitución establece que la primera fuente a utilizar como sustituta es "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" tampoco está disponible, pero "Courier New" sí.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

//El documento de salida mostrará el texto que utiliza la fuente "Amethysta" formateada con "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Muestra cómo trabajar con tablas de sustitución de fuentes personalizadas.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Cree una nueva regla de sustitución de tabla y cargue la tabla de sustitución de fuentes predeterminada de Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Si seleccionamos fuentes exclusivamente de nuestra carpeta, necesitaremos una tabla de sustitución personalizada.
//Ya no tendremos acceso a las fuentes de Microsoft Windows,
// como "Arial" o "Times New Roman" ya que no existen en nuestra nueva carpeta de fuentes.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

A continuación se muestran dos formas de cargar una tabla de sustitución desde un archivo en el sistema de archivos local.
// 1 - Desde un stream:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Directamente desde un archivo:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Como ya no tenemos acceso a "Arial", nuestra tabla de fuentes primero intentará sustituirla por "Fuente inexistente".
//No tenemos esta fuente, por lo que pasaremos al siguiente sustituto, "Kreon", que se encuentra en la carpeta "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

Podemos expandir esta tabla programáticamente. Agregaremos una entrada que sustituya "Times New Roman" por "Arvo".
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Podemos agregar un sustituto secundario para una entrada de fuente existente con AddSubstitutes().
// En caso de que "Arvo" no esté disponible, nuestra tabla buscará "M+ 2m" como segunda opción sustitutiva.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() puede establecer una nueva lista de fuentes sustitutas para una fuente.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Escribir texto en fuentes a las que no tenemos acceso invocará nuestras reglas de sustitución.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Ver también

* class [TableSubstitutionRule](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
