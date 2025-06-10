---
title: Document.firstSection property
linktitle: firstSection property
articleTitle: firstSection property
second_title: Aspose.Words for Node.js
description: "Document.firstSection property. Gets the first section in the document."
type: docs
weight: 140
url: /nodejs-net/aspose.words/document/firstSection/
---

## Document.firstSection property

Gets the first section in the document.


```js
get firstSection(): Aspose.Words.Section
```

### Remarks

Returns ``null`` if there are no sections.



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

Shows how to iterate through the children of a composite node.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("Primary header");
builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.write("Primary footer");

let section = doc.firstSection;

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
for (let node of section)
{
  switch (node.nodeType)
  {
    case aw.NodeType.Body:
    {
      let body = node.asBody();

      console.log("Body:");
      console.log(`\t\"${body.getText().trim()}\"`);
      break;
    }
    case aw.NodeType.HeaderFooter:
    {
      let headerFooter = node.asHeaderFooter();

      console.log(`HeaderFooter type: ${headerFooter.headerFooterType}:`);
      console.log(`\t\"${headerFooter.getText().trim()}\"`);
      break;
    }
    default:
    {
      throw new Error("Unexpected node type in a section.");
    }
  }
}
```

Shows how to replace text in a document's footer.

```js
let doc = new aw.Document(base.myDir + "Footer.docx");

let headersFooters = doc.firstSection.headersFooters;
let footer = headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary);

let options = new aw.Replacing.FindReplaceOptions();
options.matchCase = false;
options.findWholeWordsOnly = false;

let currentYear = new Date().getYear();
footer.range.replace("(C) 2006 Aspose Pty Ltd.", `Copyright (C) ${currentYear} by Aspose Pty Ltd.`, options);

doc.save(base.artifactsDir + "HeaderFooter.ReplaceText.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

