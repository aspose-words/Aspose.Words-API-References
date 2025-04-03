---
title: ShapeBase.wrapType property
linktitle: wrapType property
articleTitle: wrapType property
second_title: Aspose.Words for NodeJs
description: "ShapeBase.wrapType property. Defines whether the shape is inline or floating"
type: docs
weight: 580
url: /nodejs-net/aspose.words.drawing/shapebase/wrapType/
---

## ShapeBase.wrapType property

Defines whether the shape is inline or floating. For floating shapes defines the wrapping mode for text around the shape.


```js
get wrapType(): Aspose.Words.Drawing.WrapType
```

### Remarks

The default value is [WrapType.None](../../wraptype/#None).

Has effect only for top level shapes.




### Examples

Shows how to insert a floating image to the center of a page.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a floating image that will appear behind the overlapping text and align it to the page's center.
let shape = builder.insertImage(base.imageDir + "Logo.jpg");
shape.wrapType = aw.Drawing.WrapType.None;
shape.behindText = true;
shape.relativeHorizontalPosition = aw.Drawing.RelativeHorizontalPosition.Page;
shape.relativeVerticalPosition = aw.Drawing.RelativeVerticalPosition.Page;
shape.horizontalAlignment = aw.Drawing.HorizontalAlignment.Center;
shape.verticalAlignment = aw.Drawing.VerticalAlignment.Center;

doc.save(base.artifactsDir + "Image.CreateFloatingPageCenter.docx");
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

* module [Aspose.Words.Drawing](../../)
* class [ShapeBase](../)

