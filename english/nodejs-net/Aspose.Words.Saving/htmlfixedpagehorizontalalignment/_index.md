---
title: HtmlFixedPageHorizontalAlignment enumeration
linktitle: HtmlFixedPageHorizontalAlignment enumeration
articleTitle: HtmlFixedPageHorizontalAlignment enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.HtmlFixedPageHorizontalAlignment enumeration. Specifies the horizontal alignment for pages in output HTML document."
type: docs
weight: 230
url: /nodejs-net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---

## HtmlFixedPageHorizontalAlignment enumeration

Specifies the horizontal alignment for pages in output HTML document.


### Members

| Name | Description |
| --- | --- |
| Left | Align pages to the left. |
| Center | Center pages. This is the default value. |
| Right | Align pages to the right. |

### Examples

Shows how to set the horizontal alignment of pages when saving a document to HTML.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.pageHorizontalAlignment = pageHorizontalAlignment;

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.horizontalAlignment.html", htmlFixedSaveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlFixedSaveOptions.horizontalAlignment/styles.css").toString();

switch (pageHorizontalAlignment)
{
  case aw.Saving.HtmlFixedPageHorizontalAlignment.Center:
    expect(outDocContents.includes(".awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }")).toBeTruthy();
    break;
  case aw.Saving.HtmlFixedPageHorizontalAlignment.Left:
    expect(outDocContents.includes(".awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }")).toBeTruthy();
    break;
  case aw.Saving.HtmlFixedPageHorizontalAlignment.Right:
    expect(outDocContents.includes(".awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }")).toBeTruthy();
    break;
}
```

### See Also

* module [Aspose.Words.Saving](../)

