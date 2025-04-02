---
title: SvgTextOutputMode enumeration
linktitle: SvgTextOutputMode enumeration
articleTitle: SvgTextOutputMode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.SvgTextOutputMode enumeration. Allows to specify how text inside a document should be rendered when saving in SVG format."
type: docs
weight: 810
url: /nodejs-net/Aspose.Words.Saving/svgtextoutputmode/
---

## SvgTextOutputMode enumeration

Allows to specify how text inside a document should be rendered
when saving in SVG format.


### Members

| Name | Description |
| --- | --- |
| UseSvgFonts | SVG fonts are used to render text. Note, not all browsers support SVG fonts. |
| UseTargetMachineFonts | Fonts installed on the target machine are used to render text.  Note, if some of fonts used in the document are not available on the target machine, document can look differently. |
| UsePlacedGlyphs | Text is rendered using curves. Note, text selection will not work if you use this option. |

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

* module [Aspose.Words.Saving](../)

