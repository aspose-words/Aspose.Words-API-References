---
title: PageSetup.sectionStart property
linktitle: sectionStart property
articleTitle: sectionStart property
second_title: Aspose.Words for Node.js
description: "PageSetup.sectionStart property. Returns or sets the type of section break for the specified object."
type: docs
weight: 390
url: /nodejs-net/aspose.words/pagesetup/sectionStart/
---

## PageSetup.sectionStart property

Returns or sets the type of section break for the specified object.


```js
get sectionStart(): Aspose.Words.SectionStart
```

### Examples

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

Shows how to construct an Aspose.words document by hand.

```js
let doc = new aw.Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.removeAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
let section = new aw.Section(doc);
doc.appendChild(section);

// Set some page setup properties for the section.
section.pageSetup.sectionStart = aw.SectionStart.NewPage;
section.pageSetup.paperSize = aw.PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
let body = new aw.Body(doc);
section.appendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
let para = new aw.Paragraph(doc);

para.paragraphFormat.styleName = "Heading 1";
para.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

body.appendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
let run = new aw.Run(doc);
run.text = "Hello World!";
run.font.color = "#FF0000";
para.appendChild(run);

expect(doc.getText().trim()).toEqual("Hello World!");

doc.save(base.artifactsDir + "Section.CreateManually.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

