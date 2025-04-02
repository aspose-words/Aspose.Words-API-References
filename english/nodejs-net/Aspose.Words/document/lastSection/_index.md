---
title: Document.lastSection property
linktitle: lastSection property
articleTitle: lastSection property
second_title: Aspose.Words for NodeJs
description: "Document.lastSection property. Gets the last section in the document."
type: docs
weight: 250
url: /nodejs-net/Aspose.Words/document/lastSection/
---

## Document.lastSection property

Gets the last section in the document.


```js
get lastSection(): Aspose.Words.Section
```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```js
let doc = new aw.Document();

// A blank document contains one section by default,
// which contains child nodes that we can edit.
expect(doc.sections.count).toEqual(1);

// Use a document builder to add text to the first section.
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Create a second section by inserting a section break.
builder.insertBreak(aw.BreakType.SectionBreakNewPage);

expect(doc.sections.count).toEqual(2);

// Each section has its own page setup settings.
// We can split the text in the second section into two columns.
// This will not affect the text in the first section.
doc.lastSection.pageSetup.textColumns.setCount(2);
builder.writeln("Column 1.");
builder.insertBreak(aw.BreakType.ColumnBreak);
builder.writeln("Column 2.");

expect(doc.firstSection.pageSetup.textColumns.count).toEqual(1);
expect(doc.lastSection.pageSetup.textColumns.count).toEqual(2);

doc.save(base.artifactsDir + "Section.create.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

