---
title: Document.sections property
linktitle: sections property
articleTitle: sections property
second_title: Aspose.Words for Node.js
description: "Document.sections property. Returns a collection that represents all sections in the document."
type: docs
weight: 370
url: /nodejs-net/aspose.words/document/sections/
---

## Document.sections property

Returns a collection that represents all sections in the document.


```js
get sections(): Aspose.Words.SectionCollection
```

### Examples

Shows how to add and remove sections in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 2");

expect(doc.getText().trim()).toEqual("Section 1\u000cSection 2");

// Delete the first section from the document.
doc.sections.removeAt(0);

expect(doc.getText().trim()).toEqual("Section 2");

// Append a copy of what is now the first section to the end of the document.
let lastSectionIdx = doc.sections.count - 1;
let newSection = doc.sections.at(lastSectionIdx).clone();
doc.sections.add(newSection);

expect(doc.getText().trim()).toEqual("Section 2\u000cSection 2");
```

Shows how to specify how a new section separates itself from the previous.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("This text is in section 1.");

// Section break types determine how a new section separates itself from the previous section.
// Below are five types of section breaks.
// 1 -  Starts the next section on a new page:
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.writeln("This text is in section 2.");

expect(doc.sections.at(1).pageSetup.sectionStart).toEqual(aw.SectionStart.NewPage);

// 2 -  Starts the next section on the current page:
builder.insertBreak(aw.BreakType.SectionBreakContinuous);
builder.writeln("This text is in section 3.");

expect(doc.sections.at(2).pageSetup.sectionStart).toEqual(aw.SectionStart.Continuous);

// 3 -  Starts the next section on a new even page:
builder.insertBreak(aw.BreakType.SectionBreakEvenPage);
builder.writeln("This text is in section 4.");

expect(doc.sections.at(3).pageSetup.sectionStart).toEqual(aw.SectionStart.EvenPage);

// 4 -  Starts the next section on a new odd page:
builder.insertBreak(aw.BreakType.SectionBreakOddPage);
builder.writeln("This text is in section 5.");

expect(doc.sections.at(4).pageSetup.sectionStart).toEqual(aw.SectionStart.OddPage);

// 5 -  Starts the next section on a new column:
let columns = builder.pageSetup.textColumns;
columns.setCount(2);

builder.insertBreak(aw.BreakType.SectionBreakNewColumn);
builder.writeln("This text is in section 6.");

expect(doc.sections.at(5).pageSetup.sectionStart).toEqual(aw.SectionStart.NewColumn);

doc.save(base.artifactsDir + "PageSetup.SetSectionStart.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

