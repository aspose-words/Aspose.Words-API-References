---
title: HtmlFixedSaveOptions.pageMargins property
linktitle: pageMargins property
articleTitle: pageMargins property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.pageMargins property. Specifies the margins around pages in an HTML document"
type: docs
weight: 130
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/pageMargins/
---

## HtmlFixedSaveOptions.pageMargins property

Specifies the margins around pages in an HTML document.
The margins value is measured in points and should be equal to or greater than 0.
Default value is 10 points.


```js
get pageMargins(): number
```

### Remarks

Depends on the value of [HtmlFixedSaveOptions.pageHorizontalAlignment](../pageHorizontalAlignment/) property:


* Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.Left](../../htmlfixedpagehorizontalalignment/#Left).
  
  
* Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.Right](../../htmlfixedpagehorizontalalignment/#Right).
  
  
* Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.Center](../../htmlfixedpagehorizontalalignment/#Center).
  
  



### Examples

Shows how to adjust page margins when saving a document to HTML.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let saveOptions = new aw.Saving.HtmlFixedSaveOptions();
saveOptions.pageMargins = 15;

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.pageMargins.html", saveOptions);

let outDocContents = fs.readFileSync(base.artifactsDir + "HtmlFixedSaveOptions.pageMargins/styles.css").toString();

expect(outDocContents.includes(".awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")).toBeTruthy();
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

