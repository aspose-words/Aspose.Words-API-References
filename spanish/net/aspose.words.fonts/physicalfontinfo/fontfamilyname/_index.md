---
title: PhysicalFontInfo.FontFamilyName
linktitle: FontFamilyName
articleTitle: FontFamilyName
second_title: Aspose.Words para .NET
description: PhysicalFontInfo FontFamilyName propiedad. Apellido de la fuente en C#.
type: docs
weight: 20
url: /es/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

Apellido de la fuente.

```csharp
public string FontFamilyName { get; }
```

## Ejemplos

Muestra cómo enumerar las fuentes disponibles.

```csharp
// Configure Aspose.Words para obtener fuentes de una carpeta personalizada y luego imprima todas las fuentes disponibles.
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

* class [PhysicalFontInfo](../)
* espacio de nombres [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../../)
