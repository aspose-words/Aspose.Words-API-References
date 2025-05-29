---
title: FontSourceBase.GetAvailableFonts
linktitle: GetAvailableFonts
articleTitle: GetAvailableFonts
second_title: Aspose.Words para .NET
description: Descubre las fuentes disponibles con el método GetAvailableFonts de FontSourceBase. ¡Mejora tus proyectos con una selección diversa de tipografías de alta calidad!
type: docs
weight: 40
url: /es/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

Devuelve la lista de fuentes disponibles a través de esta fuente.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

## Ejemplos

Muestra cómo enumerar las fuentes disponibles.

```csharp
// Configure Aspose.Words para obtener fuentes de una carpeta personalizada y luego imprimir todas las fuentes disponibles.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### Ver también

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
