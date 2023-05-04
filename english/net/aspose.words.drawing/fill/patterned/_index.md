---
title: Fill.Patterned
linktitle: Patterned
articleTitle: Patterned
second_title: Aspose.Words for .NET
description: Fill Patterned method. Sets the specified fill to a pattern in C#.
type: docs
weight: 210
url: /net/aspose.words.drawing/fill/patterned/
---
## Patterned(*[PatternType](../../patterntype/)*) {#patterned}

Sets the specified fill to a pattern.

```csharp
public void Patterned(PatternType patternType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |

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
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)

---

## Patterned(*[PatternType](../../patterntype/), Color, Color*) {#patterned_1}

Sets the specified fill to a pattern.

```csharp
public void Patterned(PatternType patternType, Color foreColor, Color backColor)
```

| Parameter | Type | Description |
| --- | --- | --- |
| patternType | PatternType | [`PatternType`](../../patterntype/) |
| foreColor | Color | The color of the foreground fill. |
| backColor | Color | The color of the background fill. |

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
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)
