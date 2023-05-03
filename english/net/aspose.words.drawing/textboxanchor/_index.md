---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Drawing.TextBoxAnchor enum. Specifies values used for shape text vertical alignment in C#.
type: docs
weight: 1300
url: /net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Specifies values used for shape text vertical alignment.

```csharp
public enum TextBoxAnchor
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Top | `0` | Text is aligned to the top of the textbox. |
| Middle | `1` | Text is aligned to the middle of the textbox. |
| Bottom | `2` | Text is aligned to the bottom of the textbox. |
| TopCentered | `3` | Text is aligned to the top centered of the textbox. |
| MiddleCentered | `4` | Text is aligned to the middle centered of the textbox. |
| BottomCentered | `5` | Text is aligned to the bottom centered of the textbox. |
| TopBaseline | `6` | Text is aligned to the top baseline of the textbox. |
| BottomBaseline | `7` | Text is aligned to the bottom baseline of the textbox. |
| TopCenteredBaseline | `8` | Text is aligned to the top centered baseline of the textbox. |
| BottomCenteredBaseline | `9` | Text is aligned to the bottom centered baseline of the textbox. |

## Examples

Shows how to vertically align the text contents of a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
// align the text in this text box with the top side of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
// align the text in this text box to the center of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
// align the text in this text box to the bottom of the shape.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
