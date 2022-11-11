---
title: ChartAxis
second_title: Aspose.Words for Java API 参考
description:表示图表的轴选项。
type: docs
weight: 56
url: /zh/java/com.aspose.words/chartaxis/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Cloneable
```
public class ChartAxis implements Cloneable
```

表示图表的轴选项。

要了解更多信息，请访问**Working with Charts**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAxisBetweenCategories()](#getAxisBetweenCategories--) | 获取一个标志，该标志指示值轴是否与类别之间的类别轴相交。 |
| [getBaseTimeUnit()](#getBaseTimeUnit--) | 获取时间类别轴上表示的最小时间单位。 |
| [getCategory类型()](#getCategory类型--) | 获取类别轴的类型。 |
| [get班级()](#get班级--) |  |
| [getCrosses()](#getCrosses--) | 指定此轴如何与垂直轴相交。 |
| [getCrossesAt()](#getCrossesAt--) | 指定轴在垂直轴上的交叉位置。 |
| [getDisplayUnit()](#getDisplayUnit--) | 指定数值轴的显示单位的缩放值。 |
| [getDocument()](#getDocument--) | 返回标题持有者所属的文档。 |
| [getHidden()](#getHidden--) | 获取指示此轴是否隐藏的标志。 |
| [getMajorTickMark()](#getMajorTickMark--) | 获取主要刻度线。 |
| [getMajorUnit()](#getMajorUnit--) | 获取主要刻度线之间的距离。 |
| [getMajorUnitIsAuto()](#getMajorUnitIsAuto--) | 获取一个标志，该标志指示是否应使用主要刻度线之间的默认距离。 |
| [getMajorUnitScale()](#getMajorUnitScale--) | 获取时间类别轴上主要刻度线的刻度值。 |
| [getMinorTickMark()](#getMinorTickMark--) | 获取轴的次要刻度线。 |
| [getMinorUnit()](#getMinorUnit--) | 获取次要刻度线之间的距离。 |
| [getMinorUnitIsAuto()](#getMinorUnitIsAuto--) | 获取一个标志，该标志指示是否应使用次刻度线之间的默认距离。 |
| [getMinorUnitScale()](#getMinorUnitScale--) | 获取时间类别轴上次要刻度线的刻度值。 |
| [getNumberFormat()](#getNumberFormat--) | 返回一个[ChartNumberFormat](../../com.aspose.words/chartnumberformat)允许为轴定义数字格式的对象。 |
| [getReverseOrder()](#getReverseOrder--) | 获取一个标志，该标志指示轴的值是否应该以相反的顺序显示，即 |
| [getScaling()](#getScaling--) | 提供对轴缩放选项的访问。 |
| [getTickLabelAlignment()](#getTickLabelAlignment--) | 获取轴刻度标签的文本对齐方式。 |
| [getTickLabelOffset()](#getTickLabelOffset--) | 获取标签与轴的距离。 |
| [getTickLabelPosition()](#getTickLabelPosition--) | 获取刻度标签在轴上的位置。 |
| [getTickLabelSpacing()](#getTickLabelSpacing--) | 获取绘制刻度标签的间隔。 |
| [getTickLabelSpacingIsAuto()](#getTickLabelSpacingIsAuto--) | 获取一个标志，该标志指示是否应使用绘制刻度标签的自动间隔。 |
| [getTickMarkSpacing()](#getTickMarkSpacing--) | 获取绘制刻度线的间隔。 |
| [getTitle()](#getTitle--) |  |
| [getTitleDeleted()](#getTitleDeleted--) |  |
| [getTitlePosition()](#getTitlePosition--) |  |
| [get类型()](#get类型--) | 返回轴的类型。 |
| [hashCode()](#hashCode--) |  |
| [isInherited()](#isInherited--) |  |
| [isVisible()](#isVisible--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAxisBetweenCategories(boolean value)](#setAxisBetweenCategories-boolean-) | 设置一个标志，指示值轴是否与类别之间的类别轴相交。 |
| [setBaseTimeUnit(int value)](#setBaseTimeUnit-int-) | 设置时间类别轴上表示的最小时间单位。 |
| [setCategory类型(int value)](#setCategory类型-int-) | 设置类别轴的类型。 |
| [setCrosses(int value)](#setCrosses-int-) | 指定此轴如何与垂直轴相交。 |
| [setCrossesAt(double value)](#setCrossesAt-double-) | 指定轴在垂直轴上的交叉位置。 |
| [setHidden(boolean value)](#setHidden-boolean-) | 设置一个标志，指示此轴是否隐藏。 |
| [setMajorTickMark(int value)](#setMajorTickMark-int-) | 设置主要刻度线。 |
| [setMajorUnit(double value)](#setMajorUnit-double-) | 设置主要刻度线之间的距离。 |
| [setMajorUnitIsAuto(boolean value)](#setMajorUnitIsAuto-boolean-) | 设置一个标志，指示是否应使用主要刻度线之间的默认距离。 |
| [setMajorUnitScale(int value)](#setMajorUnitScale-int-) | 设置时间类别轴上主要刻度线的刻度值。 |
| [setMinorTickMark(int value)](#setMinorTickMark-int-) | 设置轴的次刻度线。 |
| [setMinorUnit(double value)](#setMinorUnit-double-) | 设置次要刻度线之间的距离。 |
| [setMinorUnitIsAuto(boolean value)](#setMinorUnitIsAuto-boolean-) | 设置一个标志，指示是否应使用小刻度线之间的默认距离。 |
| [setMinorUnitScale(int value)](#setMinorUnitScale-int-) | 设置时间类别轴上次要刻度线的刻度值。 |
| [setReverseOrder(boolean value)](#setReverseOrder-boolean-) | 设置一个标志，指示轴的值是否应该以相反的顺序显示，即 |
| [setTickLabelAlignment(int value)](#setTickLabelAlignment-int-) | 设置轴刻度标签的文本对齐方式。 |
| [setTickLabelOffset(int value)](#setTickLabelOffset-int-) | 设置标签与轴的距离。 |
| [setTickLabelPosition(int value)](#setTickLabelPosition-int-) | 设置刻度标签在轴上的位置。 |
| [setTickLabelSpacing(int value)](#setTickLabelSpacing-int-) | 设置绘制刻度标签的时间间隔。 |
| [setTickLabelSpacingIsAuto(boolean value)](#setTickLabelSpacingIsAuto-boolean-) | 设置一个标志，指示是否应使用绘图刻度标签的自动间隔。 |
| [setTickMarkSpacing(int value)](#setTickMarkSpacing-int-) | 设置绘制刻度线的间隔。 |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle-) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getAxisBetweenCategories() {#getAxisBetweenCategories--}
```
public boolean getAxisBetweenCategories()
```


获取一个标志，该标志指示值轴是否与类别之间的类别轴相交。该属性仅对值轴有效。 MS Office 2016 新图表不支持它。

**退货:**
boolean - 一个标志，指示值轴是否与类别之间的类别轴相交。
### getBaseTimeUnit() {#getBaseTimeUnit--}
```
public int getBaseTimeUnit()
```


获取时间类别轴上表示的最小时间单位。该属性仅对时间类别轴有效。

**退货:**
 int - 时间类别轴上表示的最小时间单位。返回值是以下之一[AxisTimeUnit](../../com.aspose.words/axistimeunit)常数。
### getCategory类型() {#getCategory类型--}
```
public int getCategory类型()
```


获取类别轴的类型。仅文本类别 ([AxisCategory类型.CATEGORY](../../com.aspose.words/axiscategorytype\#CATEGORY)) 在 MS Office 2016 新图表中是允许的。

**退货:**
 int - 类别轴的类型。返回值是以下之一[AxisCategory类型](../../com.aspose.words/axiscategorytype)常数。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCrosses() {#getCrosses--}
```
public int getCrosses()
```


指定此轴如何与垂直轴相交。

默认值为[AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses\#AUTOMATIC).

MS Office 2016 新图表不支持该属性。

**退货:**
int - 对应的 int 值。返回值是以下之一[AxisCrosses](../../com.aspose.words/axiscrosses)常数。
### getCrossesAt() {#getCrossesAt--}
```
public double getCrossesAt()
```


指定轴在垂直轴上的交叉位置。

该属性仅在以下情况下有效[getCrosses()](../../com.aspose.words/chartaxis\#getCrosses--) / [setCrosses(int)](../../com.aspose.words/chartaxis\#setCrosses-int-)设置为[AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses\#CUSTOM)MS Office 2016 新图表不支持它。

单位由轴的类型决定。当轴为数值轴时，该属性的值是数值轴上的十进制数。当轴是时间类别轴时，该值定义为相对于基准日期 (30/12/1899) 的整数天数。对于文本类别轴，该值是一个整数类别编号，从 1 开始作为第一个类别。

**退货:**
double - 对应的双精度值。
### getDisplayUnit() {#getDisplayUnit--}
```
public AxisDisplayUnit getDisplayUnit()
```


指定数值轴的显示单位的缩放值。该属性仅对值轴有效。

**退货:**
[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit) - 相应的[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit)价值。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


返回标题持有者所属的文档。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 所有权人所属的文件。
### getHidden() {#getHidden--}
```
public boolean getHidden()
```


获取指示此轴是否隐藏的标志。默认值为**false**.

**退货:**
boolean - 指示此轴是否隐藏的标志。
### getMajorTickMark() {#getMajorTickMark--}
```
public int getMajorTickMark()
```


获取主要刻度线。

**退货:**
 int - 主要刻度线。返回值是以下之一[AxisTickMark](../../com.aspose.words/axistickmark)常数。
### getMajorUnit() {#getMajorUnit--}
```
public double getMajorUnit()
```


获取主要刻度线之间的距离。

值的有效范围大于零。该属性对时间类别和值轴有影响。

设置此属性会设置[getMajorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMajorUnitIsAuto--) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMajorUnitIsAuto-boolean-)财产**false**.

**退货:**
double - 主要刻度线之间的距离。
### getMajorUnitIsAuto() {#getMajorUnitIsAuto--}
```
public boolean getMajorUnitIsAuto()
```


获取一个标志，该标志指示是否应使用主要刻度线之间的默认距离。该属性对时间类别和值轴有影响。

**退货:**
boolean - 一个标志，指示是否应使用主要刻度线之间的默认距离。
### getMajorUnitScale() {#getMajorUnitScale--}
```
public int getMajorUnitScale()
```


获取时间类别轴上主要刻度线的刻度值。该属性仅对时间类别轴有效。

**退货:**
 int - 时间类别轴上主要刻度线的刻度值。返回值是以下之一[AxisTimeUnit](../../com.aspose.words/axistimeunit)常数。
### getMinorTickMark() {#getMinorTickMark--}
```
public int getMinorTickMark()
```


获取轴的次要刻度线。

**退货:**
int - 轴的次要刻度线。返回值是以下之一[AxisTickMark](../../com.aspose.words/axistickmark)常数。
### getMinorUnit() {#getMinorUnit--}
```
public double getMinorUnit()
```


获取次要刻度线之间的距离。

值的有效范围大于零。该属性对时间类别和值轴有影响。

设置此属性会设置[getMinorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMinorUnitIsAuto--) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMinorUnitIsAuto-boolean-)财产**false**.

**退货:**
double - 次要刻度线之间的距离。
### getMinorUnitIsAuto() {#getMinorUnitIsAuto--}
```
public boolean getMinorUnitIsAuto()
```


获取一个标志，该标志指示是否应使用次刻度线之间的默认距离。该属性对时间类别和值轴有影响。

**退货:**
boolean - 指示是否应使用次刻度标记之间的默认距离的标志。
### getMinorUnitScale() {#getMinorUnitScale--}
```
public int getMinorUnitScale()
```


获取时间类别轴上次要刻度线的刻度值。该属性仅对时间类别轴有效。

**退货:**
int - 时间类别轴上的次要刻度线的刻度值。返回值是以下之一[AxisTimeUnit](../../com.aspose.words/axistimeunit)常数。
### getNumberFormat() {#getNumberFormat--}
```
public ChartNumberFormat getNumberFormat()
```


返回一个[ChartNumberFormat](../../com.aspose.words/chartnumberformat)允许为轴定义数字格式的对象。

**退货:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat) - 一个[ChartNumberFormat](../../com.aspose.words/chartnumberformat)允许为轴定义数字格式的对象。
### getReverseOrder() {#getReverseOrder--}
```
public boolean getReverseOrder()
```


获取一个标志，该标志指示轴的值是否应以相反的顺序显示，即从最大值到最小值。 MS Office 2016 新图表不支持该属性。默认值为**false**.

**退货:**
boolean - 指示轴的值是否应以相反顺序显示的标志，即
### getScaling() {#getScaling--}
```
public AxisScaling getScaling()
```


提供对轴缩放选项的访问。

**退货:**
[AxisScaling](../../com.aspose.words/axisscaling) - 相应的[AxisScaling](../../com.aspose.words/axisscaling)价值。
### getTickLabelAlignment() {#getTickLabelAlignment--}
```
public int getTickLabelAlignment()
```


获取轴刻度标签的文本对齐方式。

此属性仅对多行标签有效。

默认值为[ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment\#CENTER).

.

**退货:**
 int - 轴刻度标签的文本对齐方式。返回值是以下之一[ParagraphAlignment](../../com.aspose.words/paragraphalignment)常数。
### getTickLabelOffset() {#getTickLabelOffset--}
```
public int getTickLabelOffset()
```


获取标签与轴的距离。

该属性表示默认标签偏移的百分比。

有效范围为 0 到 1000%（含）。默认值为 100%。

该属性仅对类别轴有效。 MS Office 2016 新图表不支持它。

**退货:**
int - 标签到轴的距离。
### getTickLabelPosition() {#getTickLabelPosition--}
```
public int getTickLabelPosition()
```


获取刻度标签在轴上的位置。 MS Office 2016 新图表不支持该属性。

**退货:**
int - 刻度标签在轴上的位置。返回值是以下之一[AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition)常数。
### getTickLabelSpacing() {#getTickLabelSpacing--}
```
public int getTickLabelSpacing()
```


获取绘制刻度标签的间隔。

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。值的有效范围大于或等于 1。

设置此属性会设置[getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis\#getTickLabelSpacingIsAuto--) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis\#setTickLabelSpacingIsAuto-boolean-)财产**false**.

**退货:**
int - 绘制刻度标签的时间间隔。
### getTickLabelSpacingIsAuto() {#getTickLabelSpacingIsAuto--}
```
public boolean getTickLabelSpacingIsAuto()
```


获取一个标志，该标志指示是否应使用绘制刻度标签的自动间隔。

默认值为**true**.

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。

**退货:**
boolean - 指示是否应使用绘图刻度标签的自动间隔的标志。
### getTickMarkSpacing() {#getTickMarkSpacing--}
```
public int getTickMarkSpacing()
```


获取绘制刻度线的间隔。

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。

值的有效范围大于或等于 1。

**退货:**
int - 绘制刻度线的时间间隔。
### getTitle() {#getTitle--}
```
public ChartTitle getTitle()
```




**退货:**
[ChartTitle](../../com.aspose.words/charttitle)
### getTitleDeleted() {#getTitleDeleted--}
```
public boolean getTitleDeleted()
```




**退货:**
布尔值
### getTitlePosition() {#getTitlePosition--}
```
public int getTitlePosition()
```




**退货:**
整数
### get类型() {#get类型--}
```
public int get类型()
```


返回轴的类型。

**退货:**
 int - 轴的类型。返回值是以下之一[ChartAxis类型](../../com.aspose.words/chartaxistype)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isInherited() {#isInherited--}
```
public boolean isInherited()
```




**退货:**
布尔值
### isVisible() {#isVisible--}
```
public boolean isVisible()
```




**退货:**
布尔值
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAxisBetweenCategories(boolean value) {#setAxisBetweenCategories-boolean-}
```
public void setAxisBetweenCategories(boolean value)
```


设置一个标志，指示值轴是否与类别之间的类别轴相交。该属性仅对值轴有效。 MS Office 2016 新图表不支持它。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示值轴是否与类别之间的类别轴相交的标志。 |

### setBaseTimeUnit(int value) {#setBaseTimeUnit-int-}
```
public void setBaseTimeUnit(int value)
```


设置时间类别轴上表示的最小时间单位。该属性仅对时间类别轴有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 时间类别轴上表示的最小时间单位。该值必须是以下之一[AxisTimeUnit](../../com.aspose.words/axistimeunit)常数。 |

### setCategory类型(int value) {#setCategory类型-int-}
```
public void setCategory类型(int value)
```


设置类别轴的类型。仅文本类别 ([AxisCategory类型.CATEGORY](../../com.aspose.words/axiscategorytype\#CATEGORY)) 在 MS Office 2016 新图表中是允许的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 类别轴的类型。该值必须是以下之一[AxisCategory类型](../../com.aspose.words/axiscategorytype)常数。 |

### setCrosses(int value) {#setCrosses-int-}
```
public void setCrosses(int value)
```


指定此轴如何与垂直轴相交。

默认值为[AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses\#AUTOMATIC).

MS Office 2016 新图表不支持该属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[AxisCrosses](../../com.aspose.words/axiscrosses)常数。 |

### setCrossesAt(double value) {#setCrossesAt-double-}
```
public void setCrossesAt(double value)
```


指定轴在垂直轴上的交叉位置。

该属性仅在以下情况下有效[getCrosses()](../../com.aspose.words/chartaxis\#getCrosses--) / [setCrosses(int)](../../com.aspose.words/chartaxis\#setCrosses-int-)设置为[AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses\#CUSTOM)MS Office 2016 新图表不支持它。

单位由轴的类型决定。当轴为数值轴时，该属性的值是数值轴上的十进制数。当轴是时间类别轴时，该值定义为相对于基准日期 (30/12/1899) 的整数天数。对于文本类别轴，该值是一个整数类别编号，从 1 开始作为第一个类别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setHidden(boolean value) {#setHidden-boolean-}
```
public void setHidden(boolean value)
```


设置一个标志，指示此轴是否隐藏。默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示此轴是否隐藏的标志。 |

### setMajorTickMark(int value) {#setMajorTickMark-int-}
```
public void setMajorTickMark(int value)
```


设置主要刻度线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 主要的刻度线。该值必须是以下之一[AxisTickMark](../../com.aspose.words/axistickmark)常数。 |

### setMajorUnit(double value) {#setMajorUnit-double-}
```
public void setMajorUnit(double value)
```


设置主要刻度线之间的距离。

值的有效范围大于零。该属性对时间类别和值轴有影响。

设置此属性会设置[getMajorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMajorUnitIsAuto--) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMajorUnitIsAuto-boolean-)财产**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 主要刻度线之间的距离。 |

### setMajorUnitIsAuto(boolean value) {#setMajorUnitIsAuto-boolean-}
```
public void setMajorUnitIsAuto(boolean value)
```


设置一个标志，指示是否应使用主要刻度线之间的默认距离。该属性对时间类别和值轴有影响。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否应使用主要刻度线之间的默认距离的标志。 |

### setMajorUnitScale(int value) {#setMajorUnitScale-int-}
```
public void setMajorUnitScale(int value)
```


设置时间类别轴上主要刻度线的刻度值。该属性仅对时间类别轴有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 时间类别轴上主要刻度线的刻度值。该值必须是以下之一[AxisTimeUnit](../../com.aspose.words/axistimeunit)常数。 |

### setMinorTickMark(int value) {#setMinorTickMark-int-}
```
public void setMinorTickMark(int value)
```


设置轴的次刻度线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 轴的次要刻度线。该值必须是以下之一[AxisTickMark](../../com.aspose.words/axistickmark)常数。 |

### setMinorUnit(double value) {#setMinorUnit-double-}
```
public void setMinorUnit(double value)
```


设置次要刻度线之间的距离。

值的有效范围大于零。该属性对时间类别和值轴有影响。

设置此属性会设置[getMinorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMinorUnitIsAuto--) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMinorUnitIsAuto-boolean-)财产**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 次要刻度线之间的距离。 |

### setMinorUnitIsAuto(boolean value) {#setMinorUnitIsAuto-boolean-}
```
public void setMinorUnitIsAuto(boolean value)
```


设置一个标志，指示是否应使用小刻度线之间的默认距离。该属性对时间类别和值轴有影响。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否应使用次要刻度线之间的默认距离的标志。 |

### setMinorUnitScale(int value) {#setMinorUnitScale-int-}
```
public void setMinorUnitScale(int value)
```


设置时间类别轴上次要刻度线的刻度值。该属性仅对时间类别轴有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 时间类别轴上次要刻度线的刻度值。该值必须是以下之一[AxisTimeUnit](../../com.aspose.words/axistimeunit)常数。 |

### setReverseOrder(boolean value) {#setReverseOrder-boolean-}
```
public void setReverseOrder(boolean value)
```


设置一个标志，指示轴的值是否应该以相反的顺序显示，即从最大值到最小值。 MS Office 2016 新图表不支持该属性。默认值为**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示轴的值是否应以相反顺序显示的标志，即 |

### setTickLabelAlignment(int value) {#setTickLabelAlignment-int-}
```
public void setTickLabelAlignment(int value)
```


设置轴刻度标签的文本对齐方式。

此属性仅对多行标签有效。

默认值为[ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment\#CENTER).

.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 轴刻度标签的文本对齐方式。该值必须是以下之一[ParagraphAlignment](../../com.aspose.words/paragraphalignment)常数。 |

### setTickLabelOffset(int value) {#setTickLabelOffset-int-}
```
public void setTickLabelOffset(int value)
```


设置标签与轴的距离。

该属性表示默认标签偏移的百分比。

有效范围为 0 到 1000%（含）。默认值为 100%。

该属性仅对类别轴有效。 MS Office 2016 新图表不支持它。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 标签到轴的距离。 |

### setTickLabelPosition(int value) {#setTickLabelPosition-int-}
```
public void setTickLabelPosition(int value)
```


设置刻度标签在轴上的位置。 MS Office 2016 新图表不支持该属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 刻度标签在轴上的位置。该值必须是以下之一[AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition)常数。 |

### setTickLabelSpacing(int value) {#setTickLabelSpacing-int-}
```
public void setTickLabelSpacing(int value)
```


设置绘制刻度标签的时间间隔。

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。值的有效范围大于或等于 1。

设置此属性会设置[getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis\#getTickLabelSpacingIsAuto--) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis\#setTickLabelSpacingIsAuto-boolean-)财产**false**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 绘制刻度标签的间隔。 |

### setTickLabelSpacingIsAuto(boolean value) {#setTickLabelSpacingIsAuto-boolean-}
```
public void setTickLabelSpacingIsAuto(boolean value)
```


设置一个标志，指示是否应使用绘图刻度标签的自动间隔。

默认值为**true**.

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否应使用绘制刻度标签的自动间隔的标志。 |

### setTickMarkSpacing(int value) {#setTickMarkSpacing-int-}
```
public void setTickMarkSpacing(int value)
```


设置绘制刻度线的间隔。

该属性对文本类别和系列轴有效。 MS Office 2016 新图表不支持它。

值的有效范围大于或等于 1。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 绘制刻度线的间隔。 |

### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle-}
```
public void setTitle(ChartTitle value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle) |  |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean-}
```
public void setTitleDeleted(boolean value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
