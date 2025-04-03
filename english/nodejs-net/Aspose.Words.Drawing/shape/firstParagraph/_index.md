---
title: Shape.firstParagraph property
linktitle: firstParagraph property
articleTitle: firstParagraph property
second_title: Aspose.Words for NodeJs
description: "Shape.firstParagraph property. Gets the first paragraph in the shape."
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing/shape/firstParagraph/
---

## Shape.firstParagraph property

Gets the first paragraph in the shape.


```js
get firstParagraph(): Aspose.Words.Paragraph
```

### Examples

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

* module [Aspose.Words.Drawing](../../)
* class [Shape](../)

