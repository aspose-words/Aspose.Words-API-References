---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words para .NET
description: FontSettings SetFontsFolders método. Establece las carpetas donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes en C#.
type: docs
weight: 90
url: /es/net/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method

Establece las carpetas donde Aspose.Words busca fuentes TrueType al renderizar documentos o incrustar fuentes.

```csharp
public void SetFontsFolders(string[] fontsFolders, bool recursive)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontsFolders | String[] | Una serie de carpetas que contienen fuentes TrueType. |
| recursive | Boolean | True para escanear las carpetas especificadas en busca de fuentes de forma recursiva. |

## Observaciones

De forma predeterminada, Aspose.Words busca fuentes instaladas en el sistema.

Establecer esta propiedad restablece el caché de todas las fuentes cargadas anteriormente.

## Ejemplos

Muestra cómo configurar múltiples directorios de fuentes de fuentes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Nuestras fuentes de fuentes no contienen la fuente que hemos utilizado para el texto de este documento.
// Si utilizamos esta configuración de fuente al renderizar este documento,
// Aspose.Words aplicará una fuente alternativa al texto que tenga una fuente que Aspose.Words no pueda localizar.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// A las fuentes de fuentes predeterminadas les faltan las dos fuentes que estamos usando en este documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Utilice el método "SetFontsFolders" para crear una fuente de fuente a partir de cada directorio de fuentes que pasemos como primer argumento.
// Pasa "falso" como argumento "recursivo" para incluir fuentes de todos los archivos de fuentes que están en los directorios
// que estamos pasando el primer argumento, pero no incluimos ninguna fuente de ninguna de las subcarpetas de los directorios.
// Pasa "true" como argumento "recursivo" para incluir todos los archivos de fuentes en los directorios que estamos pasando
// en el primer argumento, así como todas las fuentes en sus subdirectorios.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// La carpeta "Junction" en sí no contiene archivos de fuentes, pero tiene subcarpetas que sí los contienen.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Restaurar las fuentes de fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ver también

* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
