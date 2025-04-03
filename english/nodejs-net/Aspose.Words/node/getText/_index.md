---
title: Node.getText method
linktitle: getText method
articleTitle: getText method
second_title: Aspose.Words for NodeJs
description: "Node.getText method. Gets the text of this node and of all its children."
type: docs
weight: 450
url: /nodejs-net/aspose.words/node/getText/
---

## getText() {#default}

Gets the text of this node and of all its children.


```js
getText()
```

### Remarks

The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).




### Examples

Shows how to use control characters.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert paragraphs with text with DocumentBuilder.
builder.writeln("Hello world!");
builder.writeln("Hello again!");

// Converting the document to text form reveals that control characters
// represent some of the document's structural elements, such as page breaks.
expect(doc.getText()).toEqual(`Hello world!${aw.ControlChar.cr}` +
                        `Hello again!${aw.ControlChar.cr}` +
                        aw.ControlChar.pageBreak);

// When converting a document to string form,
// we can omit some of the control characters with the Trim method.
expect(doc.getText().trim()).toEqual(`Hello world!${aw.ControlChar.cr}` +
                        "Hello again!");
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
* class [Node](../)

