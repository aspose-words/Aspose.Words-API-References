---
title: Story.firstParagraph property
linktitle: firstParagraph property
articleTitle: firstParagraph property
second_title: Aspose.Words for NodeJs
description: "Story.firstParagraph property. Gets the first paragraph in the story."
type: docs
weight: 10
url: /nodejs-net/aspose.words/story/firstParagraph/
---

## Story.firstParagraph property

Gets the first paragraph in the story.


```js
get firstParagraph(): Aspose.Words.Paragraph
```

### Examples

Shows how to format a run of text using its font property.

```js
let doc = new aw.Document();
let run = new aw.Run(doc, "Hello world!");

let font = run.font;
font.name = "Courier New";
font.size = 36;
font.highlightColor = "#FFFF00";

doc.firstSection.body.firstParagraph.appendChild(run);
doc.save(base.artifactsDir + "Font.CreateFormattedRun.docx");
```

Shows how to create and format a text box.

```js
let doc = new aw.Document();

// Create a floating text box.
let textBox = new aw.Drawing.Shape(doc, aw.Drawing.ShapeType.TextBox);
textBox.wrapType = aw.Drawing.WrapType.None;
textBox.height = 50;
textBox.width = 200;

// Set the horizontal, and vertical alignment of the text inside the shape.
textBox.horizontalAlignment = aw.Drawing.HorizontalAlignment.Center;
textBox.verticalAlignment = aw.Drawing.VerticalAlignment.Top;

// Add a paragraph to the text box and add a run of text that the text box will display.
textBox.appendChild(new aw.Paragraph(doc));
let para = textBox.firstParagraph;
para.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
let run = new aw.Run(doc);
run.text = "Hello world!";
para.appendChild(run);

doc.firstSection.body.firstParagraph.appendChild(textBox);

doc.save(base.artifactsDir + "Shape.CreateTextBox.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Story](../)

