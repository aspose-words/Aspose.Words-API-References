---
title: PageSetup.borderSurroundsHeader property
linktitle: borderSurroundsHeader property
articleTitle: borderSurroundsHeader property
second_title: Aspose.Words for NodeJs
description: "PageSetup.borderSurroundsHeader property. Specifies whether the page border includes or excludes the header."
type: docs
weight: 60
url: /nodejs-net/aspose.words/pagesetup/borderSurroundsHeader/
---

## PageSetup.borderSurroundsHeader property

Specifies whether the page border includes or excludes the header.


```js
get borderSurroundsHeader(): boolean
```

### Remarks

Note, changing this property affects all sections in the document.


### Examples

Shows how to apply a border to the page and header/footer.

```js
let doc = new aw.Document();

let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world! This is the main body text.");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("This is the header.");
builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.write("This is the footer.");
builder.moveToDocumentEnd();

// Insert a blue double-line border.
let pageSetup = doc.sections.at(0).pageSetup;
pageSetup.borders.lineStyle = aw.LineStyle.Double;
pageSetup.borders.color = "#0000FF";

// A section's PageSetup object has "BorderSurroundsHeader" and "BorderSurroundsFooter" flags that determine
// whether a page border surrounds the main body text, also includes the header or footer, respectively.
// Set the "BorderSurroundsHeader" flag to "true" to surround the header with our border,
// and then set the "BorderSurroundsFooter" flag to leave the footer outside of the border.
pageSetup.borderSurroundsHeader = true;
pageSetup.borderSurroundsFooter = false;

doc.save(base.artifactsDir + "PageSetup.PageBorder.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

