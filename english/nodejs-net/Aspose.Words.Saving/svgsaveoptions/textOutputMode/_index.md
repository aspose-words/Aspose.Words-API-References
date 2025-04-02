---
title: SvgSaveOptions.textOutputMode property
linktitle: textOutputMode property
articleTitle: textOutputMode property
second_title: Aspose.Words for NodeJs
description: "SvgSaveOptions.textOutputMode property. Gets or sets a value determining how text should be rendered in SVG."
type: docs
weight: 120
url: /nodejs-net/Aspose.Words.Saving/svgsaveoptions/textOutputMode/
---

## SvgSaveOptions.textOutputMode property

Gets or sets a value determining how text should be rendered in SVG.


```js
get textOutputMode(): Aspose.Words.Saving.SvgTextOutputMode
```

### Remarks

Use this property to get or set the mode of how text inside a document should be rendered
when saving in SVG format.

The default value is [SvgTextOutputMode.UseTargetMachineFonts](../../svgtextoutputmode/#UseTargetMachineFonts).




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

