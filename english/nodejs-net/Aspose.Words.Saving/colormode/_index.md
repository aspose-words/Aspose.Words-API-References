---
title: ColorMode enumeration
linktitle: ColorMode enumeration
articleTitle: ColorMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.ColorMode enumeration. Specifies how colors are rendered."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Saving/colormode/
---

## ColorMode enumeration

Specifies how colors are rendered.


### Members

| Name | Description |
| --- | --- |
| Normal | Rendering with unmodified colors. |
| Grayscale | Rendering with colors in a range of gray shades from white to black. |

### Examples

Shows how to change image color with saving options property.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
// Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
// The size of the output document may be larger with this setting.
// Set the "ColorMode" property to "Normal" to render all images in color.
let pdfSaveOptions = new aw.Saving.PdfSaveOptions();
pdfSaveOptions.colorMode = colorMode;

doc.save(base.artifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

