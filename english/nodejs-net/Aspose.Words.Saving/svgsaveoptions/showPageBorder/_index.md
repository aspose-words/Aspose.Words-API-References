---
title: SvgSaveOptions.showPageBorder property
linktitle: showPageBorder property
articleTitle: showPageBorder property
second_title: Aspose.Words for NodeJs
description: "SvgSaveOptions.showPageBorder property. Controls whether a border is added to the outline of the page"
type: docs
weight: 110
url: /nodejs-net/Aspose.Words.Saving/svgsaveoptions/showPageBorder/
---

## SvgSaveOptions.showPageBorder property

Controls whether a border is added to the outline of the page.
Default is ``true``.



```js
get showPageBorder(): boolean
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

