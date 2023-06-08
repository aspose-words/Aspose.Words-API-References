---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words for .NET
description: TextBox NoTextRotation property. Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated in C#.
type: docs
weight: 80
url: /net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Gets or sets a boolean value indicating either text of the TextBox should not rotate when the shape is rotated.

```csharp
public bool NoTextRotation { get; set; }
```

## Remarks

The default value is `false`

## Examples

Shows how to disable text rotation when the shape is rotate.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### See Also

* class [TextBox](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
