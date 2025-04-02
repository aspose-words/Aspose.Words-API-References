---
title: HtmlFixedSaveOptions.cssClassNamesPrefix property
linktitle: cssClassNamesPrefix property
articleTitle: cssClassNamesPrefix property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.cssClassNamesPrefix property. Specifies prefix which is added to all class names in style.css file"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/cssClassNamesPrefix/
---

## HtmlFixedSaveOptions.cssClassNamesPrefix property

Specifies prefix which is added to all class names in style.css file.
Default value is ``"aw"``.



```js
get cssClassNamesPrefix(): string
```

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

