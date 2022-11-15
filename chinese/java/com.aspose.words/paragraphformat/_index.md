---
title: ParagraphFormat
second_title: Aspose.Words for Java API 参考
description: 表示段落的所有格式。
type: docs
weight: 446
url: /zh/java/com.aspose.words/paragraphformat/
---

**遗产:**
java.lang.Object
```
public class ParagraphFormat
```

表示段落的所有格式。

要了解更多信息，请访问**Working with Paragraphs**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 重置为默认段落格式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [getAddSpaceBetweenFarEastAndAlpha()](#getAddSpaceBetweenFarEastAndAlpha--) | 获取一个标志，该标志指示是否在当前段落中的拉丁文本区域和东亚文本区域之间自动调整字符间距。 |
| [getAddSpaceBetweenFarEastAndDigit()](#getAddSpaceBetweenFarEastAndDigit--) | 获取一个标志，指示是否在当前段落中的数字区域和东亚文本区域之间自动调整字符间距。 |
| [getAlignment()](#getAlignment--) | 获取段落的文本对齐方式。 |
| [getBidi()](#getBidi--) | 获取这是否是从右到左的段落。 |
| [getBorders()](#getBorders--) | 获取段落边框的集合。 |
| [getCharacterUnitFirstLineIndent()](#getCharacterUnitFirstLineIndent--) | 获取第一行或悬挂缩进的值（以字符为单位）。 |
| [getCharacterUnitLeftIndent()](#getCharacterUnitLeftIndent--) | 获取指定段落的左缩进值（以字符为单位）。 |
| [getCharacterUnitRightIndent()](#getCharacterUnitRightIndent--) | 获取指定段落的正确缩进值（以字符为单位）。 |
| [getClass()](#getClass--) |  |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDropCapPosition()](#getDropCapPosition--) | 获取首字下沉文本的位置。 |
| [getFarEastLineBreakControl()](#getFarEastLineBreakControl--) | 获取一个标志，指示是否将东亚换行规则应用于当前段落。 |
| [getFirstLineIndent()](#getFirstLineIndent--) | 获取第一行或悬挂缩进的值（以磅为单位）。 |
| [getHangingPunctuation()](#getHangingPunctuation--) | 获取一个标志，该标志指示是否为当前段落启用悬挂标点符号。 |
| [getKeepTogether()](#getKeepTogether--) | 如果段落中的所有行都保留在同一页上，则为真。 |
| [getKeepWithNext()](#getKeepWithNext--) | 如果该段落要与其后的段落保持在同一页面上，则为真。 |
| [getLeftIndent()](#getLeftIndent--) | 获取表示段落左缩进的值（以磅为单位）。 |
| [getLineSpacing()](#getLineSpacing--) | 获取段落的行距（以磅为单位）。 |
| [getLineSpacingRule()](#getLineSpacingRule--) | 获取段落的行间距。 |
| [getLineUnitAfter()](#getLineUnitAfter--) | 获取段落后的间距量（以网格线表示）。 |
| [getLineUnitBefore()](#getLineUnitBefore--) | 获取段落前的间距量（以网格线表示）。 |
| [getLinesToDrop()](#getLinesToDrop--) | 获取用于计算首字下沉高度的段落文本的行数。 |
| [getNoSpaceBetweenParagraphsOfSameStyle()](#getNoSpaceBetweenParagraphsOfSameStyle--) | 当为真时，[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-)和[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-)相同样式的段落之间将被忽略。 |
| [getOutlineLevel()](#getOutlineLevel--) | 指定文档中段落的大纲级别。 |
| [getPageBreakBefore()](#getPageBreakBefore--) | 如果在段落前强制分页，则为真。 |
| [getRightIndent()](#getRightIndent--) | 获取表示段落正确缩进的值（以磅为单位）。 |
| [getShading()](#getShading--) | 返回一个 Shading 对象，该对象引用段落的底纹格式。 |
| [getSnapToGrid()](#getSnapToGrid--) | 指定在布置段落中的内容时，当前段落是否应使用每页设置的文档网格线。 |
| [getSpaceAfter()](#getSpaceAfter--) | 获取段落后的间距量（以磅为单位）。 |
| [getSpaceAfterAuto()](#getSpaceAfterAuto--) | 如果自动设置段落后的间距量，则为真。 |
| [getSpaceBefore()](#getSpaceBefore--) | 获取段落前的间距量（以磅为单位）。 |
| [getSpaceBeforeAuto()](#getSpaceBeforeAuto--) | 如果自动设置段落前的间距量，则为真。 |
| [getStyle()](#getStyle--) | 获取应用于此格式的段落样式。 |
| [getStyleIdentifier()](#getStyleIdentifier--) | 获取应用于此格式的段落样式的与区域设置无关的样式标识符。 |
| [getStyleName()](#getStyleName--) | 获取应用于此格式的段落样式的名称。 |
| [getSuppressAutoHyphens()](#getSuppressAutoHyphens--) | 指定当前段落是否应免除文档设置中应用的任何断字。 |
| [getSuppressLineNumbers()](#getSuppressLineNumbers--) | 指定当前段落的行是否应免除在父节中应用的行编号。 |
| [getTabStops()](#getTabStops--) | 获取为此对象定义的自定义制表位的集合。 |
| [getWidowControl()](#getWidowControl--) | 如果段落中的第一行和最后一行要与段落的其余部分保持在同一页上，则为真。 |
| [getWordWrap()](#getWordWrap--) | 如果这个属性是**false**单词中间的拉丁文字可以为当前段落换行。 |
| [hashCode()](#hashCode--) |  |
| [isHeading()](#isHeading--) | 当段落样式是内置标题样式之一时为真。 |
| [isListItem()](#isListItem--) | 当段落是项目符号或编号列表中的项目时为真。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAddSpaceBetweenFarEastAndAlpha(boolean value)](#setAddSpaceBetweenFarEastAndAlpha-boolean-) | 设置一个标志，指示是否在当前段落中的拉丁文本区域和东亚文本区域之间自动调整字符间距。 |
| [setAddSpaceBetweenFarEastAndDigit(boolean value)](#setAddSpaceBetweenFarEastAndDigit-boolean-) | 设置一个标志，指示是否在当前段落中的数字区域和东亚文本区域之间自动调整字符间距。 |
| [setAlignment(int value)](#setAlignment-int-) | 设置段落的文本对齐方式。 |
| [setBidi(boolean value)](#setBidi-boolean-) | 设置这是否是从右到左的段落。 |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setCharacterUnitFirstLineIndent(double value)](#setCharacterUnitFirstLineIndent-double-) | 设置第一行或悬挂缩进的值（以字符为单位）。 |
| [setCharacterUnitLeftIndent(double value)](#setCharacterUnitLeftIndent-double-) | 设置指定段落的左缩进值（以字符为单位）。 |
| [setCharacterUnitRightIndent(double value)](#setCharacterUnitRightIndent-double-) | 为指定段落设置正确的缩进值（以字符为单位）。 |
| [setDropCapPosition(int value)](#setDropCapPosition-int-) | 设置首字下沉文本的位置。 |
| [setFarEastLineBreakControl(boolean value)](#setFarEastLineBreakControl-boolean-) | 设置一个标志，指示是否将东亚换行规则应用于当前段落。 |
| [setFirstLineIndent(double value)](#setFirstLineIndent-double-) | 设置第一行或悬挂缩进的值（以磅为单位）。 |
| [setHangingPunctuation(boolean value)](#setHangingPunctuation-boolean-) | 设置一个标志，指示是否为当前段落启用悬挂标点符号。 |
| [setKeepTogether(boolean value)](#setKeepTogether-boolean-) | 如果段落中的所有行都保留在同一页上，则为真。 |
| [setKeepWithNext(boolean value)](#setKeepWithNext-boolean-) | 如果该段落要与其后的段落保持在同一页面上，则为真。 |
| [setLeftIndent(double value)](#setLeftIndent-double-) | 设置代表段落左缩进的值（以磅为单位）。 |
| [setLineSpacing(double value)](#setLineSpacing-double-) | 设置段落的行距（以磅为单位）。 |
| [setLineSpacingRule(int value)](#setLineSpacingRule-int-) | 设置段落的行距。 |
| [setLineUnitAfter(double value)](#setLineUnitAfter-double-) | 设置段落后的间距量（以网格线为单位）。 |
| [setLineUnitBefore(double value)](#setLineUnitBefore-double-) | 设置段落前的间距量（以网格线为单位）。 |
| [setLinesToDrop(int value)](#setLinesToDrop-int-) | 设置用于计算首字下沉高度的段落文本的行数。 |
| [setNoSpaceBetweenParagraphsOfSameStyle(boolean value)](#setNoSpaceBetweenParagraphsOfSameStyle-boolean-) | 当为真时，[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-)和[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-)相同样式的段落之间将被忽略。 |
| [setOutlineLevel(int value)](#setOutlineLevel-int-) | 指定文档中段落的大纲级别。 |
| [setPageBreakBefore(boolean value)](#setPageBreakBefore-boolean-) | 如果在段落前强制分页，则为真。 |
| [setRightIndent(double value)](#setRightIndent-double-) | 设置代表段落右缩进的值（以磅为单位）。 |
| [setSnapToGrid(boolean value)](#setSnapToGrid-boolean-) | 指定在布置段落中的内容时，当前段落是否应使用每页设置的文档网格线。 |
| [setSpaceAfter(double value)](#setSpaceAfter-double-) | 设置段落后的间距量（以磅为单位）。 |
| [setSpaceAfterAuto(boolean value)](#setSpaceAfterAuto-boolean-) | 如果自动设置段落后的间距量，则为真。 |
| [setSpaceBefore(double value)](#setSpaceBefore-double-) | 设置段落前的间距量（以磅为单位）。 |
| [setSpaceBeforeAuto(boolean value)](#setSpaceBeforeAuto-boolean-) | 如果自动设置段落前的间距量，则为真。 |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | 设置应用于此格式的段落样式。 |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | 设置应用于此格式的段落样式的独立于区域设置的样式标识符。 |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | 设置应用于此格式的段落样式的名称。 |
| [setSuppressAutoHyphens(boolean value)](#setSuppressAutoHyphens-boolean-) | 指定当前段落是否应免除文档设置中应用的任何断字。 |
| [setSuppressLineNumbers(boolean value)](#setSuppressLineNumbers-boolean-) | 指定当前段落的行是否应免除在父节中应用的行编号。 |
| [setWidowControl(boolean value)](#setWidowControl-boolean-) | 如果段落中的第一行和最后一行要与段落的其余部分保持在同一页上，则为真。 |
| [setWordWrap(boolean value)](#setWordWrap-boolean-) | 如果这个属性是**false**单词中间的拉丁文字可以为当前段落换行。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


重置为默认段落格式。默认段落格式为普通样式、左对齐、无缩进、无间距、无边框和无底纹。

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
### getAddSpaceBetweenFarEastAndAlpha() {#getAddSpaceBetweenFarEastAndAlpha--}
```
public boolean getAddSpaceBetweenFarEastAndAlpha()
```


获取一个标志，该标志指示是否在当前段落中的拉丁文本区域和东亚文本区域之间自动调整字符间距。

**退货:**
boolean - 一个标志，指示是否在当前段落中的拉丁文本区域和东亚文本区域之间自动调整字符间距。
### getAddSpaceBetweenFarEastAndDigit() {#getAddSpaceBetweenFarEastAndDigit--}
```
public boolean getAddSpaceBetweenFarEastAndDigit()
```


获取一个标志，指示是否在当前段落中的数字区域和东亚文本区域之间自动调整字符间距。

**退货:**
boolean - 一个标志，指示是否在当前段落中的数字区域和东亚文本区域之间自动调整字符间距。
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


获取段落的文本对齐方式。

**退货:**
int - 段落的文本对齐方式。返回值是以下之一[ParagraphAlignment](../../com.aspose.words/paragraphalignment)常数。
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


获取这是否是从右到左的段落。

如果为 true，则本段中的运行和其他内联对象从右到左布局。

**退货:**
boolean - 这是否是从右到左的段落。
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取段落边框的集合。

**退货:**
[BorderCollection](../../com.aspose.words/bordercollection) - 段落边框的集合。
### getCharacterUnitFirstLineIndent() {#getCharacterUnitFirstLineIndent--}
```
public double getCharacterUnitFirstLineIndent()
```


获取第一行或悬挂缩进的值（以字符为单位）。

使用正值设置首行缩进，使用负值设置悬挂缩进。

**退货:**
double - 第一行或悬挂缩进的值（以字符为单位）。
### getCharacterUnitLeftIndent() {#getCharacterUnitLeftIndent--}
```
public double getCharacterUnitLeftIndent()
```


获取指定段落的左缩进值（以字符为单位）。

**退货:**
double - 指定段落的左缩进值（以字符为单位）。
### getCharacterUnitRightIndent() {#getCharacterUnitRightIndent--}
```
public double getCharacterUnitRightIndent()
```


获取指定段落的正确缩进值（以字符为单位）。

**退货:**
double - 指定段落的右缩进值（以字符为单位）。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
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
### getDropCapPosition() {#getDropCapPosition--}
```
public int getDropCapPosition()
```


获取首字下沉文本的位置。

**退货:**
 int - 首字下沉文本的位置。返回值是以下之一[DropCapPosition](../../com.aspose.words/dropcapposition)常数。
### getFarEastLineBreakControl() {#getFarEastLineBreakControl--}
```
public boolean getFarEastLineBreakControl()
```


获取一个标志，指示是否将东亚换行规则应用于当前段落。

**退货:**
boolean - 指示是否将东亚换行规则应用于当前段落的标志。
### getFirstLineIndent() {#getFirstLineIndent--}
```
public double getFirstLineIndent()
```


获取第一行或悬挂缩进的值（以磅为单位）。

使用正值设置首行缩进，使用负值设置悬挂缩进。

**退货:**
double - 第一行或悬挂缩进的值（以磅为单位）。
### getHangingPunctuation() {#getHangingPunctuation--}
```
public boolean getHangingPunctuation()
```


获取一个标志，该标志指示是否为当前段落启用悬挂标点符号。

**退货:**
boolean - 指示是否为当前段落启用悬挂标点符号的标志。
### getKeepTogether() {#getKeepTogether--}
```
public boolean getKeepTogether()
```


如果段落中的所有行都保留在同一页上，则为真。

**退货:**
boolean - 对应的布尔值。
### getKeepWithNext() {#getKeepWithNext--}
```
public boolean getKeepWithNext()
```


如果该段落要与其后的段落保持在同一页面上，则为真。

**退货:**
boolean - 对应的布尔值。
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


获取表示段落左缩进的值（以磅为单位）。

**退货:**
double - 代表段落左缩进的值（以磅为单位）。
### getLineSpacing() {#getLineSpacing--}
```
public double getLineSpacing()
```


获取段落的行距（以磅为单位）。

当 LineSpacingRule 属性设置为 AtLeast 时，行距可以大于或等于，但不能小于指定的 LineSpacing 值。

当 LineSpacingRule 属性设置为 Exactly 时，即使段落中使用了较大的字体，行距也不会从指定的 LineSpacing 值更改。

**退货:**
double - 段落的行距（以磅为单位）。
### getLineSpacingRule() {#getLineSpacingRule--}
```
public int getLineSpacingRule()
```


获取段落的行间距。

**退货:**
 int - 段落的行距。返回值是以下之一[LineSpacingRule](../../com.aspose.words/linespacingrule)常数。
### getLineUnitAfter() {#getLineUnitAfter--}
```
public double getLineUnitAfter()
```


获取段落后的间距量（以网格线表示）。

**退货:**
double - 段落后的间距（以网格线为单位）。
### getLineUnitBefore() {#getLineUnitBefore--}
```
public double getLineUnitBefore()
```


获取段落前的间距量（以网格线表示）。

**退货:**
double - 段落前的间距（以网格线为单位）。
### getLinesToDrop() {#getLinesToDrop--}
```
public int getLinesToDrop()
```


获取用于计算首字下沉高度的段落文本的行数。

**退货:**
int - 用于计算首字下沉高度的段落文本行数。
### getNoSpaceBetweenParagraphsOfSameStyle() {#getNoSpaceBetweenParagraphsOfSameStyle--}
```
public boolean getNoSpaceBetweenParagraphsOfSameStyle()
```


当为真时，[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-)和[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-)相同样式的段落之间将被忽略。

此设置仅在应用于段落样式时生效。如果直接应用于段落，则没有效果。

**退货:**
boolean - 对应的布尔值。
### getOutlineLevel() {#getOutlineLevel--}
```
public int getOutlineLevel()
```


指定文档中段落的大纲级别。

**退货:**
int - 对应的 int 值。返回值是以下之一[OutlineLevel](../../com.aspose.words/outlinelevel)常数。
### getPageBreakBefore() {#getPageBreakBefore--}
```
public boolean getPageBreakBefore()
```


如果在段落前强制分页，则为真。

**退货:**
boolean - 对应的布尔值。
### getRightIndent() {#getRightIndent--}
```
public double getRightIndent()
```


获取表示段落正确缩进的值（以磅为单位）。

**退货:**
double - 代表段落右缩进的值（以磅为单位）。
### getShading() {#getShading--}
```
public Shading getShading()
```


返回一个 Shading 对象，该对象引用段落的底纹格式。

**退货:**
[Shading](../../com.aspose.words/shading) 引用段落的阴影格式的 Shading 对象。
### getSnapToGrid() {#getSnapToGrid--}
```
public boolean getSnapToGrid()
```


指定在布置段落中的内容时，当前段落是否应使用每页设置的文档网格线。

**退货:**
boolean - 对应的布尔值。
### getSpaceAfter() {#getSpaceAfter--}
```
public double getSpaceAfter()
```


获取段落后的间距量（以磅为单位）。

时无效[getSpaceAfterAuto()](../../com.aspose.words/paragraphformat\#getSpaceAfterAuto--) / [setSpaceAfterAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceAfterAuto-boolean-)是真的。

有效值\\u200b\\u200brange 从 0 到 1584（含）。

**退货:**
double - 段落后的间距量（以磅为单位）。
### getSpaceAfterAuto() {#getSpaceAfterAuto--}
```
public boolean getSpaceAfterAuto()
```


如果自动设置段落后的间距量，则为真。

当设置为 true 时，覆盖的效果[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-).

当您将段落前间距和后间距设置为自动时，Microsoft Word 会根据以下规则自动在段落之间添加 14 磅间距：

 *  通常，在所有段落之后添加间距。
 *  在项目符号列表或编号列表中，仅在列表中的最后一项之后添加间距。列表项之间不添加间距。
 *  在嵌套的项目符号列表或编号列表中不添加间距。
 *  通常在表格后添加间距。
 *  如果表格是表格单元格中的最后一个块，则不会在表格后添加间距。
 *  在表格单元格的最后一段之后不添加间距。

**退货:**
boolean - 对应的布尔值。
### getSpaceBefore() {#getSpaceBefore--}
```
public double getSpaceBefore()
```


获取段落前的间距量（以磅为单位）。

时无效[getSpaceBeforeAuto()](../../com.aspose.words/paragraphformat\#getSpaceBeforeAuto--) / [setSpaceBeforeAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceBeforeAuto-boolean-)是真的。

有效值范围从 0 到 1584（含）。

**退货:**
double - 段落前的间距量（以磅为单位）。
### getSpaceBeforeAuto() {#getSpaceBeforeAuto--}
```
public boolean getSpaceBeforeAuto()
```


如果自动设置段落前的间距量，则为真。

当设置为 true 时，覆盖的效果[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-).

当您将段落前间距和后间距设置为自动时，Microsoft Word 会根据以下规则自动在段落之间添加 14 磅间距：

 *  通常，在所有段落之后添加间距。
 *  在项目符号列表或编号列表中，仅在列表中的最后一项之后添加间距。列表项之间不添加间距。
 *  在嵌套的项目符号列表或编号列表中不添加间距。
 *  通常在表格后添加间距。
 *  如果表格是表格单元格中的最后一个块，则不会在表格后添加间距。
 *  在表格单元格的最后一段之后不添加间距。

**退货:**
boolean - 对应的布尔值。
### getStyle() {#getStyle--}
```
public Style getStyle()
```


获取应用于此格式的段落样式。

**退货:**
[Style](../../com.aspose.words/style) 应用于此格式的段落样式。
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


获取应用于此格式的段落样式的与区域设置无关的样式标识符。

**退货:**
 int - 应用于此格式的段落样式的区域独立样式标识符。返回值是以下之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


获取应用于此格式的段落样式的名称。

**退货:**
java.lang.String - 应用于此格式的段落样式的名称。
### getSuppressAutoHyphens() {#getSuppressAutoHyphens--}
```
public boolean getSuppressAutoHyphens()
```


指定当前段落是否应免除文档设置中应用的任何断字。

**退货:**
boolean - 对应的布尔值。
### getSuppressLineNumbers() {#getSuppressLineNumbers--}
```
public boolean getSuppressLineNumbers()
```


指定当前段落的行是否应免除在父节中应用的行编号。

**退货:**
boolean - 对应的布尔值。
### getTabStops() {#getTabStops--}
```
public TabStopCollection getTabStops()
```


获取为此对象定义的自定义制表位的集合。

**退货:**
[TabStopCollection](../../com.aspose.words/tabstopcollection) - 为此对象定义的自定义制表位集合。
### getWidowControl() {#getWidowControl--}
```
public boolean getWidowControl()
```


如果段落中的第一行和最后一行要与段落的其余部分保持在同一页上，则为真。

**退货:**
boolean - 对应的布尔值。
### getWordWrap() {#getWordWrap--}
```
public boolean getWordWrap()
```


如果这个属性是**false**, 单词中间的拉丁文本可以换行为当前段落。否则，拉丁文本将被整个单词包裹。

**退货:**
boolean - 对应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isHeading() {#isHeading--}
```
public boolean isHeading()
```


当段落样式是内置标题样式之一时为真。

**退货:**
boolean - 对应的布尔值。
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


当段落是项目符号或编号列表中的项目时为真。

**退货:**
boolean - 对应的布尔值。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAddSpaceBetweenFarEastAndAlpha(boolean value) {#setAddSpaceBetweenFarEastAndAlpha-boolean-}
```
public void setAddSpaceBetweenFarEastAndAlpha(boolean value)
```


设置一个标志，指示是否在当前段落中的拉丁文本区域和东亚文本区域之间自动调整字符间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否在当前段落中的拉丁文本区域和东亚文本区域之间自动调整字符间距的标志。 |

### setAddSpaceBetweenFarEastAndDigit(boolean value) {#setAddSpaceBetweenFarEastAndDigit-boolean-}
```
public void setAddSpaceBetweenFarEastAndDigit(boolean value)
```


设置一个标志，指示是否在当前段落中的数字区域和东亚文本区域之间自动调整字符间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否在当前段落中的数字区域和东亚文本区域之间自动调整字符间距的标志。 |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


设置段落的文本对齐方式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 段落的文本对齐方式。该值必须是其中之一[ParagraphAlignment](../../com.aspose.words/paragraphalignment)常数。 |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


设置这是否是从右到左的段落。

如果为 true，则本段中的运行和其他内联对象从右到左布局。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 这是否是从右到左的段落。 |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCharacterUnitFirstLineIndent(double value) {#setCharacterUnitFirstLineIndent-double-}
```
public void setCharacterUnitFirstLineIndent(double value)
```


设置第一行或悬挂缩进的值（以字符为单位）。

使用正值设置首行缩进，使用负值设置悬挂缩进。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 第一行或悬挂缩进的值（以字符为单位）。 |

### setCharacterUnitLeftIndent(double value) {#setCharacterUnitLeftIndent-double-}
```
public void setCharacterUnitLeftIndent(double value)
```


设置指定段落的左缩进值（以字符为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 指定段落的左缩进值（以字符为单位）。 |

### setCharacterUnitRightIndent(double value) {#setCharacterUnitRightIndent-double-}
```
public void setCharacterUnitRightIndent(double value)
```


为指定段落设置正确的缩进值（以字符为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 指定段落的右缩进值（以字符为单位）。 |

### setDropCapPosition(int value) {#setDropCapPosition-int-}
```
public void setDropCapPosition(int value)
```


设置首字下沉文本的位置。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 首字下沉文本的位置。该值必须是其中之一[DropCapPosition](../../com.aspose.words/dropcapposition)常数。 |

### setFarEastLineBreakControl(boolean value) {#setFarEastLineBreakControl-boolean-}
```
public void setFarEastLineBreakControl(boolean value)
```


设置一个标志，指示是否将东亚换行规则应用于当前段落。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示东亚换行规则是否应用于当前段落的标志。 |

### setFirstLineIndent(double value) {#setFirstLineIndent-double-}
```
public void setFirstLineIndent(double value)
```


设置第一行或悬挂缩进的值（以磅为单位）。

使用正值设置首行缩进，使用负值设置悬挂缩进。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 第一行或悬挂缩进的值（以磅为单位）。 |

### setHangingPunctuation(boolean value) {#setHangingPunctuation-boolean-}
```
public void setHangingPunctuation(boolean value)
```


设置一个标志，指示是否为当前段落启用悬挂标点符号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否为当前段落启用悬挂标点的标志。 |

### setKeepTogether(boolean value) {#setKeepTogether-boolean-}
```
public void setKeepTogether(boolean value)
```


如果段落中的所有行都保留在同一页上，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setKeepWithNext(boolean value) {#setKeepWithNext-boolean-}
```
public void setKeepWithNext(boolean value)
```


如果该段落要与其后的段落保持在同一页面上，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


设置代表段落左缩进的值（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 代表段落左缩进的值（以磅为单位）。 |

### setLineSpacing(double value) {#setLineSpacing-double-}
```
public void setLineSpacing(double value)
```


设置段落的行距（以磅为单位）。

当 LineSpacingRule 属性设置为 AtLeast 时，行距可以大于或等于，但不能小于指定的 LineSpacing 值。

当 LineSpacingRule 属性设置为 Exactly 时，即使段落中使用了较大的字体，行距也不会从指定的 LineSpacing 值更改。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 段落的行距（以磅为单位）。 |

### setLineSpacingRule(int value) {#setLineSpacingRule-int-}
```
public void setLineSpacingRule(int value)
```


设置段落的行距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 段落的行距。该值必须是其中之一[LineSpacingRule](../../com.aspose.words/linespacingrule)常数。 |

### setLineUnitAfter(double value) {#setLineUnitAfter-double-}
```
public void setLineUnitAfter(double value)
```


设置段落后的间距量（以网格线为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 段落后的间距量（以网格线为单位）。 |

### setLineUnitBefore(double value) {#setLineUnitBefore-double-}
```
public void setLineUnitBefore(double value)
```


设置段落前的间距量（以网格线为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 段落前的间距（以网格线为单位）。 |

### setLinesToDrop(int value) {#setLinesToDrop-int-}
```
public void setLinesToDrop(int value)
```


设置用于计算首字下沉高度的段落文本的行数。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 用于计算首字下沉高度的段落文本的行数。 |

### setNoSpaceBetweenParagraphsOfSameStyle(boolean value) {#setNoSpaceBetweenParagraphsOfSameStyle-boolean-}
```
public void setNoSpaceBetweenParagraphsOfSameStyle(boolean value)
```


当为真时，[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-)和[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-)相同样式的段落之间将被忽略。

此设置仅在应用于段落样式时生效。如果直接应用于段落，则没有效果。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setOutlineLevel(int value) {#setOutlineLevel-int-}
```
public void setOutlineLevel(int value)
```


指定文档中段落的大纲级别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[OutlineLevel](../../com.aspose.words/outlinelevel)常数。 |

### setPageBreakBefore(boolean value) {#setPageBreakBefore-boolean-}
```
public void setPageBreakBefore(boolean value)
```


如果在段落前强制分页，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setRightIndent(double value) {#setRightIndent-double-}
```
public void setRightIndent(double value)
```


设置代表段落右缩进的值（以磅为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 代表段落右缩进的值（以磅为单位）。 |

### setSnapToGrid(boolean value) {#setSnapToGrid-boolean-}
```
public void setSnapToGrid(boolean value)
```


指定在布置段落中的内容时，当前段落是否应使用每页设置的文档网格线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpaceAfter(double value) {#setSpaceAfter-double-}
```
public void setSpaceAfter(double value)
```


设置段落后的间距量（以磅为单位）。

时无效[getSpaceAfterAuto()](../../com.aspose.words/paragraphformat\#getSpaceAfterAuto--) / [setSpaceAfterAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceAfterAuto-boolean-)是真的。

有效值\\u200b\\u200brange 从 0 到 1584（含）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 段落后的间距量（以磅为单位）。 |

### setSpaceAfterAuto(boolean value) {#setSpaceAfterAuto-boolean-}
```
public void setSpaceAfterAuto(boolean value)
```


如果自动设置段落后的间距量，则为真。

当设置为 true 时，覆盖的效果[getSpaceAfter()](../../com.aspose.words/paragraphformat\#getSpaceAfter--) / [setSpaceAfter(double)](../../com.aspose.words/paragraphformat\#setSpaceAfter-double-).

当您将段落前间距和后间距设置为自动时，Microsoft Word 会根据以下规则自动在段落之间添加 14 磅间距：

 *  通常，在所有段落之后添加间距。
 *  在项目符号列表或编号列表中，仅在列表中的最后一项之后添加间距。列表项之间不添加间距。
 *  在嵌套的项目符号列表或编号列表中不添加间距。
 *  通常在表格后添加间距。
 *  如果表格是表格单元格中的最后一个块，则不会在表格后添加间距。
 *  在表格单元格的最后一段之后不添加间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSpaceBefore(double value) {#setSpaceBefore-double-}
```
public void setSpaceBefore(double value)
```


设置段落前的间距量（以磅为单位）。

时无效[getSpaceBeforeAuto()](../../com.aspose.words/paragraphformat\#getSpaceBeforeAuto--) / [setSpaceBeforeAuto(boolean)](../../com.aspose.words/paragraphformat\#setSpaceBeforeAuto-boolean-)是真的。

有效值范围从 0 到 1584（含）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 段落前的间距量（以磅为单位）。 |

### setSpaceBeforeAuto(boolean value) {#setSpaceBeforeAuto-boolean-}
```
public void setSpaceBeforeAuto(boolean value)
```


如果自动设置段落前的间距量，则为真。

当设置为 true 时，覆盖的效果[getSpaceBefore()](../../com.aspose.words/paragraphformat\#getSpaceBefore--) / [setSpaceBefore(double)](../../com.aspose.words/paragraphformat\#setSpaceBefore-double-).

当您将段落前间距和后间距设置为自动时，Microsoft Word 会根据以下规则自动在段落之间添加 14 磅间距：

 *  通常，在所有段落之后添加间距。
 *  在项目符号列表或编号列表中，仅在列表中的最后一项之后添加间距。列表项之间不添加间距。
 *  在嵌套的项目符号列表或编号列表中不添加间距。
 *  通常在表格后添加间距。
 *  如果表格是表格单元格中的最后一个块，则不会在表格后添加间距。
 *  在表格单元格的最后一段之后不添加间距。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


设置应用于此格式的段落样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | 应用于此格式的段落样式。 |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


设置应用于此格式的段落样式的独立于区域设置的样式标识符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应用于此格式的段落样式的区域设置独立样式标识符。该值必须是其中之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。 |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


设置应用于此格式的段落样式的名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于此格式的段落样式的名称。 |

### setSuppressAutoHyphens(boolean value) {#setSuppressAutoHyphens-boolean-}
```
public void setSuppressAutoHyphens(boolean value)
```


指定当前段落是否应免除文档设置中应用的任何断字。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSuppressLineNumbers(boolean value) {#setSuppressLineNumbers-boolean-}
```
public void setSuppressLineNumbers(boolean value)
```


指定当前段落的行是否应免除在父节中应用的行编号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWidowControl(boolean value) {#setWidowControl-boolean-}
```
public void setWidowControl(boolean value)
```


如果段落中的第一行和最后一行要与段落的其余部分保持在同一页上，则为真。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWordWrap(boolean value) {#setWordWrap-boolean-}
```
public void setWordWrap(boolean value)
```


如果这个属性是**false**, 单词中间的拉丁文本可以换行为当前段落。否则，拉丁文本将被整个单词包裹。

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
