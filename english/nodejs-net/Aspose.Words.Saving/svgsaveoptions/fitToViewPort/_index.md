---
title: SvgSaveOptions.fitToViewPort property
linktitle: fitToViewPort property
articleTitle: fitToViewPort property
second_title: Aspose.Words for NodeJs
description: "SvgSaveOptions.fitToViewPort property. Specifies if the output SVG should fill the available viewport area (browser window or container)"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/svgsaveoptions/fitToViewPort/
---

## SvgSaveOptions.fitToViewPort property

Specifies if the output SVG should fill the available viewport area (browser window or container).
When set to ``True`` width and height of output SVG are set to 100%.

The default value is ``False``.




```js
get fitToViewPort(): boolean
```

### Examples

Shows how to mimic the properties of images when converting a .docx document to .svg.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

// Configure the SvgSaveOptions object to save with no page borders or selectable text.
let options = new aw.Saving.SvgSaveOptions();
options.fitToViewPort = true;
options.showPageBorder = false;
options.textOutputMode = aw.Saving.SvgTextOutputMode.UsePlacedGlyphs;

doc.save(base.artifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SvgSaveOptions](../)

