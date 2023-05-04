---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words for .NET
description: ITextShaper ShapeText method. Returns Cluster objects generated from a sequence of text fragments. Length of the returned array is equal to length of runs. If run at an index has corresponding clusters then result at the same index will have them recorded in C#.
type: docs
weight: 10
url: /net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Returns [`Cluster`](../../cluster/) objects generated from a sequence of text fragments. Length of the returned array is equal to length of *runs*. If run at an index has corresponding clusters then result at the same index will have them recorded.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Parameter | Type | Description |
| --- | --- | --- |
| runs | String[] | A sequence of text fragments |
| direction | Direction | A direction of text |
| script | UnicodeScript | A script |
| fontFeatures | FontFeature[] | A set of features to consider |

### See Also

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* namespace [Aspose.Words.Shaping](../../itextshaper/)
* assembly [Aspose.Words](../../../)
