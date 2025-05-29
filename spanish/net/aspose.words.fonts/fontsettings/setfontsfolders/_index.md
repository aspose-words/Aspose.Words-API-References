---
title: FontSettings.SetFontsFolders
linktitle: SetFontsFolders
articleTitle: SetFontsFolders
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar el método SetFontsFolders en Aspose.Words para personalizar las ubicaciones de las fuentes TrueType para una representación e incrustación óptimas de documentos.
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
| fontsFolders | String[] | Una matriz de carpetas que contienen fuentes TrueType. |
| recursive | Boolean | Verdadero para escanear las carpetas especificadas en busca de fuentes de forma recursiva. |

## Observaciones

De forma predeterminada, Aspose.Words busca fuentes instaladas en el sistema.

Al establecer esta propiedad se restablece el caché de todas las fuentes cargadas previamente.

## Ejemplos

Muestra cómo configurar múltiples directorios de fuentes de origen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

//Nuestras fuentes no contienen la fuente que hemos utilizado para el texto de este documento.
// Si utilizamos estas configuraciones de fuente al renderizar este documento,
// Aspose.Words aplicará una fuente alternativa al texto que tenga una fuente que Aspose.Words no pueda localizar.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Las fuentes predeterminadas carecen de las dos fuentes que estamos usando en este documento.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Utilice el método "SetFontsFolders" para crear una fuente de fuente desde cada directorio de fuentes que pasemos como primer argumento.
// Pase "falso" como argumento "recursivo" para incluir fuentes de todos los archivos de fuentes que están en los directorios
// que estamos pasando en el primer argumento, pero no incluimos ninguna fuente de ninguna de las subcarpetas de los directorios.
// Pase "verdadero" como argumento "recursivo" para incluir todos los archivos de fuentes en los directorios que estamos pasando
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

// Restaurar las fuentes originales.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ver también

* class [FontSettings](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
