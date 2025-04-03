---
title: Inline.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for NodeJs
description: "Inline.font property. Provides access to the font formatting of this object."
type: docs
weight: 10
url: /nodejs-net/aspose.words/inline/font/
---

## Inline.font property

Provides access to the font formatting of this object.


```js
get font(): Aspose.Words.Font
```

### Examples

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
* class [Inline](../)

