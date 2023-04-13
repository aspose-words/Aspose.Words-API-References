---
title: TextBox Class
linktitle: TextBox
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.TextBox class. Defines attributes that specify how a text is displayed inside a shape in C#.
type: docs
weight: 1210
url: /net/aspose.words.drawing/textbox/
---
## TextBox class

Defines attributes that specify how a text is displayed inside a shape.

To learn more, visit the [Working with Shapes](https://docs.aspose.com/words/net/working-with-shapes/) documentation article.

```csharp
public class TextBox
```

## Properties

| Name | Description |
| --- | --- |
| [FitShapeToText](../../aspose.words.drawing/textbox/fitshapetotext/) { get; set; } | Determines whether Microsoft Word will grow the shape to fit text. |
| [InternalMarginBottom](../../aspose.words.drawing/textbox/internalmarginbottom/) { get; set; } | Specifies the inner bottom margin in points for a shape. |
| [InternalMarginLeft](../../aspose.words.drawing/textbox/internalmarginleft/) { get; set; } | Specifies the inner left margin in points for a shape. |
| [InternalMarginRight](../../aspose.words.drawing/textbox/internalmarginright/) { get; set; } | Specifies the inner right margin in points for a shape. |
| [InternalMarginTop](../../aspose.words.drawing/textbox/internalmargintop/) { get; set; } | Specifies the inner top margin in points for a shape. |
| [LayoutFlow](../../aspose.words.drawing/textbox/layoutflow/) { get; set; } | Determines the flow of the text layout in a shape. |
| [Next](../../aspose.words.drawing/textbox/next/) { get; set; } | Returns or sets a `TextBox` that represents the next `TextBox` in a sequence of shapes. |
| [NoTextRotation](../../aspose.words.drawing/textbox/notextrotation/) { get; set; } | Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated. |
| [Parent](../../aspose.words.drawing/textbox/parent/) { get; } | Gets a parent shape for the `TextBox`. |
| [Previous](../../aspose.words.drawing/textbox/previous/) { get; } | Returns a `TextBox` that represents the previous `TextBox` in a sequence of shapes. |
| [TextBoxWrapMode](../../aspose.words.drawing/textbox/textboxwrapmode/) { get; set; } | Determines how text wraps inside a shape. |
| [VerticalAnchor](../../aspose.words.drawing/textbox/verticalanchor/) { get; set; } | Specifies the vertical alignment of the text within a shape. |

## Methods

| Name | Description |
| --- | --- |
| [BreakForwardLink](../../aspose.words.drawing/textbox/breakforwardlink/)() | Breaks the link to the next `TextBox`. |
| [IsValidLinkTarget](../../aspose.words.drawing/textbox/isvalidlinktarget/)(*TextBox*) | Determines whether this `TextBox` can be linked to the target `TextBox`. |

## Remarks

Use the [`TextBox`](../shape/textbox/) property to access text properties of a shape. You do not create instances of the `TextBox` class directly.

## Examples

Shows how to set internal margins for a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert another textbox with specific margins.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

Shows how to set the orientation of text inside a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Move the document builder to inside the TextBox and add text.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Set the "LayoutFlow" property to set an orientation for the text contents of this text box.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

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

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
