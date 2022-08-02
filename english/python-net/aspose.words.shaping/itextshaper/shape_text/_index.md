---
title: shape_text method
second_title: Aspose.Words for Python via .NET API Reference
description: "Returns [Cluster](../../cluster/) objects generated from a sequence of text fragments"
type: docs
weight: 10
url: /python-net/aspose.words.shaping/itextshaper/shape_text/
---

## shape_text(runs, direction, script, font_features) {#strlist_direction_unicodescript_fontfeaturelist}

Returns [Cluster](../../cluster/) objects generated from a sequence of text fragments.
Length of the returned array is equal to length of .
If run at an index has corresponding clusters then result at the same index will have them recorded.


```python
def shape_text(self, runs: List[str], direction: aspose.words.shaping.Direction, script: aspose.words.shaping.UnicodeScript, font_features: List[aspose.words.shaping.FontFeature]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| runs | List[str] |  |
| direction | [Direction](../../direction/) |  |
| script | [UnicodeScript](../../unicodescript/) |  |
| font_features | List[[FontFeature](../../fontfeature/)] |  |

### See Also

* module [aspose.words.shaping](../../)
* class [ITextShaper](../)

