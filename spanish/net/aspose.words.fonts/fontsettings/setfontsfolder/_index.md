---
title: FontSettings.SetFontsFolder
second_title: Referencia de API de Aspose.Words para .NET
description: FontSettings método. Establece la carpeta donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. Este es un acceso directo aSetFontsFolders para configurar solo un directorio de fuentes.
type: docs
weight: 80
url: /es/net/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings.SetFontsFolder method

Establece la carpeta donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes. Este es un acceso directo a[`SetFontsFolders`](../setfontsfolders/) para configurar solo un directorio de fuentes.

```csharp
public void SetFontsFolder(string fontFolder, bool recursive)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontFolder | String | La carpeta que contiene las fuentes TrueType. |
| recursive | Boolean | True para escanear las carpetas especificadas en busca de fuentes de forma recursiva. |

### Ejemplos

Muestra cómo configurar un directorio fuente de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nuestras fuentes de fuentes no contienen la fuente que hemos usado para el texto en este documento.
// Si usamos esta configuración de fuente mientras renderizamos este documento,
// Aspose.Words aplicará una fuente alternativa al texto que tenga una fuente que Aspose.Words no pueda localizar.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// A las fuentes de fuentes predeterminadas les faltan las dos fuentes que estamos usando en este documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Use el método "SetFontsFolder" para establecer un directorio que actuará como una nueva fuente de fuente.
// Pase "falso" como argumento "recursivo" para incluir fuentes de todos los archivos de fuentes que están en el directorio
// que estamos pasando en el primer argumento, pero sin incluir ninguna fuente en ninguna de las subcarpetas de ese directorio.
// Pasar "verdadero" como argumento "recursivo" para incluir todos los archivos de fuentes en el directorio que estamos pasando
// en el primer argumento, así como todas las fuentes en sus subdirectorios.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// La fuente "Amethysta" está en una subcarpeta del directorio de fuentes.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Restaurar las fuentes de fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ver también

* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../fontsettings/)
* asamblea [Aspose.Words](../../../)


