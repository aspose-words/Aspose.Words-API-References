---
title: ImageType enumeration
linktitle: ImageType enumeration
articleTitle: ImageType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.ImageType enumeration. Specifies the type (format) of an image in a Microsoft Word document."
type: docs
weight: 230
url: /nodejs-net/aspose.words.drawing/imagetype/
---

## ImageType enumeration

Specifies the type (format) of an image in a Microsoft Word document.


### Members

| Name | Description |
| --- | --- |
| NoImage | The is no image data. |
| Unknown | An unknown image type or image type that cannot be directly stored inside a Microsoft Word document. |
| Emf | Windows Enhanced Metafile. |
| Wmf | Windows Metafile. |
| Pict | Macintosh PICT. An existing image will be preserved in a document, but inserting new PICT images into a document is not supported. |
| Jpeg | JPEG JFIF. |
| Png | Portable Network Graphics. |
| Bmp | Windows Bitmap. |
| Eps | Encapsulated PostScript. |
| WebP | WebP. |
| Gif | GIF |

### Examples

Shows how to read WebP image.

```js
let doc = new aw.Document(base.myDir + "Document with WebP image.docx");

let shape = doc.getShape(0, true);
expect(shape.imageData.imageType).toEqual(aw.Drawing.ImageType.WebP);
```

### See Also

* module [Aspose.Words.Drawing](../)
* property [ImageData.imageType](../imagedata/imageType/)

