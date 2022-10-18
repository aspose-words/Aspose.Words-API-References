---
title: ChartLegend
second_title: Aspose.Words for Java API Reference
description: Represents chart legend properties.
type: docs
weight: 63
url: /java/com.aspose.words/chartlegend/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegend implements Cloneable
```

Represents chart legend properties.

To learn more, visit the **Working with Charts** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [ChartLegend()](#ChartLegend--) | Initializes a new instance of the [ChartLegend](../../com.aspose.words/chartlegend) class. |
## Methods

| Method | Description |
| --- | --- |
| [getLegendEntries()](#getLegendEntries--) | Returns a collection of legend entries for all series and trendlines of the parent chart. |
| [getPosition()](#getPosition--) | Specifies the position of the legend on a chart. |
| [setPosition(int value)](#setPosition-int-) | Specifies the position of the legend on a chart. |
| [getOverlay()](#getOverlay--) | Determines whether other chart elements shall be allowed to overlap legend. |
| [setOverlay(boolean value)](#setOverlay-boolean-) | Determines whether other chart elements shall be allowed to overlap legend. |
### ChartLegend() {#ChartLegend--}
```
public ChartLegend()
```


Initializes a new instance of the [ChartLegend](../../com.aspose.words/chartlegend) class.

### getLegendEntries() {#getLegendEntries--}
```
public ChartLegendEntryCollection getLegendEntries()
```


Returns a collection of legend entries for all series and trendlines of the parent chart.

**Returns:**
[ChartLegendEntryCollection](../../com.aspose.words/chartlegendentrycollection) - A collection of legend entries for all series and trendlines of the parent chart.
### getPosition() {#getPosition--}
```
public int getPosition()
```


Specifies the position of the legend on a chart. Default value is [LegendPosition.RIGHT](../../com.aspose.words/legendposition\#RIGHT).

**Returns:**
int - The corresponding  int  value. The returned value is one of [LegendPosition](../../com.aspose.words/legendposition) constants.
### setPosition(int value) {#setPosition-int-}
```
public void setPosition(int value)
```


Specifies the position of the legend on a chart. Default value is [LegendPosition.RIGHT](../../com.aspose.words/legendposition\#RIGHT).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LegendPosition](../../com.aspose.words/legendposition) constants. |

### getOverlay() {#getOverlay--}
```
public boolean getOverlay()
```


Determines whether other chart elements shall be allowed to overlap legend. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### setOverlay(boolean value) {#setOverlay-boolean-}
```
public void setOverlay(boolean value)
```


Determines whether other chart elements shall be allowed to overlap legend. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

