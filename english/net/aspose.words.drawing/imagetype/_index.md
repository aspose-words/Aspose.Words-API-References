---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.ImageType enum. Specifies the type format of an image in a Microsoft Word document in C#.
type: docs
weight: 1270
url: /net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Specifies the type (format) of an image in a Microsoft Word document.

```csharp
public enum ImageType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| NoImage | `0` | The is no image data. |
| Unknown | `1` | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| Emf | `2` | Windows Enhanced Metafile. |
| Wmf | `3` | Windows Metafile. |
| Pict | `4` | Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Portable Network Graphics. |
| Bmp | `7` | Windows Bitmap. |
| Eps | `8` | Encapsulated PostScript. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## Examples

Shows how to read WebP image.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Shows how to add an image to a shape and check its type.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### See Also

* property [ImageType](../imagedata/imagetype/)
* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
