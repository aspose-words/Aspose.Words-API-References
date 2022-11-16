---
title: TableStyle
second_title: Aspose.Words for Java API 参考
description: 代表表格样式。
type: docs
weight: 552
url: /zh/java/com.aspose.words/tablestyle/
---

**遗产：**
java.lang.Object, [com.aspose.words.Style](../../com.aspose.words/style)
```
public class TableStyle extends Style
```

代表表格样式。

要了解更多信息，请访问**Working with Tables**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs--) |  |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRowAttrs()](#clearRowAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Style style)](#equals-com.aspose.words.Style-) | 与指定样式进行比较。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int-) |  |
| [getAliases()](#getAliases--) | 获取此样式的所有别名。 |
| [getAlignment()](#getAlignment--) | 指定表格样式的对齐方式。 |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages--) | 获取一个标志，该标志指示是否允许表行中的文本跨分页符拆分。 |
| [getBaseStyleName()](#getBaseStyleName--) | 获取/设置此样式所基于的样式的名称。 |
| [getBidi()](#getBidi--) | 获取这是否是从右到左表格的样式。 |
| [getBorders()](#getBorders--) | 获取样式的默认单元格边框的集合。 |
| [getBottomPadding()](#getBottomPadding--) | 获取要添加到表格单元格内容下方的空间量（以磅为单位）。 |
| [getBuiltIn()](#getBuiltIn--) | 如果此样式是 MS Word 中的内置样式之一，则为真。 |
| [getCellSpacing()](#getCellSpacing--) | 获取单元格之间的空间量（以磅为单位）。 |
| [getClass()](#getClass--) |  |
| [getColumnStripe()](#getColumnStripe--) | 当样式指定奇数/偶数列分段时，获取要包含在分段中的列数。 |
| [getConditionalStyles()](#getConditionalStyles--) | 可以为此表格样式定义的条件样式的集合。 |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int-) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取所有者文档。 |
| [getFont()](#getFont--) | 获取样式的字符格式。 |
| [getLeftIndent()](#getLeftIndent--) | 获取表示表格左缩进的值。 |
| [getLeftPadding()](#getLeftPadding--) | 获取要添加到表格单元格内容左侧的空间量（以磅为单位）。 |
| [getLinkedStyleName()](#getLinkedStyleName--) | 获取链接到此样式的样式的名称。 |
| [getList()](#getList--) | 获取定义此列表样式格式的列表。 |
| [getListFormat()](#getListFormat--) | 提供对段落样式的列表格式属性的访问。 |
| [getName()](#getName--) | 获取样式的名称。 |
| [getNextParagraphStyleName()](#getNextParagraphStyleName--) | 获取/设置样式的名称，该样式的名称将自动应用于插入到以指定样式格式化的段落之后的新段落。 |
| [getParagraphFormat()](#getParagraphFormat--) | 获取样式的段落格式。 |
| [getRightPadding()](#getRightPadding--) | 获取要添加到表格单元格内容右侧的空间量（以磅为单位）。 |
| [getRowStripe()](#getRowStripe--) | 当样式指定奇数/偶数行分段时，获取要包含在分段中的行数。 |
| [getShading()](#getShading--) | 得到一个[Shading](../../com.aspose.words/shading)引用表格单元格的阴影格式的对象。 |
| [getStyleIdentifier()](#getStyleIdentifier--) | 获取内置样式的独立于语言环境的样式标识符。 |
| [getStyles()](#getStyles--) | 获取该样式所属的样式集合。 |
| [getTopPadding()](#getTopPadding--) | 获取要添加到表格单元格内容上方的空间量（以磅为单位）。 |
| [getType()](#getType--) | 获取样式类型（段落或字符）。 |
| [getVerticalAlignment()](#getVerticalAlignment--) | 指定单元格的垂直对齐方式。 |
| [hashCode()](#hashCode--) |  |
| [isHeading()](#isHeading--) | 当样式是内置标题样式之一时为真。 |
| [isQuickStyle()](#isQuickStyle--) | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean-) | 指定此样式是否显示在 MS Word UI 内的快速样式库中。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | 从文档中删除指定的样式。 |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs--) |  |
| [setAlignment(int value)](#setAlignment-int-) | 指定表格样式的对齐方式。 |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean-) | 设置一个标志，指示是否允许表格行中的文本跨分页符进行拆分。 |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String-) | 获取/设置此样式所基于的样式的名称。 |
| [setBidi(boolean value)](#setBidi-boolean-) | 设置这是否是从右到左表格的样式。 |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | 设置要在表格单元格内容下方添加的空间量（以磅为单位）。 |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object-) |  |
| [setCellSpacing(double value)](#setCellSpacing-double-) | 设置单元格之间的空间量（以磅为单位）。 |
| [setColumnStripe(int value)](#setColumnStripe-int-) | 当样式指定奇数/偶数列条带时，设置要包含在条带中的列数。 |
| [setLeftIndent(double value)](#setLeftIndent-double-) | 设置表示表格左缩进的值。 |
| [setLeftPadding(double value)](#setLeftPadding-double-) | 设置要添加到表格单元格内容左侧的空间量（以磅为单位）。 |
| [setName(String value)](#setName-java.lang.String-) | 设置样式的名称。 |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String-) | 获取/设置样式的名称，该样式的名称将自动应用于插入到以指定样式格式化的段落之后的新段落。 |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRightPadding(double value)](#setRightPadding-double-) | 设置要添加到表格单元格内容右侧的空间量（以磅为单位）。 |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object-) |  |
| [setRowStripe(int value)](#setRowStripe-int-) | 当样式指定奇数/偶数行条带时，设置要包含在条带中的行数。 |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setTopPadding(double value)](#setTopPadding-double-) | 设置要在表格单元格内容上方添加的空间量（以磅为单位）。 |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int-) | 指定单元格的垂直对齐方式。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearCellAttrs() {#clearCellAttrs--}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs--}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style-}
```
public boolean equals(Style style)
```


与指定样式进行比较。样式 Istds 仅针对内置样式进行比较。比较中不包括样式默认值。递归比较基本样式、链接样式和下一段样式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) |  |

**退货：**
布尔值
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### fetchCellAttr(int key) {#fetchCellAttr-int-}
```
public Object fetchCellAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int-}
```
public Object fetchInheritedCellAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int-}
```
public Object fetchInheritedRowAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int-}
```
public Object fetchInheritedShadingAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int-}
```
public Object fetchRowAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getAliases() {#getAliases--}
```
public String[] getAliases()
```


获取此样式的所有别名。如果样式没有别名，则返回空字符串数组。

**退货：**
java.lang.字符串[] - 这种风格的所有别名。
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


指定表格样式的对齐方式。默认值为[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**退货：**
int - 相应的 int 值。返回值是其中之一[TableAlignment](../../com.aspose.words/tablealignment)常数。
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages--}
```
public boolean getAllowBreakAcrossPages()
```


获取一个标志，该标志指示是否允许表行中的文本跨分页符拆分。默认值为**true**.

**退货：**
boolean - 一个标志，指示表格行中的文本是否允许跨分页符拆分。
### getBaseStyleName() {#getBaseStyleName--}
```
public String getBaseStyleName()
```


获取/设置此样式所基于的样式的名称。如果样式不基于任何其他样式并且可以将其设置为空字符串，则这将是一个空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


获取这是否是从右到左表格的样式。

什么时候**true**，行中的单元格从右到左排列。

默认值为**false**.

**退货：**
boolean - 这是否是从右到左表格的样式。
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


获取样式的默认单元格边框的集合。

**退货：**
[BorderCollection](../../com.aspose.words/bordercollection) - 样式的默认单元格边框集合。
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


获取要添加到表格单元格内容下方的空间量（以磅为单位）。

**退货：**
double - 在表格单元格内容下方添加的空间量（以磅为单位）。
### getBuiltIn() {#getBuiltIn--}
```
public boolean getBuiltIn()
```


如果此样式是 MS Word 中的内置样式之一，则为真。

**退货：**
boolean - 相应的布尔值。
### getCellSpacing() {#getCellSpacing--}
```
public double getCellSpacing()
```


获取单元格之间的空间量（以磅为单位）。

**退货：**
double - 单元格之间的空间量（以磅为单位）。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getColumnStripe() {#getColumnStripe--}
```
public int getColumnStripe()
```


当样式指定奇数/偶数列分段时，获取要包含在分段中的列数。

**退货：**
int - 当样式指定奇数/偶数列条带时要包含在条带中的列数。
### getConditionalStyles() {#getConditionalStyles--}
```
public ConditionalStyleCollection getConditionalStyles()
```


可以为此表格样式定义的条件样式的集合。

**退货：**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection) - 相应的[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection)价值。
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getDirectCellAttr(int key) {#getDirectCellAttr-int-}
```
public Object getDirectCellAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**退货：**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int-}
```
public Object getDirectRowAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货：**
java.lang.Object
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取所有者文档。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase) - 所有者文件。
### getFont() {#getFont--}
```
public Font getFont()
```


获取样式的字符格式。

对于列表样式，此属性返回 null。

**退货：**
[Font](../../com.aspose.words/font) - 样式的字符格式。
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


获取表示表格左缩进的值。

**退货：**
double - 表示表格左缩进的值。
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


获取要添加到表格单元格内容左侧的空间量（以磅为单位）。

**退货：**
double - 添加到表格单元格内容左侧的空间量（以磅为单位）。
### getLinkedStyleName() {#getLinkedStyleName--}
```
public String getLinkedStyleName()
```


获取链接到此样式的样式的名称。如果没有链接任何样式，则返回空字符串。

**退货：**
java.lang.String - 链接到这个样式的名称。
### getList() {#getList--}
```
public List getList()
```


获取定义此列表样式格式的列表。

此属性仅对列表样式有效。对于其他样式类型，此属性返回 null。

**退货：**
[List](../../com.aspose.words/list) - 定义此列表样式格式的列表。
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


提供对段落样式的列表格式属性的访问。

此属性仅对段落样式有效。对于其他样式类型，此属性返回 null。

**退货：**
[ListFormat](../../com.aspose.words/listformat) - 相应的[ListFormat](../../com.aspose.words/listformat)价值。
### getName() {#getName--}
```
public String getName()
```


获取样式的名称。

不能为空字符串。

如果集合中已经存在具有此类名称的样式，则此样式将覆盖它。所有受影响的节点都将引用新样式。

**退货：**
java.lang.String - 样式的名称。
### getNextParagraphStyleName() {#getNextParagraphStyleName--}
```
public String getNextParagraphStyleName()
```


获取/设置样式的名称，该样式的名称将自动应用于插入到以指定样式格式化的段落之后的新段落。 Aspose.Words 不使用此属性。只有当您在 MS Word 中编辑文档时，才会自动应用下一个段落样式。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


获取样式的段落格式。

对于字符和列表样式，此属性返回 null。

**退货：**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 样式的段落格式。
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


获取要添加到表格单元格内容右侧的空间量（以磅为单位）。

**退货：**
double - 添加到表格单元格内容右侧的空间量（以磅为单位）。
### getRowStripe() {#getRowStripe--}
```
public int getRowStripe()
```


当样式指定奇数/偶数行分段时，获取要包含在分段中的行数。

**退货：**
int - 当样式指定奇数/偶数行分带时要包含在分带中的行数。
### getShading() {#getShading--}
```
public Shading getShading()
```


得到一个[Shading](../../com.aspose.words/shading)引用表格单元格的阴影格式的对象。

**退货：**
[Shading](../../com.aspose.words/shading) - 一个[Shading](../../com.aspose.words/shading)引用表格单元格的阴影格式的对象。
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


获取内置样式的独立于语言环境的样式标识符。

对于用户定义（自定义）样式，此属性返回[StyleIdentifier.USER](../../com.aspose.words/styleidentifier\#USER).

**退货：**
int - 内置样式的独立于语言环境的样式标识符。返回值是其中之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


获取该样式所属的样式集合。

**退货：**
[StyleCollection](../../com.aspose.words/stylecollection) 此样式所属的样式集合。
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


获取要添加到表格单元格内容上方的空间量（以磅为单位）。

**退货：**
double - 添加到表格单元格内容上方的空间量（以磅为单位）。
### getType() {#getType--}
```
public int getType()
```


获取样式类型（段落或字符）。

**退货：**
 int - 样式类型（段落或字符）。返回值是其中之一[StyleType](../../com.aspose.words/styletype)常数。
### getVerticalAlignment() {#getVerticalAlignment--}
```
public int getVerticalAlignment()
```


指定单元格的垂直对齐方式。默认值为[CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment\#TOP).

**退货：**
int - 相应的 int 值。返回值是其中之一[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isHeading() {#isHeading--}
```
public boolean isHeading()
```


当样式是内置标题样式之一时为真。

**退货：**
boolean - 相应的布尔值。
### isQuickStyle() {#isQuickStyle--}
```
public boolean isQuickStyle()
```


指定此样式是否显示在 MS Word UI 内的快速样式库中。

**退货：**
boolean - 相应的布尔值。
### isQuickStyle(boolean value) {#isQuickStyle-boolean-}
```
public void isQuickStyle(boolean value)
```


指定此样式是否显示在 MS Word UI 内的快速样式库中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public void remove()
```


从文档中删除指定的样式。样式移除对文档模型有以下影响：

 *  从相应的段落、运行和表格中删除对样式的所有引用。
 *  如果删除基本样式，则其格式将移至子样式。
 *  如果要删除的样式具有链接样式，则这两个样式都将被删除。

### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs--}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


指定表格样式的对齐方式。默认值为[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[TableAlignment](../../com.aspose.words/tablealignment)常数。 |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean-}
```
public void setAllowBreakAcrossPages(boolean value)
```


设置一个标志，指示是否允许表格行中的文本跨分页符进行拆分。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否允许表格行中的文本跨分页符拆分的标志。 |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String-}
```
public void setBaseStyleName(String value)
```


获取/设置此样式所基于的样式的名称。如果样式不基于任何其他样式并且可以将其设置为空字符串，则这将是一个空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


设置这是否是从右到左表格的样式。

什么时候**true**，行中的单元格从右到左排列。

默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 这是否是从右到左表格的样式。 |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


设置要在表格单元格内容下方添加的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在表格单元格内容下方添加的空间量（以磅为单位）。 |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object-}
```
public void setCellAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double-}
```
public void setCellSpacing(double value)
```


设置单元格之间的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 单元格之间的空间量（以磅为单位）。 |

### setColumnStripe(int value) {#setColumnStripe-int-}
```
public void setColumnStripe(int value)
```


当样式指定奇数/偶数列条带时，设置要包含在条带中的列数。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 当样式指定奇数/偶数列条带时，要包含在条带中的列数。 |

### setLeftIndent(double value) {#setLeftIndent-double-}
```
public void setLeftIndent(double value)
```


设置表示表格左缩进的值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 表示表格左缩进的值。 |

### setLeftPadding(double value) {#setLeftPadding-double-}
```
public void setLeftPadding(double value)
```


设置要添加到表格单元格内容左侧的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到表格单元格内容左侧的空间量（以磅为单位）。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置样式的名称。

不能为空字符串。

如果集合中已经存在具有此类名称的样式，则此样式将覆盖它。所有受影响的节点都将引用新样式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 样式的名称。 |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String-}
```
public void setNextParagraphStyleName(String value)
```


获取/设置样式的名称，该样式的名称将自动应用于插入到以指定样式格式化的段落之后的新段落。 Aspose.Words 不使用此属性。只有当您在 MS Word 中编辑文档时，才会自动应用下一个段落样式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


设置要添加到表格单元格内容右侧的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到表格单元格内容右侧的空间量（以磅为单位）。 |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object-}
```
public void setRowAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int-}
```
public void setRowStripe(int value)
```


当样式指定奇数/偶数行条带时，设置要包含在条带中的行数。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 当样式指定奇数/偶数行分带时要包含在分带中的行数。 |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


设置要在表格单元格内容上方添加的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到表格单元格内容上方的空间量（以磅为单位）。 |

### setVerticalAlignment(int value) {#setVerticalAlignment-int-}
```
public void setVerticalAlignment(int value)
```


指定单元格的垂直对齐方式。默认值为[CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment\#TOP).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[CellVerticalAlignment](../../com.aspose.words/cellverticalalignment)常数。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
