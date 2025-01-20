---
title: ITextShaper
linktitle: ITextShaper
second_title: Aspose.Words for Java
description: Provides methods for text shaping in Java.
type: docs
weight: 756
url: /java/com.aspose.words/itextshaper/
---
```
public interface ITextShaper
```

Provides methods for text shaping.
## Methods

| Method | Description |
| --- | --- |
| [shapeText(String[] runs, int direction, int script, int[] enabledFontFeatures, VariationAxisCoordinate[] variations)](#shapeText-java.lang.String---int-int-int---com.aspose.words.VariationAxisCoordinate) |  |
### shapeText(String[] runs, int direction, int script, int[] enabledFontFeatures, VariationAxisCoordinate[] variations) {#shapeText-java.lang.String---int-int-int---com.aspose.words.VariationAxisCoordinate}
```
public abstract Cluster[][] shapeText(String[] runs, int direction, int script, int[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| runs | java.lang.String[] |  |
| direction | int |  |
| script | int |  |
| enabledFontFeatures | int[] |  |
| variations | [VariationAxisCoordinate\[\]](../../com.aspose.words/variationaxiscoordinate/) |  |

**Returns:**
com.aspose.words.Cluster[][]
