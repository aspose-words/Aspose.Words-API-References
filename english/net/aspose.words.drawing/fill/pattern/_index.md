---
title: Fill.Pattern
linktitle: Pattern
articleTitle: Pattern
second_title: Aspose.Words for .NET
description: Fill Pattern property. Gets a PatternType for the fill in C#.
type: docs
weight: 160
url: /net/aspose.words.drawing/fill/pattern/
---
## Fill.Pattern property

Gets a [`PatternType`](../../patterntype/) for the fill.

```csharp
public PatternType Pattern { get; }
```

## Examples

Shows how to set pattern for a shape.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// There are several ways specified fill to a pattern.
// 1 -  Apply pattern to the shape fill:
fill.Patterned(PatternType.DiagonalBrick);

// 2 -  Apply pattern with foreground and background colors to the shape fill:
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### See Also

* enum [PatternType](../../patterntype/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
