---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words for .NET
description: Discover iTextShaper's ShapeText method, which efficiently generates Cluster objects from text fragments, ensuring precise text formatting and alignment.
type: docs
weight: 10
url: /net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Returns [`Cluster`](../../cluster/) objects generated from a sequence of text fragments. Length of the returned array is equal to length of *runs*. If run at an index has corresponding clusters then result at the same index will have them recorded.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Parameter | Type | Description |
| --- | --- | --- |
| runs | String[] | A sequence of text fragments |
| direction | Direction | A direction of text |
| script | UnicodeScript | A script |
| enabledFontFeatures | FontFeature[] | A set of explicitly enabled OpenType features to consider |
| variations | VariationAxisCoordinate[] | Font's variation axis values |

### See Also

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* namespace [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* assembly [Aspose.Words](../../../)
