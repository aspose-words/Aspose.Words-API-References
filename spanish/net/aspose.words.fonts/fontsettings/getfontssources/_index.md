---
title: FontSettings.GetFontsSources
linktitle: GetFontsSources
articleTitle: GetFontsSources
second_title: Aspose.Words para .NET
description: Descubre el método GetFontsSources de FontSettings para acceder fácilmente a la matriz de fuentes TrueType en Aspose.Words. ¡Optimiza tu gestión de fuentes hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method

Obtiene una copia de la matriz que contiene la lista de fuentes donde Aspose.Words busca fuentes TrueType.

```csharp
public FontSourceBase[] GetFontsSources()
```

### Valor_devuelto

Una copia de las fuentes actuales.

## Observaciones

El valor devuelto es una copia de los datos que utiliza Aspose.Words. Si modifica entries en la matriz devuelta, no afectará la representación del documento. Para especificar la nueva fuente sources , utilice[`SetFontsSources`](../setfontssources/) método.

## Ejemplos

Muestra cómo agregar una fuente de fuente a nuestras fuentes de fuentes existentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

//A la fuente de fuente predeterminada le faltan dos de las fuentes que estamos usando en nuestro documento.
// Cuando guardemos este documento, Aspose.Words aplicará fuentes de respaldo a todo el texto formateado con fuentes inaccesibles.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Crea una fuente de fuente desde una carpeta que contiene fuentes.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Aplicar una nueva matriz de fuentes de fuentes que contenga las fuentes de fuentes originales, así como nuestras fuentes personalizadas.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Verifique que Aspose.Words tenga acceso a todas las fuentes requeridas antes de convertir el documento a PDF.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Restaurar las fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ver también

* class [FontSourceBase](../../fontsourcebase/)
* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
