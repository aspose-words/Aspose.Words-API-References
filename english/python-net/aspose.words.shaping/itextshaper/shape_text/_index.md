---
title: ITextShaper.shape_text method
linktitle: shape_text method
articleTitle: shape_text method
second_title: Aspose.Words for Python
description: "ITextShaper.shape_text method. Returns [Cluster](../../cluster/) objects generated from a sequence of text fragments"
type: docs
weight: 10
url: /python-net/aspose.words.shaping/itextshaper/shape_text/
---

## shape_text(runs, direction, script, enabled_font_features, variations) {#strlist_direction_unicodescript_fontfeaturelist_variationaxiscoordinatelist}

Returns [Cluster](../../cluster/) objects generated from a sequence of text fragments.
Length of the returned array is equal to length of *runs*.
If run at an index has corresponding clusters then result at the same index will have them recorded.


```python
def shape_text(self, runs: List[str], direction: aspose.words.shaping.Direction, script: aspose.words.shaping.UnicodeScript, enabled_font_features: List[aspose.words.shaping.FontFeature], variations: List[aspose.words.shaping.VariationAxisCoordinate]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| runs | List[str] | A sequence of text fragments |
| direction | [Direction](../../direction/) | A direction of text |
| script | [UnicodeScript](../../unicodescript/) | A script |
| enabled_font_features | List[[FontFeature](../../fontfeature/)] | A set of explicitly enabled OpenType features to consider |
| variations | List[[VariationAxisCoordinate](../../variationaxiscoordinate/)] | Font's variation axis values |

### See Also

* module [aspose.words.shaping](../../)
* class [ITextShaper](../)

