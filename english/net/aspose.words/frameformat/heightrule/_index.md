---
title: FrameFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words for .NET
description: Discover the FrameFormat HeightRule property to easily determine frame height. Optimize your designs with precise control and improved layout efficiency.
type: docs
weight: 20
url: /net/aspose.words/frameformat/heightrule/
---
## FrameFormat.HeightRule property

Gets the rule for determining the height of the specified frame.

```csharp
public HeightRule HeightRule { get; }
```

## Examples

Shows how to get information about formatting properties of paragraphs that are frames.

```csharp
Document doc = new Document(MyDir + "Paragraph frame.docx");

Paragraph paragraphFrame = doc.FirstSection.Body.Paragraphs.OfType<Paragraph>().First(p => p.FrameFormat.IsFrame);

Assert.That(paragraphFrame.FrameFormat.Width, Is.EqualTo(233.3d));
Assert.That(paragraphFrame.FrameFormat.Height, Is.EqualTo(138.8d));
Assert.That(paragraphFrame.FrameFormat.HeightRule, Is.EqualTo(HeightRule.AtLeast));
Assert.That(paragraphFrame.FrameFormat.HorizontalAlignment, Is.EqualTo(HorizontalAlignment.Default));
Assert.That(paragraphFrame.FrameFormat.VerticalAlignment, Is.EqualTo(VerticalAlignment.Default));
Assert.That(paragraphFrame.FrameFormat.HorizontalPosition, Is.EqualTo(34.05d));
Assert.That(paragraphFrame.FrameFormat.RelativeHorizontalPosition, Is.EqualTo(RelativeHorizontalPosition.Page));
Assert.That(paragraphFrame.FrameFormat.HorizontalDistanceFromText, Is.EqualTo(9.0d));
Assert.That(paragraphFrame.FrameFormat.VerticalPosition, Is.EqualTo(20.5d));
Assert.That(paragraphFrame.FrameFormat.RelativeVerticalPosition, Is.EqualTo(RelativeVerticalPosition.Paragraph));
Assert.That(paragraphFrame.FrameFormat.VerticalDistanceFromText, Is.EqualTo(0.0d));
```

### See Also

* enum [HeightRule](../../heightrule/)
* class [FrameFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
