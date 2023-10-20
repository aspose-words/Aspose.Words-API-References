---
title: FontSubstitutionSettings.TableSubstitution
linktitle: TableSubstitution
articleTitle: TableSubstitution
second_title: Aspose.Words para .NET
description: FontSubstitutionSettings TableSubstitution propiedad. Configuraciones relacionadas con la regla de sustitución de tablas en C#.
type: docs
weight: 50
url: /es/net/aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/
---
## FontSubstitutionSettings.TableSubstitution property

Configuraciones relacionadas con la regla de sustitución de tablas.

```csharp
public TableSubstitutionRule TableSubstitution { get; }
```

## Ejemplos

Muestra cómo trabajar con tablas de sustitución de fuentes personalizadas.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crea una nueva regla de sustitución de tablas y carga la tabla de sustitución de fuentes predeterminada de Windows.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Si seleccionamos fuentes exclusivamente de nuestra carpeta, necesitaremos una tabla de sustitución personalizada.
// Ya no tendremos acceso a las fuentes de Microsoft Windows,
// como "Arial" o "Times New Roman" ya que no existen en nuestra nueva carpeta de fuentes.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// A continuación se muestran dos formas de cargar una tabla de sustitución desde un archivo en el sistema de archivos local.
// 1 - Desde una secuencia:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Directamente desde un archivo:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Como ya no tenemos acceso a "Arial", nuestra tabla de fuentes primero intentará sustituirla por "Fuente inexistente".
// No tenemos esta fuente, por lo que pasará al siguiente sustituto, "Kreon", que se encuentra en la carpeta "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Podemos expandir esta tabla mediante programación. Agregaremos una entrada que sustituya "Times New Roman" por "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Podemos agregar un sustituto secundario para una entrada de fuente existente con AddSubstitutes().
// En caso de que "Arvo" no esté disponible, nuestra tabla buscará "M+ 2m" como segunda opción sustituta.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() puede establecer una nueva lista de fuentes sustitutas para una fuente.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
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

* class [TableSubstitutionRule](../../tablesubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
