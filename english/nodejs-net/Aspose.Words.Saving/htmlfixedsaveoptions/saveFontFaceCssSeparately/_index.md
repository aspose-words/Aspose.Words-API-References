---
title: HtmlFixedSaveOptions.saveFontFaceCssSeparately property
linktitle: saveFontFaceCssSeparately property
articleTitle: saveFontFaceCssSeparately property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.saveFontFaceCssSeparately property. Flag indicates whether @font-face CSS rules should be placed into a separate file fontFaces.css when a document is being saved with external stylesheet (that is, when [HtmlFixedSaveOptions.exportEmbeddedCss](../exportEmbeddedCss/) is ``false``)"
type: docs
weight: 180
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/saveFontFaceCssSeparately/
---

## HtmlFixedSaveOptions.saveFontFaceCssSeparately property

Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css"
when a document is being saved with external stylesheet (that is, when [HtmlFixedSaveOptions.exportEmbeddedCss](../exportEmbeddedCss/)
is ``false``).
Default value is ``false``, all CSS rules are written into single file "styles.css".



```js
get saveFontFaceCssSeparately(): boolean
```

### Remarks

Setting this property to ``true`` restores the old behavior (separate files) for compatibility with legacy code.



### Examples

Shows how to place CSS into a separate file and add a prefix to all of its CSS class names.

```js
let doc = new aw.Document(base.myDir + "Bookmarks.docx");

let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.cssClassNamesPrefix = "myprefix";
htmlFixedSaveOptions.saveFontFaceCssSeparately = true;

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html").toString();

expect(outDocContents.includes("<div class=\"myprefixdiv myprefixpage\" style=\"width:595.3pt; height:841.9pt;\">" +
  "<div class=\"myprefixdiv\" style=\"left:85.05pt; top:36pt; clip:rect(0pt,510.25pt,74.95pt,-85.05pt);\">" +
  "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294.73pt; top:0.36pt; line-height:12.29pt;\">")).toBeTruthy();

outDocContents = fs.readFileSync(base.artifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css").toString();

expect(outDocContents.includes(".myprefixdiv { position:absolute; } " +
  ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }")).toBeTruthy();
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

