---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.FrameFormat class for advanced frame formatting in paragraphs. Enhance your document design with seamless integration and flexibility.
type: docs
weight: 3520
url: /net/aspose.words/frameformat/
---
## FrameFormat class

Represents frame related formatting for a paragraph.

```csharp
public class FrameFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Gets the height of the specified frame. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Gets the rule for determining the height of the specified frame. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Gets horizontal alignment of the specified frame. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Gets horizontal distance between a frame and the surrounding text, in points. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Gets horizontal distance between the edge of the frame and the item specified by the [`RelativeHorizontalPosition`](./relativehorizontalposition/) property. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Returns `true` if the paragraph is a frame. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Gets the relative horizontal position of a frame. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Gets the relative vertical position of a frame. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Gets vertical alignment of the specified frame. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Specifies vertical distance (in points) between a frame and the surrounding text. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Gets vertical distance between the edge of the frame and the item specified by the [`RelativeVerticalPosition`](./relativeverticalposition/) property. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Gets the width of the specified frame, in points. |

## Remarks

This object is always created. If a paragraph is a frame, then all properties will contain respective values, otherwise all properties are set to their defaults.

Use [`IsFrame`](./isframe/) to check whether paragraph is a frame.

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
