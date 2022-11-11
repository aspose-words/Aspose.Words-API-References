---
title: ChartDataLabel
second_title: Aspose.Words for Java API Reference
description: Represents data label on a chart point or trendline.
type: docs
weight: 58
url: /java/com.aspose.words/chartdatalabel/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataLabel implements Cloneable
```

Represents data label on a chart point or trendline.

To learn more, visit the **Working with Charts** documentation article.

On a series, the [ChartDataLabel](../../com.aspose.words/chartdatalabel) object is a member of the [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection). The [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) contains a [ChartDataLabel](../../com.aspose.words/chartdatalabel) object for each point.
## Methods

| Method | Description |
| --- | --- |
| [clearFormat()](#clearFormat--) | Clears format of this data label. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getIndex()](#getIndex--) | Specifies the index of the containing element. |
| [getNumberFormat()](#getNumberFormat--) | Returns number format of the parent element. |
| [getSeparator()](#getSeparator--) | Gets string separator used for the data labels on a chart. |
| [getShowBubbleSize()](#getShowBubbleSize--) | Allows to specify if bubble size is to be displayed for the data labels on a chart. |
| [getShowCategoryName()](#getShowCategoryName--) | Allows to specify if category name is to be displayed for the data labels on a chart. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange--) | Allows to specify if values from data labels range to be displayed in the data labels. |
| [getShowLeaderLines()](#getShowLeaderLines--) | Allows to specify if data label leader lines need be shown. |
| [getShowLegendKey()](#getShowLegendKey--) | Allows to specify if legend key is to be displayed for the data labels on a chart. |
| [getShowPercentage()](#getShowPercentage--) | Allows to specify if percentage value is to be displayed for the data labels on a chart. |
| [getShowSeriesName()](#getShowSeriesName--) | Gets a Boolean to indicate the series name display behavior for the data labels on a chart. |
| [getShowValue()](#getShowValue--) | Allows to specify if values are to be displayed in the data labels. |
| [hashCode()](#hashCode--) |  |
| [isHidden()](#isHidden--) | Gets/sets a flag indicating whether this label is hidden. |
| [isHidden(boolean value)](#isHidden-boolean-) | Gets/sets a flag indicating whether this label is hidden. |
| [isInherited()](#isInherited--) |  |
| [isVisible()](#isVisible--) | Returns true if this data label has something to display. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setSeparator(String value)](#setSeparator-java.lang.String-) | Sets string separator used for the data labels on a chart. |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean-) | Allows to specify if bubble size is to be displayed for the data labels on a chart. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean-) | Allows to specify if category name is to be displayed for the data labels on a chart. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean-) | Allows to specify if values from data labels range to be displayed in the data labels. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean-) | Allows to specify if data label leader lines need be shown. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean-) | Allows to specify if legend key is to be displayed for the data labels on a chart. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean-) | Allows to specify if percentage value is to be displayed for the data labels on a chart. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean-) | Sets a Boolean to indicate the series name display behavior for the data labels on a chart. |
| [setShowValue(boolean value)](#setShowValue-boolean-) | Allows to specify if values are to be displayed in the data labels. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormat() {#clearFormat--}
```
public void clearFormat()
```


Clears format of this data label. The properties are set to the default values defined in the parent data label collection.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getIndex() {#getIndex--}
```
public int getIndex()
```


Specifies the index of the containing element. This index shall determine which of the parent's children collection this element applies to. Default value is 0.

**Returns:**
int - The corresponding  int  value.
### getNumberFormat() {#getNumberFormat--}
```
public ChartNumberFormat getNumberFormat()
```


Returns number format of the parent element.

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat) - Number format of the parent element.
### getSeparator() {#getSeparator--}
```
public String getSeparator()
```


Gets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead.

**Returns:**
java.lang.String - String separator used for the data labels on a chart.
### getShowBubbleSize() {#getShowBubbleSize--}
```
public boolean getShowBubbleSize()
```


Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowCategoryName() {#getShowCategoryName--}
```
public boolean getShowCategoryName()
```


Allows to specify if category name is to be displayed for the data labels on a chart. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowDataLabelsRange() {#getShowDataLabelsRange--}
```
public boolean getShowDataLabelsRange()
```


Allows to specify if values from data labels range to be displayed in the data labels. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowLeaderLines() {#getShowLeaderLines--}
```
public boolean getShowLeaderLines()
```


Allows to specify if data label leader lines need be shown. Default value is false. Applies to Pie charts only. Leader lines create a visual connection between a data label and its corresponding data point.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowLegendKey() {#getShowLegendKey--}
```
public boolean getShowLegendKey()
```


Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowPercentage() {#getShowPercentage--}
```
public boolean getShowPercentage()
```


Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowSeriesName() {#getShowSeriesName--}
```
public boolean getShowSeriesName()
```


Gets a Boolean to indicate the series name display behavior for the data labels on a chart. True to show the series name. False to hide. By default false.

**Returns:**
boolean - A Boolean to indicate the series name display behavior for the data labels on a chart.
### getShowValue() {#getShowValue--}
```
public boolean getShowValue()
```


Allows to specify if values are to be displayed in the data labels. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isHidden() {#isHidden--}
```
public boolean isHidden()
```


Gets/sets a flag indicating whether this label is hidden. The default value is **false**.

**Returns:**
boolean - The corresponding  boolean  value.
### isHidden(boolean value) {#isHidden-boolean-}
```
public void isHidden(boolean value)
```


Gets/sets a flag indicating whether this label is hidden. The default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### isInherited() {#isInherited--}
```
public boolean isInherited()
```




**Returns:**
boolean
### isVisible() {#isVisible--}
```
public boolean isVisible()
```


Returns true if this data label has something to display.

**Returns:**
boolean - True if this data label has something to display.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setSeparator(String value) {#setSeparator-java.lang.String-}
```
public void setSeparator(String value)
```


Sets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | String separator used for the data labels on a chart. |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean-}
```
public void setShowBubbleSize(boolean value)
```


Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean-}
```
public void setShowCategoryName(boolean value)
```


Allows to specify if category name is to be displayed for the data labels on a chart. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean-}
```
public void setShowDataLabelsRange(boolean value)
```


Allows to specify if values from data labels range to be displayed in the data labels. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean-}
```
public void setShowLeaderLines(boolean value)
```


Allows to specify if data label leader lines need be shown. Default value is false. Applies to Pie charts only. Leader lines create a visual connection between a data label and its corresponding data point.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean-}
```
public void setShowLegendKey(boolean value)
```


Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean-}
```
public void setShowPercentage(boolean value)
```


Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean-}
```
public void setShowSeriesName(boolean value)
```


Sets a Boolean to indicate the series name display behavior for the data labels on a chart. True to show the series name. False to hide. By default false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A Boolean to indicate the series name display behavior for the data labels on a chart. |

### setShowValue(boolean value) {#setShowValue-boolean-}
```
public void setShowValue(boolean value)
```


Allows to specify if values are to be displayed in the data labels. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

