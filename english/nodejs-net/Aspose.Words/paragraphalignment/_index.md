---
title: ParagraphAlignment enumeration
linktitle: ParagraphAlignment enumeration
articleTitle: ParagraphAlignment enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ParagraphAlignment enumeration. Specifies text alignment in a paragraph."
type: docs
weight: 1020
url: /nodejs-net/aspose.words/paragraphalignment/
---

## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.


### Members

| Name | Description |
| --- | --- |
| Left | Text is aligned to the left. |
| Center | Text is centered horizontally. |
| Right | Text is aligned to the right. |
| Justify | Text is aligned to both left and right. |
| Distributed | Text is evenly distributed. |
| ArabicMediumKashida | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ArabicHighKashida | Arabic only. Kashida length for text is extended to its widest possible length. |
| ArabicLowKashida | Arabic only. Kashida length for text is extended to a slightly longer length. |
| ThaiDistributed | Thai only. Text is justified with an optimization for Thai. |
| MathElementCenterAsGroup | The only Math element in a line, aligned as 'Centered As Group'. |

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

* module [Aspose.Words](../)

