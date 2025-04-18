---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words for .NET
description: Discover how the FitShapeToText property in Microsoft Word automatically adjusts shapes to perfectly fit your text, enhancing document presentation.
type: docs
weight: 10
url: /net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Determines whether Microsoft Word will grow the shape to fit text.

```csharp
public bool FitShapeToText { get; set; }
```

## Remarks

The default value is `false`.

## Examples

Shows how to get a text box to resize itself to fit its contents tightly.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Apply these values to both these members to get the parent shape to fit
// tightly around the text contents, ignoring the dimensions we have set.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### See Also

* class [TextBox](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
