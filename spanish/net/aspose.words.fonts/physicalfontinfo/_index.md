---
title: PhysicalFontInfo Class
linktitle: PhysicalFontInfo
articleTitle: PhysicalFontInfo
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fonts.PhysicalFontInfo, que proporciona detalles esenciales sobre las fuentes físicas para mejorar el procesamiento y el diseño de documentos.
type: docs
weight: 3460
url: /es/net/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class

Especifica información sobre la fuente física disponible para el motor de fuentes Aspose.Words.

Para obtener más información, visite el[Trabajar con fuentes](https://docs.aspose.com/words/net/working-with-fonts/) Artículo de documentación.

```csharp
public class PhysicalFontInfo
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [EmbeddingLicensingRights](../../aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/) { get; } | Incorporación de derechos de licencia para la fuente. |
| [FilePath](../../aspose.words.fonts/physicalfontinfo/filepath/) { get; } | Ruta al archivo de fuente si lo hay. |
| [FontFamilyName](../../aspose.words.fonts/physicalfontinfo/fontfamilyname/) { get; } | Nombre de la familia de la fuente. |
| [FullFontName](../../aspose.words.fonts/physicalfontinfo/fullfontname/) { get; } | Nombre completo de la fuente. |
| [Version](../../aspose.words.fonts/physicalfontinfo/version/) { get; } | Cadena de versión de la fuente. |

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

* espacio de nombres [Aspose.Words.Fonts](../../aspose.words.fonts/)
* asamblea [Aspose.Words](../../)
