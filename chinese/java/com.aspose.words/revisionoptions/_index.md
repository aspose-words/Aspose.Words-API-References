---
title: RevisionOptions
second_title: Aspose.Words for Java API Reference
description: 允许控制在布局过程中如何处理文档修订。
type: docs
weight: 488
url: /zh/java/com.aspose.words/revisionoptions/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class RevisionOptions implements Cloneable
```

允许控制在布局过程中如何处理文档修订。

要了解更多信息，请访问**Converting to Fixed-page Format**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getCommentColor()](#getCommentColor--) | 允许指定用于注释的颜色。 |
| [getDeletedTextColor()](#getDeletedTextColor--) | 允许指定用于已删除内容的颜色[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [getDeletedTextEffect()](#getDeletedTextEffect--) | 允许指定要应用于已删除内容的效果[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [getInsertedTextColor()](#getInsertedTextColor--) | 允许指定用于插入内容的颜色[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [getInsertedTextEffect()](#getInsertedTextEffect--) | 允许指定要应用于插入内容的效果[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [getMeasurementUnit()](#getMeasurementUnit--) | 允许为修订注释指定测量单位。 |
| [getMovedFromTextColor()](#getMovedFromTextColor--) | 允许指定用于移动内容的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedFromTextEffect()](#getMovedFromTextEffect--) | 允许指定要应用于内容移动区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedToTextColor()](#getMovedToTextColor--) | 允许指定要用于内容移动到的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getMovedToTextEffect()](#getMovedToTextEffect--) | 允许指定要应用于内容移动到的区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [getRevisedPropertiesColor()](#getRevisedPropertiesColor--) | 允许通过更改格式属性指定要用于内容的颜色[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT). |
| [getRevisedPropertiesEffect()](#getRevisedPropertiesEffect--) | 允许通过更改格式属性来指定内容区域的效果[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)是不允许的，会导致 java.lang.IllegalArgumentException。 |
| [getRevisionBarsColor()](#getRevisionBarsColor--) | 允许指定用于标识包含修订信息的文档行的侧栏的颜色。 |
| [getRevisionBarsPosition()](#getRevisionBarsPosition--) | 获取修订栏的渲染位置。 |
| [getRevisionBarsWidth()](#getRevisionBarsWidth--) | 获取修订条的宽度，点。 |
| [getShowInBalloons()](#getShowInBalloons--) | 允许指定是否在气球中呈现修订。 |
| [getShowOriginalRevision()](#getShowOriginalRevision--) | 允许指定是否应显示原始文本而不是修订文本。 |
| [getShowRevisionBars()](#getShowRevisionBars--) | 允许指定是否应在包含修订内容的行附近呈现修订栏。 |
| [getShowRevisionMarks()](#getShowRevisionMarks--) | 允许指定是否应使用特殊格式标记来标记修订文本。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCommentColor(int value)](#setCommentColor-int-) | 允许指定用于注释的颜色。 |
| [setDeletedTextColor(int value)](#setDeletedTextColor-int-) | 允许指定用于已删除内容的颜色[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [setDeletedTextEffect(int value)](#setDeletedTextEffect-int-) | 允许指定要应用于已删除内容的效果[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION). |
| [setInsertedTextColor(int value)](#setInsertedTextColor-int-) | 允许指定用于插入内容的颜色[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [setInsertedTextEffect(int value)](#setInsertedTextEffect-int-) | 允许指定要应用于插入内容的效果[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION). |
| [setMeasurementUnit(int value)](#setMeasurementUnit-int-) | 允许为修订注释指定测量单位。 |
| [setMovedFromTextColor(int value)](#setMovedFromTextColor-int-) | 允许指定用于移动内容的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedFromTextEffect(int value)](#setMovedFromTextEffect-int-) | 允许指定要应用于内容移动区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedToTextColor(int value)](#setMovedToTextColor-int-) | 允许指定要用于内容移动到的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setMovedToTextEffect(int value)](#setMovedToTextEffect-int-) | 允许指定要应用于内容移动到的区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING). |
| [setRevisedPropertiesColor(int value)](#setRevisedPropertiesColor-int-) | 允许通过更改格式属性指定要用于内容的颜色[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT). |
| [setRevisedPropertiesEffect(int value)](#setRevisedPropertiesEffect-int-) | 允许通过更改格式属性来指定内容区域的效果[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)是不允许的，会导致 java.lang.IllegalArgumentException。 |
| [setRevisionBarsColor(int value)](#setRevisionBarsColor-int-) | 允许指定用于标识包含修订信息的文档行的侧栏的颜色。 |
| [setRevisionBarsPosition(int value)](#setRevisionBarsPosition-int-) | 设置修订栏的渲染位置。 |
| [setRevisionBarsWidth(float value)](#setRevisionBarsWidth-float-) | 设置修订栏、点的宽度。 |
| [setShowInBalloons(int value)](#setShowInBalloons-int-) | 允许指定是否在气球中呈现修订。 |
| [setShowOriginalRevision(boolean value)](#setShowOriginalRevision-boolean-) | 允许指定是否应显示原始文本而不是修订文本。 |
| [setShowRevisionBars(boolean value)](#setShowRevisionBars-boolean-) | 允许指定是否应在包含修订内容的行附近呈现修订栏。 |
| [setShowRevisionMarks(boolean value)](#setShowRevisionMarks-boolean-) | 允许指定是否应使用特殊格式标记来标记修订文本。 |
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCommentColor() {#getCommentColor--}
```
public int getCommentColor()
```


允许指定用于注释的颜色。默认值为[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED).如果将此属性设置为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR)或者[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT)值，因此该属性将设置为默认颜色。

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getDeletedTextColor() {#getDeletedTextColor--}
```
public int getDeletedTextColor()
```


允许指定用于已删除内容的颜色[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getDeletedTextEffect() {#getDeletedTextEffect--}
```
public int getDeletedTextEffect()
```


允许指定要应用于已删除内容的效果[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION) .默认值为[RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#STRIKE-THROUGH)

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。
### getInsertedTextColor() {#getInsertedTextColor--}
```
public int getInsertedTextColor()
```


允许指定用于插入内容的颜色[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getInsertedTextEffect() {#getInsertedTextEffect--}
```
public int getInsertedTextEffect()
```


允许指定要应用于插入内容的效果[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) .默认值为[RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect\#UNDERLINE).的价值观[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)和[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)不允许并且会导致 java.lang.IllegalArgumentException。

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。
### getMeasurementUnit() {#getMeasurementUnit--}
```
public int getMeasurementUnit()
```


允许为修订注释指定测量单位。默认值为[MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits\#CENTIMETERS)

**退货:**
int - 对应的 int 值。返回值是以下之一[MeasurementUnits](../../com.aspose.words/measurementunits)常数。
### getMovedFromTextColor() {#getMovedFromTextColor--}
```
public int getMovedFromTextColor()
```


允许指定用于移动内容的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getMovedFromTextEffect() {#getMovedFromTextEffect--}
```
public int getMovedFromTextEffect()
```


允许指定要应用于内容移动区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。
### getMovedToTextColor() {#getMovedToTextColor--}
```
public int getMovedToTextColor()
```


允许指定要用于内容移动到的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getMovedToTextEffect() {#getMovedToTextEffect--}
```
public int getMovedToTextEffect()
```


允许指定要应用于内容移动到的区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect\#DOUBLE-UNDERLINE)的价值观[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)和[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)不允许并且会导致 java.lang.IllegalArgumentException。

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。
### getRevisedPropertiesColor() {#getRevisedPropertiesColor--}
```
public int getRevisedPropertiesColor()
```


允许通过更改格式属性指定要用于内容的颜色[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getRevisedPropertiesEffect() {#getRevisedPropertiesEffect--}
```
public int getRevisedPropertiesEffect()
```


允许通过更改格式属性来指定内容区域的效果[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)是不允许的，会导致 java.lang.IllegalArgumentException。

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。
### getRevisionBarsColor() {#getRevisionBarsColor--}
```
public int getRevisionBarsColor()
```


允许指定用于标识包含修订信息的文档行的侧栏的颜色。默认值为[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED).将此属性设置为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR)或者[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT)值将导致从布局中隐藏修订栏。

**退货:**
int - 对应的 int 值。返回值是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。
### getRevisionBarsPosition() {#getRevisionBarsPosition--}
```
public int getRevisionBarsPosition()
```


获取修订栏的渲染位置。默认值为[HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment\#OUTSIDE).的价值观[HorizontalAlignment.CENTER](../../com.aspose.words/horizontalalignment\#CENTER)和[HorizontalAlignment.INSIDE](../../com.aspose.words/horizontalalignment\#INSIDE)不允许并且会导致 java.lang.IllegalArgumentException。

**退货:**
int - 修订栏的渲染位置。返回值是以下之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。
### getRevisionBarsWidth() {#getRevisionBarsWidth--}
```
public float getRevisionBarsWidth()
```


获取修订条的宽度，点。

**退货:**
float - 修订条的宽度，点数。
### getShowInBalloons() {#getShowInBalloons--}
```
public int getShowInBalloons()
```


允许指定是否在气球中呈现修订。默认值为[ShowInBalloons.NONE](../../com.aspose.words/showinballoons\#NONE).请注意，修订不会在气球中呈现[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**退货:**
int - 对应的 int 值。返回值是以下之一[ShowInBalloons](../../com.aspose.words/showinballoons)常数。
### getShowOriginalRevision() {#getShowOriginalRevision--}
```
public boolean getShowOriginalRevision()
```


允许指定是否应显示原始文本而不是修订文本。默认值为假。

**退货:**
boolean - 对应的布尔值。
### getShowRevisionBars() {#getShowRevisionBars--}
```
public boolean getShowRevisionBars()
```


允许指定是否应在包含修订内容的行附近呈现修订栏。默认值为真。

**退货:**
boolean - 对应的布尔值。
### getShowRevisionMarks() {#getShowRevisionMarks--}
```
public boolean getShowRevisionMarks()
```


允许指定是否应使用特殊格式标记来标记修订文本。默认值为真。

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCommentColor(int value) {#setCommentColor-int-}
```
public void setCommentColor(int value)
```


允许指定用于注释的颜色。默认值为[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED).如果将此属性设置为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR)或者[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT)值，因此该属性将设置为默认颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setDeletedTextColor(int value) {#setDeletedTextColor-int-}
```
public void setDeletedTextColor(int value)
```


允许指定用于已删除内容的颜色[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setDeletedTextEffect(int value) {#setDeletedTextEffect-int-}
```
public void setDeletedTextEffect(int value)
```


允许指定要应用于已删除内容的效果[Revision类型.DELETION](../../com.aspose.words/revisiontype\#DELETION) .默认值为[RevisionTextEffect.STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#STRIKE-THROUGH)

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。 |

### setInsertedTextColor(int value) {#setInsertedTextColor-int-}
```
public void setInsertedTextColor(int value)
```


允许指定用于插入内容的颜色[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setInsertedTextEffect(int value) {#setInsertedTextEffect-int-}
```
public void setInsertedTextEffect(int value)
```


允许指定要应用于插入内容的效果[Revision类型.INSERTION](../../com.aspose.words/revisiontype\#INSERTION) .默认值为[RevisionTextEffect.UNDERLINE](../../com.aspose.words/revisiontexteffect\#UNDERLINE).的价值观[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)和[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)不允许并且会导致 java.lang.IllegalArgumentException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。 |

### setMeasurementUnit(int value) {#setMeasurementUnit-int-}
```
public void setMeasurementUnit(int value)
```


允许为修订注释指定测量单位。默认值为[MeasurementUnits.CENTIMETERS](../../com.aspose.words/measurementunits\#CENTIMETERS)

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[MeasurementUnits](../../com.aspose.words/measurementunits)常数。 |

### setMovedFromTextColor(int value) {#setMovedFromTextColor-int-}
```
public void setMovedFromTextColor(int value)
```


允许指定用于移动内容的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setMovedFromTextEffect(int value) {#setMovedFromTextEffect-int-}
```
public void setMovedFromTextEffect(int value)
```


允许指定要应用于内容移动区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。 |

### setMovedToTextColor(int value) {#setMovedToTextColor-int-}
```
public void setMovedToTextColor(int value)
```


允许指定要用于内容移动到的区域的颜色[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setMovedToTextEffect(int value) {#setMovedToTextEffect-int-}
```
public void setMovedToTextEffect(int value)
```


允许指定要应用于内容移动到的区域的效果[Revision类型.MOVING](../../com.aspose.words/revisiontype\#MOVING) .默认值为[RevisionTextEffect.DOUBLE\_UNDERLINE](../../com.aspose.words/revisiontexteffect\#DOUBLE-UNDERLINE)的价值观[RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)和[RevisionTextEffect.DOUBLE\_STRIKE\_THROUGH](../../com.aspose.words/revisiontexteffect\#DOUBLE-STRIKE-THROUGH)不允许并且会导致 java.lang.IllegalArgumentException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。 |

### setRevisedPropertiesColor(int value) {#setRevisedPropertiesColor-int-}
```
public void setRevisedPropertiesColor(int value)
```


允许通过更改格式属性指定要用于内容的颜色[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setRevisedPropertiesEffect(int value) {#setRevisedPropertiesEffect-int-}
```
public void setRevisedPropertiesEffect(int value)
```


允许通过更改格式属性来指定内容区域的效果[Revision类型.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE)默认值为[RevisionTextEffect.NONE](../../com.aspose.words/revisiontexteffect\#NONE) [RevisionTextEffect.HIDDEN](../../com.aspose.words/revisiontexteffect\#HIDDEN)是不允许的，会导致 java.lang.IllegalArgumentException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionTextEffect](../../com.aspose.words/revisiontexteffect)常数。 |

### setRevisionBarsColor(int value) {#setRevisionBarsColor-int-}
```
public void setRevisionBarsColor(int value)
```


允许指定用于标识包含修订信息的文档行的侧栏的颜色。默认值为[RevisionColor.RED](../../com.aspose.words/revisioncolor\#RED).将此属性设置为[RevisionColor.BY\_AUTHOR](../../com.aspose.words/revisioncolor\#BY-AUTHOR)或者[RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT)值将导致从布局中隐藏修订栏。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[RevisionColor](../../com.aspose.words/revisioncolor)常数。 |

### setRevisionBarsPosition(int value) {#setRevisionBarsPosition-int-}
```
public void setRevisionBarsPosition(int value)
```


设置修订栏的渲染位置。默认值为[HorizontalAlignment.OUTSIDE](../../com.aspose.words/horizontalalignment\#OUTSIDE).的价值观[HorizontalAlignment.CENTER](../../com.aspose.words/horizontalalignment\#CENTER)和[HorizontalAlignment.INSIDE](../../com.aspose.words/horizontalalignment\#INSIDE)不允许并且会导致 java.lang.IllegalArgumentException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 修订栏的渲染位置。该值必须是以下之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。 |

### setRevisionBarsWidth(float value) {#setRevisionBarsWidth-float-}
```
public void setRevisionBarsWidth(float value)
```


设置修订栏、点的宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 修订条的宽度，点。 |

### setShowInBalloons(int value) {#setShowInBalloons-int-}
```
public void setShowInBalloons(int value)
```


允许指定是否在气球中呈现修订。默认值为[ShowInBalloons.NONE](../../com.aspose.words/showinballoons\#NONE).请注意，修订不会在气球中呈现[CommentDisplayMode.SHOW\_IN\_ANNOTATIONS](../../com.aspose.words/commentdisplaymode\#SHOW-IN-ANNOTATIONS).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[ShowInBalloons](../../com.aspose.words/showinballoons)常数。 |

### setShowOriginalRevision(boolean value) {#setShowOriginalRevision-boolean-}
```
public void setShowOriginalRevision(boolean value)
```


允许指定是否应显示原始文本而不是修订文本。默认值为假。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowRevisionBars(boolean value) {#setShowRevisionBars-boolean-}
```
public void setShowRevisionBars(boolean value)
```


允许指定是否应在包含修订内容的行附近呈现修订栏。默认值为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowRevisionMarks(boolean value) {#setShowRevisionMarks-boolean-}
```
public void setShowRevisionMarks(boolean value)
```


允许指定是否应使用特殊格式标记来标记修订文本。默认值为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
