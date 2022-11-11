---
title: CellFormat
second_title: Aspose.Words for Java API 参考
description:表示表格单元格的所有格式。
type: docs
weight: 50
url: /zh/java/com.aspose.words/cellformat/
---

**遗产:**
java.lang.Object
```
public class CellFormat
```

表示表格单元格的所有格式。

要了解更多信息，请访问**Working with Tables**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 重置为默认单元格格式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [getBorders()](#getBorders--) | 获取单元格边框的集合。 |
| [getBottomPadding()](#getBottomPadding--) | 获取要添加到单元格内容下方的空间量（以磅为单位）。 |
| [get班级()](#get班级--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getFitText()](#getFitText--) | 如果为 true，则适合单元格中的文本，将每个段落压缩到单元格的宽度。 |
| [getHorizontalMerge()](#getHorizontalMerge--) | 指定单元格如何与行中的其他单元格水平合并。 |
| [getLeftPadding()](#getLeftPadding--) | 获取要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [getOrientation()](#getOrientation--) | 获取表格单元格中文本的方向。 |
| [getPreferredWidth()](#getPreferredWidth--) | 获取单元格的首选宽度。 |
| [getRightPadding()](#getRightPadding--) | 获取要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [getShading()](#getShading--) | 返回一个 Shading 对象，该对象引用单元格的着色格式。 |
| [getTopPadding()](#getTopPadding--) | 获取要添加到单元格内容上方的空间量（以磅为单位）。 |
| [getVerticalAlignment()](#getVerticalAlignment--) | 获取单元格中文本的垂直对齐方式。 |
| [getVerticalMerge()](#getVerticalMerge--) | 指定单元格如何与其他单元格垂直合并。 |
| [getWidth()](#getWidth--) | 获取单元格的宽度（以磅为单位）。 |
| [getWrapText()](#getWrapText--) | 如果为 true，则为单元格换行文本。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | 设置要在单元格内容下方添加的空间量（以磅为单位）。 |
| [setFitText(boolean value)](#setFitText-boolean-) | 如果为 true，则适合单元格中的文本，将每个段落压缩到单元格的宽度。 |
| [setHorizontalMerge(int value)](#setHorizontalMerge-int-) | 指定单元格如何与行中的其他单元格水平合并。 |
| [setLeftPadding(double value)](#setLeftPadding-double-) | 设置要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [setOrientation(int value)](#setOrientation-int-) | 设置表格单元格中文本的方向。 |
| [setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)](#setPaddings-double-double-double-double-) | 设置要添加到单元格内容的左/上/右/下的空间量（以磅为单位）。 |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | 设置单元格的首选宽度。 |
| [setRightPadding(double value)](#setRightPadding-double-) | 设置要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [setTopPadding(double value)](#setTopPadding-double-) | 设置要在单元格内容上方添加的空间量（以磅为单位）。 |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | 设置单元格中文本的垂直对齐方式。 |
| [setVerticalMerge(int value)](#setVerticalMerge-int-) | 指定单元格如何与其他单元格垂直合并。 |
| [setWidth(double value)](#setWidth-double-) | 获取单元格的宽度（以磅为单位）。 |
| [setWrapText(boolean value)](#setWrapText-boolean-) | 如果为 true，则为单元格换行文本。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


重置为默认单元格格式。不改变单元格的宽度。

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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取单元格边框的集合。

**退货:**
[BorderCollection](../../com.aspose.words/bordercollection) - 单元格边界的集合。
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


获取要添加到单元格内容下方的空间量（以磅为单位）。

**退货:**
double - 在单元格内容下方添加的空间量（以磅为单位）。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getFitText() {#getFitText--}
```
public boolean getFitText()
```


如果为 true，则适合单元格中的文本，将每个段落压缩到单元格的宽度。

**退货:**
boolean - 对应的布尔值。
### getHorizontalMerge() {#getHorizontalMerge--}
```
public int getHorizontalMerge()
```


指定单元格如何与行中的其他单元格水平合并。

**退货:**
int - 对应的 int 值。返回值是以下之一[CellMerge](../../com.aspose.words/cellmerge)常数。
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


获取要添加到单元格内容左侧的空间量（以磅为单位）。

**退货:**
double - 添加到单元格内容左侧的空间量（以磅为单位）。
### getOrientation() {#getOrientation--}
```
public int getOrientation()
```


获取表格单元格中文本的方向。

**退货:**
 int - 表格单元格中文本的方向。返回值是以下之一[TextOrientation](../../com.aspose.words/textorientation)常数。
### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


获取单元格的首选宽度。

首选宽度（连同表格的自动调整选项）决定了表格布局算法如何计算单元格的实际宽度。表格布局可以在保存文档时由 Aspose.Words 执行，或者在显示文档时由 Microsoft Word 执行。

首选宽度可以以磅或百分比指定。首选宽度也可以指定为“auto”，这意味着没有指定首选宽度。

默认值为[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**退货:**
[PreferredWidth](../../com.aspose.words/preferredwidth) 单元格的首选宽度。
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


获取要添加到单元格内容右侧的空间量（以磅为单位）。

**退货:**
double - 添加到单元格内容右侧的空间量（以磅为单位）。
### getShading() {#getShading--}
```
public Shading getShading()
```


返回一个 Shading 对象，该对象引用单元格的着色格式。

**退货:**
[Shading](../../com.aspose.words/shading) - 引用单元格的阴影格式的 Shading 对象。
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


获取要添加到单元格内容上方的空间量（以磅为单位）。

**退货:**
double - 在单元格内容上方添加的空间量（以磅为单位）。
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


获取单元格中文本的垂直对齐方式。

**退货:**
 int - 单元格中文本的垂直对齐方式。返回值是以下之一[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment)常数。
### getVerticalMerge() {#getVerticalMerge--}
```
public int getVerticalMerge()
```


指定单元格如何与其他单元格垂直合并。

只有左右边界相同的单元格才能垂直合并。

垂直合并单元格时，合并单元格的显示区域合并。合并区域用于显示第一个垂直合并单元格的内容，其他所有垂直合并单元格必须为空。

**退货:**
int - 对应的 int 值。返回值是以下之一[CellMerge](../../com.aspose.words/cellmerge)常数。
### getWidth() {#getWidth--}
```
public double getWidth()
```


获取单元格的宽度（以磅为单位）。

宽度由 Aspose.Words 在文档加载和保存时计算。目前，并非支持表格、单元格和文档属性的所有组合。对于某些文档，返回的值可能不准确。在 MS Word 中打开文档时，它可能与 MS Word 计算的单元格宽度不完全匹配。

不建议设置此属性。无法保证单元格实际上具有设置的宽度。可以调整宽度以适应自动调整表格布局中的单元格内容。其他行中的单元格可能具有冲突的宽度设置。可以调整表格的大小以适应容器或满足表格宽度设置。考虑使用[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-)用于设置单元格宽度。设置此属性集[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-)从 15.8 版本开始隐含。

**退货:**
double - 单元格的宽度（以磅为单位）。
### getWrapText() {#getWrapText--}
```
public boolean getWrapText()
```


如果为 true，则为单元格换行文本。

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




### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


设置要在单元格内容下方添加的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在单元格内容下方添加的空间量（以磅为单位）。 |

### setFitText(boolean value) {#setFitText-boolean-}
```
public void setFitText(boolean value)
```


如果为 true，则适合单元格中的文本，将每个段落压缩到单元格的宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setHorizontalMerge(int value) {#setHorizontalMerge-int-}
```
public void setHorizontalMerge(int value)
```


指定单元格如何与行中的其他单元格水平合并。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[CellMerge](../../com.aspose.words/cellmerge)常数。 |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


设置要添加到单元格内容左侧的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到单元格内容左侧的空间量（以磅为单位）。 |

### setOrientation(int value) {#setOrientation-int-}
```
public void setOrientation(int value)
```


设置表格单元格中文本的方向。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 表格单元格中文本的方向。该值必须是以下之一[TextOrientation](../../com.aspose.words/textorientation)常数。 |

### setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding) {#setPaddings-double-double-double-double-}
```
public void setPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


设置要添加到单元格内容的左/上/右/下的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| leftPadding | double |  |
| topPadding | double |  |
| rightPadding | double |  |
| bottomPadding | double |  |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


设置单元格的首选宽度。

首选宽度（连同表格的自动调整选项）决定了表格布局算法如何计算单元格的实际宽度。表格布局可以在保存文档时由 Aspose.Words 执行，或者在显示文档时由 Microsoft Word 执行。

首选宽度可以以磅或百分比指定。首选宽度也可以指定为“auto”，这意味着没有指定首选宽度。

默认值为[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | 单元格的首选宽度。 |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


设置要添加到单元格内容右侧的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到单元格内容右侧的空间量（以磅为单位）。 |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


设置要在单元格内容上方添加的空间量（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在单元格内容上方添加的空间量（以磅为单位）。 |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


设置单元格中文本的垂直对齐方式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 单元格中文本的垂直对齐方式。该值必须是以下之一[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment)常数。 |

### setVerticalMerge(int value) {#setVerticalMerge-int-}
```
public void setVerticalMerge(int value)
```


指定单元格如何与其他单元格垂直合并。

只有左右边界相同的单元格才能垂直合并。

垂直合并单元格时，合并单元格的显示区域合并。合并区域用于显示第一个垂直合并单元格的内容，其他所有垂直合并单元格必须为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[CellMerge](../../com.aspose.words/cellmerge)常数。 |

### setWidth(double value) {#setWidth-double-}
```
public void setWidth(double value)
```


获取单元格的宽度（以磅为单位）。

宽度由 Aspose.Words 在文档加载和保存时计算。目前，并非支持表格、单元格和文档属性的所有组合。对于某些文档，返回的值可能不准确。在 MS Word 中打开文档时，它可能与 MS Word 计算的单元格宽度不完全匹配。

不建议设置此属性。无法保证单元格实际上具有设置的宽度。可以调整宽度以适应自动调整表格布局中的单元格内容。其他行中的单元格可能具有冲突的宽度设置。可以调整表格的大小以适应容器或满足表格宽度设置。考虑使用[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-)用于设置单元格宽度。设置此属性集[getPreferredWidth()](../../com.aspose.words/cellformat\#getPreferredWidth--) / [setPreferredWidth(com.aspose.words.PreferredWidth)](../../com.aspose.words/cellformat\#setPreferredWidth-com.aspose.words.PreferredWidth-)从 15.8 版本开始隐含。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 单元格的宽度（以磅为单位）。 |

### setWrapText(boolean value) {#setWrapText-boolean-}
```
public void setWrapText(boolean value)
```


如果为 true，则为单元格换行文本。

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
