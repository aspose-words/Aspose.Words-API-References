---
title: ViewOptions.doNotDisplayPageBoundaries property
linktitle: doNotDisplayPageBoundaries property
articleTitle: doNotDisplayPageBoundaries property
second_title: Aspose.Words for Node.js
description: "ViewOptions.doNotDisplayPageBoundaries property. Turns off display of the space between the top of the text and the top edge of the page."
type: docs
weight: 20
url: /nodejs-net/aspose.words.settings/viewoptions/doNotDisplayPageBoundaries/
---

## ViewOptions.doNotDisplayPageBoundaries property

Turns off display of the space between the top of the text and the top edge of the page.


```js
get doNotDisplayPageBoundaries(): boolean
```

### Examples

Shows how to hide vertical whitespace and headers/footers in view options.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert content that spans across 3 pages.
builder.writeln("Paragraph 1, Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Paragraph 2, Page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Paragraph 3, Page 3.");

// Insert a header and a footer.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.writeln("This is the header.");
builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.writeln("This is the footer.");

// This document contains a small amount of content that takes up a few full pages worth of space.
// Set the "DoNotDisplayPageBoundaries" flag to "true" to get older versions of Microsoft Word to omit headers,
// footers, and much of the vertical whitespace when displaying our document.
// Set the "DoNotDisplayPageBoundaries" flag to "false" to get older versions of Microsoft Word
// to normally display our document.
doc.viewOptions.doNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.save(base.artifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### See Also

* module [Aspose.Words.Settings](../../)
* class [ViewOptions](../)

