---
title: Table
second_title: Aspose.Words for Java API 参考
description: 表示 Word 文档中的表格。
type: docs
weight: 548
url: /zh/java/com.aspose.words/table/
---

**遗产：**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Table extends CompositeNode
```

表示 Word 文档中的表格。

要了解更多信息，请访问**Working with Tables**文档文章。

**Table**是块级节点，可以是派生自的类的子节点**Story**或者**InlineStory**.

**Table**可以包含一个或多个**Row**节点。

一个最小的有效表需要至少有一个**Row**.
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [Table(DocumentBase doc)](#Table-com.aspose.words.DocumentBase-) | 初始化一个新的实例**Table**班级。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接待来访者。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [autoFit(int behavior)](#autoFit-int-) |  |
| [clearBorders()](#clearBorders--) | 删除此表格上的所有表格和单元格边框。 |
| [clearShading()](#clearShading--) | 删除表格上的所有阴影。 |
| [convertToHorizontallyMergedCells()](#convertToHorizontallyMergedCells--) | 将按宽度水平合并的单元格转换为按宽度合并的单元格[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-). |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [ensureMinimum()](#ensureMinimum--) | 如果表没有行，创建并追加一个**Row**. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAbsoluteHorizontalDistance()](#getAbsoluteHorizontalDistance--) | 获取表格属性指定的绝对水平浮动表格位置，以磅为单位。 |
| [getAbsoluteVerticalDistance()](#getAbsoluteVerticalDistance--) | 获取表属性指定的绝对垂直浮动表位置，以磅为单位。 |
| [getAlignment()](#getAlignment--) | 指定内嵌表格在文档中的对齐方式。 |
| [getAllowAutoFit()](#getAllowAutoFit--) | 允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适合其内容。 |
| [getAllowCellSpacing()](#getAllowCellSpacing--) | 获取“允许单元格间距”选项。 |
| [getAllowOverlap()](#getAllowOverlap--) | 获取浮动表格是否允许文档中的其他浮动对象在显示时与其范围重叠。 |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | 获取指定对象类型的第一个祖先。 |
| [getBidi()](#getBidi--) | 获取这是否是从右到左的表格。 |
| [getBottomPadding()](#getBottomPadding--) | 获取要添加到单元格内容下方的空间量（以磅为单位）。 |
| [getCellSpacing()](#getCellSpacing--) | 获取单元格之间的空间量（以磅为单位）。 |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDescription()](#getDescription--) | 获取此表的说明。 |
| [getDistanceBottom()](#getDistanceBottom--) | 获取表格底部和周围文本之间的距离，以磅为单位。 |
| [getDistanceLeft()](#getDistanceLeft--) | 获取表格左侧与周围文本之间的距离，以磅为单位。 |
| [getDistanceRight()](#getDistanceRight--) | 获取表格右边和周围文本之间的距离，以磅为单位。 |
| [getDistanceTop()](#getDistanceTop--) | 获取桌面与周围文本之间的距离，以磅为单位。 |
| [getDocument()](#getDocument--) | 获取此节点所属的文档。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstRow()](#getFirstRow--) | 返回第一个**Row**表中的节点。 |
| [getHorizontalAnchor()](#getHorizontalAnchor--) | 获取应根据其计算浮动表的水平定位的基础对象。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastRow()](#getLastRow--) | 返回最后一个**Row**表中的节点。 |
| [getLeftIndent()](#getLeftIndent--) | 获取表示表的左缩进的值。 |
| [getLeftPadding()](#getLeftPadding--) | 获取要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟在该节点之后的节点。 |
| [getNodeType()](#getNodeType--) | 退货**NodeType.Table**. |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父级。 |
| [getPreferredWidth()](#getPreferredWidth--) | 获取表格的首选宽度。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在该节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在该节点中的文档部分的对象。 |
| [getRelativeHorizontalAlignment()](#getRelativeHorizontalAlignment--) | 获取浮动表格的相对水平对齐方式。 |
| [getRelativeVerticalAlignment()](#getRelativeVerticalAlignment--) | 获取浮动表格的相对垂直对齐方式。 |
| [getRightPadding()](#getRightPadding--) | 获取要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [getRows()](#getRows--) | 提供对表行的类型化访问。 |
| [getStyle()](#getStyle--) | 获取应用于此表格的表格样式。 |
| [getStyleIdentifier()](#getStyleIdentifier--) | 获取应用于此表的表样式的与区域无关的样式标识符。 |
| [getStyleName()](#getStyleName--) | 获取应用于此表的表样式的名称。 |
| [getStyleOptions()](#getStyleOptions--) | 获取指定如何将表格样式应用于此表格的位标志。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTextWrapping()](#getTextWrapping--) | 得到[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-)表。 |
| [getTitle()](#getTitle--) | 获取此表的标题。 |
| [getTopPadding()](#getTopPadding--) | 获取要添加到单元格内容上方的空间量（以磅为单位）。 |
| [getVerticalAnchor()](#getVerticalAnchor--) | 获取应该从中计算浮动表的垂直定位的基础对象。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的引用节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 将指定节点插入到紧靠指定引用节点之前。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [iterator()](#iterator--) | 为该节点的子节点上的每个样式迭代提供支持。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 删除指定的子节点。 |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setAbsoluteHorizontalDistance(double value)](#setAbsoluteHorizontalDistance-double-) | 设置表格属性指定的绝对水平浮动表格位置，以磅为单位。 |
| [setAbsoluteVerticalDistance(double value)](#setAbsoluteVerticalDistance-double-) | 设置表格属性指定的绝对垂直浮动表格位置，以磅为单位。 |
| [setAlignment(int value)](#setAlignment-int-) | 指定内嵌表格在文档中的对齐方式。 |
| [setAllowAutoFit(boolean value)](#setAllowAutoFit-boolean-) | 允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适合其内容。 |
| [setAllowCellSpacing(boolean value)](#setAllowCellSpacing-boolean-) | 设置“允许单元格之间的间距”选项。 |
| [setBidi(boolean value)](#setBidi-boolean-) | 设置这是否是从右到左的表格。 |
| [setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)](#setBorder-int-int-double-java.awt.Color-boolean-) |  |
| [setBorders(int lineStyle, double lineWidth, Color color)](#setBorders-int-double-java.awt.Color-) |  |
| [setBottomPadding(double value)](#setBottomPadding-double-) | 设置要在单元格内容下方添加的空间量（以磅为单位）。 |
| [setCellSpacing(double value)](#setCellSpacing-double-) | 设置单元格之间的空间量（以磅为单位）。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setDescription(String value)](#setDescription-java.lang.String-) | 设置此表的说明。 |
| [setHorizontalAnchor(int value)](#setHorizontalAnchor-int-) | 获取应根据其计算浮动表的水平定位的基础对象。 |
| [setLeftIndent(double value)](#setLeftIndent-double-) | 设置表示表格左缩进的值。 |
| [setLeftPadding(double value)](#setLeftPadding-double-) | 设置要添加到单元格内容左侧的空间量（以磅为单位）。 |
| [setPreferredWidth(PreferredWidth value)](#setPreferredWidth-com.aspose.words.PreferredWidth-) | 设置表格的首选宽度。 |
| [setRelativeHorizontalAlignment(int value)](#setRelativeHorizontalAlignment-int-) | 设置浮动表格相对水平对齐方式。 |
| [setRelativeVerticalAlignment(int value)](#setRelativeVerticalAlignment-int-) | 设置浮动表格相对垂直对齐方式。 |
| [setRightPadding(double value)](#setRightPadding-double-) | 设置要添加到单元格内容右侧的空间量（以磅为单位）。 |
| [setShading(int texture, Color foregroundColor, Color backgroundColor)](#setShading-int-java.awt.Color-java.awt.Color-) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | 设置应用于此表格的表格样式。 |
| [setStyleIdentifier(int value)](#setStyleIdentifier-int-) | 设置应用于此表格的表格样式的区域设置独立样式标识符。 |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | 设置应用于此表格的表格样式的名称。 |
| [setStyleOptions(int value)](#setStyleOptions-int-) | 设置指定表格样式如何应用于此表格的位标志。 |
| [setTextWrapping(int value)](#setTextWrapping-int-) | 套[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-)表。 |
| [setTitle(String value)](#setTitle-java.lang.String-) | 设置此表的标题。 |
| [setTopPadding(double value)](#setTopPadding-double-) | 设置要在单元格内容上方添加的空间量（以磅为单位）。 |
| [setVerticalAnchor(int value)](#setVerticalAnchor-int-) | 获取应该从中计算浮动表的垂直定位的基础对象。 |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Table(DocumentBase doc) {#Table-com.aspose.words.DocumentBase-}
```
public Table(DocumentBase doc)
```


初始化一个新的实例**Table**班级。

什么时候**Table**已创建，它属于指定文档，但还不是文档的一部分，并且**ParentNode**一片空白。

追加**Table**对于文档，在要插入表格的故事中使用 InsertAfter 或 InsertBefore。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | 所有者文件。 |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


接待来访者。

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货：**
boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。调用 DocumentVisitor.VisitTableStart，然后为该部分的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitTableEnd。
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的末尾。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货：**
[Node](../../com.aspose.words/node) - 添加的节点。
### autoFit(int behavior) {#autoFit-int-}
```
public void autoFit(int behavior)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| behavior | int |  |

### clearBorders() {#clearBorders--}
```
public void clearBorders()
```


删除此表格上的所有表格和单元格边框。

### clearShading() {#clearShading--}
```
public void clearShading()
```


删除表格上的所有阴影。

### convertToHorizontallyMergedCells() {#convertToHorizontallyMergedCells--}
```
public void convertToHorizontallyMergedCells()
```


将按宽度水平合并的单元格转换为按宽度合并的单元格[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-).

表格单元格可以使用合并标志水平合并[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-)或使用单元格宽度[CellFormat.getWidth()](../../com.aspose.words/cellformat\#getWidth--) / [CellFormat.setWidth(double)](../../com.aspose.words/cellformat\#setWidth-double-).

当表格单元格按宽度属性合并时[CellFormat.getHorizontalMerge()](../../com.aspose.words/cellformat\#getHorizontalMerge--) / [CellFormat.setHorizontalMerge(int)](../../com.aspose.words/cellformat\#setHorizontalMerge-int-)是没有意义的，但有时使用合并标志是更方便的方式。

使用此方法将按宽度水平合并的表格单元格转换为按合并标志合并的单元格。

### dd() {#dd--}
```
public void dd()
```




### deepClone(boolean isCloneChildren) {#deepClone-boolean-}
```
public Node deepClone(boolean isCloneChildren)
```


创建节点的副本。

此方法用作节点的复制构造函数。克隆的节点没有父节点，但与原始节点属于同一个文档。

此方法始终执行节点的深层复制。这*isCloneChildren*参数指定是否也执行复制所有子节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True 递归克隆指定节点下的子树； false 仅克隆节点本身。 |

**退货：**
[Node](../../com.aspose.words/node) - 克隆节点。
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


如果表没有行，创建并追加一个**Row**.

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
### getAbsoluteHorizontalDistance() {#getAbsoluteHorizontalDistance--}
```
public double getAbsoluteHorizontalDistance()
```


获取表格属性指定的绝对水平浮动表格位置，以磅为单位。默认值为 0。

**退货：**
double - 由表格属性指定的绝对水平浮动表格位置，以磅为单位。
### getAbsoluteVerticalDistance() {#getAbsoluteVerticalDistance--}
```
public double getAbsoluteVerticalDistance()
```


获取表属性指定的绝对垂直浮动表位置，以磅为单位。默认值为 0。

**退货：**
double - 表属性指定的绝对垂直浮动表位置，以磅为单位。
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


指定内嵌表格在文档中的对齐方式。

默认值为[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**退货：**
int - 相应的 int 值。返回值是其中之一[TableAlignment](../../com.aspose.words/tablealignment)常数。
### getAllowAutoFit() {#getAllowAutoFit--}
```
public boolean getAllowAutoFit()
```


允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适合其内容。

默认值是true 。

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**退货：**
boolean - 相应的布尔值。
### getAllowCellSpacing() {#getAllowCellSpacing--}
```
public boolean getAllowCellSpacing()
```


获取“允许单元格间距”选项。

**退货：**
布尔值 - “允许单元格之间的间距”选项。
### getAllowOverlap() {#getAllowOverlap--}
```
public boolean getAllowOverlap()
```


获取浮动表格是否允许文档中的其他浮动对象在显示时与其范围重叠。默认值为 true 。

**退货：**
boolean - 浮动表格是否允许文档中的其他浮动对象在显示时与其范围重叠。
### getAncestor(int ancestorType) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestorType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | int |  |

**退货：**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class-}
```
public CompositeNode getAncestor(Class ancestorType)
```


获取指定对象类型的第一个祖先。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestorType | java.lang.Class | 要检索的祖先的对象类型。 |

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 指定类型的祖先，如果未找到此类型的祖先，则为 null。

如果祖先类型等于 ancestorType 或派生自 ancestorType，则祖先类型匹配。
### getBidi() {#getBidi--}
```
public boolean getBidi()
```


获取这是否是从右到左的表格。

为 true 时，此行中的单元格从右到左排列。

默认值为 false 。

**退货：**
boolean - 这是否是一个从右到左的表格。
### getBottomPadding() {#getBottomPadding--}
```
public double getBottomPadding()
```


获取要添加到单元格内容下方的空间量（以磅为单位）。

**退货：**
double - 在单元格内容下方添加的空间量（以磅为单位）。
### getCellSpacing() {#getCellSpacing--}
```
public double getCellSpacing()
```


获取单元格之间的空间量（以磅为单位）。

**退货：**
double - 单元格之间的空间量（以磅为单位）。
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**退货：**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


获取此节点的所有直接子节点。

笔记，[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--)相当于调用 GetChildNodes(NodeType.Any, false) 并在每次访问时创建并返回一个新集合。

如果没有子节点，则此属性返回一个空集合。

**退货：**
[NodeCollection](../../com.aspose.words/nodecollection) - 该节点的所有直接子节点。
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**退货：**
[NodeCollection](../../com.aspose.words/nodecollection)
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货：**
[CompositeNode](../../com.aspose.words/compositenode)
### getCount() {#getCount--}
```
public int getCount()
```


获取此节点的直接子节点数。

**退货：**
int - 此节点的直接子节点数。
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**退货：**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的密钥。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**退货：**
int - 相应的 int 值。
### getDescription() {#getDescription--}
```
public String getDescription()
```


获取此表的说明。它提供表中包含的信息的替代文本表示。

默认值为空字符串。

此属性对符合 ISO/IEC 29500 的 DOCX 文档有意义（[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)）。当保存为 ISO/IEC 29500 之前的格式时，该属性将被忽略。

**退货：**
java.lang.String - 这个表的描述。
### getDistanceBottom() {#getDistanceBottom--}
```
public double getDistanceBottom()
```


获取表格底部和周围文本之间的距离，以磅为单位。

**退货：**
double - 表格底部和周围文本之间的距离，以磅为单位。
### getDistanceLeft() {#getDistanceLeft--}
```
public double getDistanceLeft()
```


获取表格左侧与周围文本之间的距离，以磅为单位。

**退货：**
double - 表格左侧和周围文本之间的距离，以磅为单位。
### getDistanceRight() {#getDistanceRight--}
```
public double getDistanceRight()
```


获取表格右边和周围文本之间的距离，以磅为单位。

**退货：**
double - 表格右边和周围文本之间的距离，以磅为单位。
### getDistanceTop() {#getDistanceTop--}
```
public double getDistanceTop()
```


获取桌面与周围文本之间的距离，以磅为单位。

**退货：**
double - 桌面和周围文本之间的距离，以磅为单位。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取此节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建并且尚未添加到树中，或者如果它已从树中删除也是如此。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的第一个孩子。
### getFirstRow() {#getFirstRow--}
```
public Row getFirstRow()
```


返回第一个**Row**表中的节点。

**退货：**
[Row](../../com.aspose.words/row) - 首先**Row**表中的节点。
### getHorizontalAnchor() {#getHorizontalAnchor--}
```
public int getHorizontalAnchor()
```


获取应根据其计算浮动表的水平定位的基础对象。默认值为[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**退货：**
int - 应该从中计算浮动表的水平定位的基础对象。返回值是其中之一[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition)常数。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的最后一个孩子。
### getLastRow() {#getLastRow--}
```
public Row getLastRow()
```


返回最后一个**Row**表中的节点。

**退货：**
[Row](../../com.aspose.words/row) 最后**Row**表中的节点。
### getLeftIndent() {#getLeftIndent--}
```
public double getLeftIndent()
```


获取表示表的左缩进的值。

**退货：**
double - 表示表格左缩进的值。
### getLeftPadding() {#getLeftPadding--}
```
public double getLeftPadding()
```


获取要添加到单元格内容左侧的空间量（以磅为单位）。

**退货：**
double - 添加到单元格内容左侧的空间量（以磅为单位）。
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**退货：**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


获取紧跟在该节点之后的节点。如果没有下一个节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 紧接此节点之后的节点。
### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


退货**NodeType.Table**.

**退货：**
整数 -**NodeType.Table** .返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父级。

如果一个节点刚刚被创建并且还没有被添加到树中，或者如果它已经被从树中移除，则父节点为空。

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 此节点的直接父节点。
### getPreferredWidth() {#getPreferredWidth--}
```
public PreferredWidth getPreferredWidth()
```


获取表格的首选宽度。

默认值为[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**退货：**
[PreferredWidth](../../com.aspose.words/preferredwidth) - 表格的首选宽度。
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


获取紧接在该节点之前的节点。如果前面没有节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 紧接在该节点之前的节点。
### getRange() {#getRange--}
```
public Range getRange()
```


返回一个**Range**表示包含在该节点中的文档部分的对象。

**退货：**
[Range](../../com.aspose.words/range) - 一个**Range**表示包含在该节点中的文档部分的对象。
### getRelativeHorizontalAlignment() {#getRelativeHorizontalAlignment--}
```
public int getRelativeHorizontalAlignment()
```


获取浮动表格的相对水平对齐方式。

**退货：**
 int - 浮动表相对水平对齐方式。返回值是其中之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。
### getRelativeVerticalAlignment() {#getRelativeVerticalAlignment--}
```
public int getRelativeVerticalAlignment()
```


获取浮动表格的相对垂直对齐方式。

**退货：**
int - 浮动表相对垂直对齐方式。返回值是其中之一[VerticalAlignment](../../com.aspose.words/verticalalignment)常数。
### getRightPadding() {#getRightPadding--}
```
public double getRightPadding()
```


获取要添加到单元格内容右侧的空间量（以磅为单位）。

**退货：**
double - 添加到单元格内容右侧的空间量（以磅为单位）。
### getRows() {#getRows--}
```
public RowCollection getRows()
```


提供对表行的类型化访问。

**退货：**
[RowCollection](../../com.aspose.words/rowcollection) - 相应的[RowCollection](../../com.aspose.words/rowcollection)价值。
### getStyle() {#getStyle--}
```
public Style getStyle()
```


获取应用于此表格的表格样式。

**退货：**
[Style](../../com.aspose.words/style) - 应用于此表格的表格样式。
### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


获取应用于此表的表样式的与区域无关的样式标识符。

**退货：**
 int - 应用于此表的表样式的区域独立样式标识符。返回值是其中之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


获取应用于此表的表样式的名称。

**退货：**
java.lang.String - 应用于此表格的表格样式的名称。
### getStyleOptions() {#getStyleOptions--}
```
public int getStyleOptions()
```


获取指定如何将表格样式应用于此表格的位标志。

**退货：**
 int - 指定表格样式如何应用于此表格的位标志。返回值是按位组合[TableStyleOptions](../../com.aspose.words/tablestyleoptions)常数。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制字符和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货：**
java.lang.字符串
### getTextWrapping() {#getTextWrapping--}
```
public int getTextWrapping()
```


得到[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-)表。

**退货：**
整数 -\{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-)表。返回值是其中之一[TextWrapping](../../com.aspose.words/textwrapping)常数。
### getTitle() {#getTitle--}
```
public String getTitle()
```


获取此表的标题。它提供表中包含的信息的替代文本表示。

默认值为空字符串。

此属性对符合 ISO/IEC 29500 的 DOCX 文档有意义（[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)）。当保存为 ISO/IEC 29500 之前的格式时，该属性将被忽略。

**退货：**
java.lang.String - 此表的标题。
### getTopPadding() {#getTopPadding--}
```
public double getTopPadding()
```


获取要添加到单元格内容上方的空间量（以磅为单位）。

**退货：**
double - 在单元格内容上方添加的空间量（以磅为单位）。
### getVerticalAnchor() {#getVerticalAnchor--}
```
public int getVerticalAnchor()
```


获取应该从中计算浮动表的垂直定位的基础对象。默认值为[RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**退货：**
int - 应该从中计算浮动表的垂直定位的基础对象。返回值是其中之一[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition)常数。
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


如果此节点有任何子节点，则返回 true。

**退货：**
boolean - 如果此节点有任何子节点则为真。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


返回子节点数组中指定子节点的索引。如果在子节点中找不到该节点，则返回 -1。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**退货：**
整数
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


在指定的引用节点之后立即插入指定的节点。

如果 refChild 为 null，则在子节点列表的开头插入 newChild。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newNode 放置在 refNode 之后。 |

**退货：**
[Node](../../com.aspose.words/node) - 插入的节点。
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


将指定节点插入到紧靠指定引用节点之前。

如果 refChild 为 null，则在子节点列表的末尾插入 newChild。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newChild 放置在此节点之前。 |

**退货：**
[Node](../../com.aspose.words/node) - 插入的节点。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货：**
boolean - True 因为这个节点可以有子节点。
### iterator() {#iterator--}
```
public Iterator iterator()
```


为该节点的子节点上的每个样式迭代提供支持。

**退货：**
java.util.迭代器
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


根据前序树遍历算法获取下一个节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶端节点（极限）。 |

**退货：**
[Node](../../com.aspose.words/node) - 预定顺序中的下一个节点。如果到达根节点则为空。
### nodeTypeToString(int nodeType) {#nodeTypeToString-int-}
```
public static String nodeTypeToString(int nodeType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| nodeType | int |  |

**退货：**
java.lang.字符串
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node-}
```
public Node prependChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的开头。

如果 newChild 已经在树中，则首先将其删除。

如果被插入的节点是从另一个文档创建的，你应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货：**
[Node](../../com.aspose.words/node) - 添加的节点。
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


根据前序树遍历算法获取上一个节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶端节点（极限）。 |

**退货：**
[Node](../../com.aspose.words/node) 预购顺序中的前一个节点。如果到达根节点则为空。
### remove() {#remove--}
```
public void remove()
```


从父级中移除自身。

### removeAllChildren() {#removeAllChildren--}
```
public void removeAllChildren()
```


移除当前节点的所有子节点。

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node-}
```
public Node removeChild(Node oldChild)
```


删除指定的子节点。

删除节点后，oldChild 的父级设置为 null。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | 要删除的节点。 |

**退货：**
[Node](../../com.aspose.words/node) - 删除的节点。
### removeSmartTags() {#removeSmartTags--}
```
public void removeSmartTags()
```


删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。此方法不会删除智能标记的内容。

### selectNodes(String xpath) {#selectNodes-java.lang.String-}
```
public NodeList selectNodes(String xpath)
```


选择与 XPath 表达式匹配的节点列表。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货：**
[NodeList](../../com.aspose.words/nodelist) - 匹配 XPath 查询的节点列表。
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


选择与 XPath 表达式匹配的第一个节点。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货：**
[Node](../../com.aspose.words/node) - 与 XPath 查询匹配的第一个节点，如果未找到匹配节点，则为 null。
### setAbsoluteHorizontalDistance(double value) {#setAbsoluteHorizontalDistance-double-}
```
public void setAbsoluteHorizontalDistance(double value)
```


设置表格属性指定的绝对水平浮动表格位置，以磅为单位。默认值为 0。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 表属性指定的绝对水平浮动表位置，以磅为单位。 |

### setAbsoluteVerticalDistance(double value) {#setAbsoluteVerticalDistance-double-}
```
public void setAbsoluteVerticalDistance(double value)
```


设置表格属性指定的绝对垂直浮动表格位置，以磅为单位。默认值为 0。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 表属性指定的绝对垂直浮动表位置，以磅为单位。 |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


指定内嵌表格在文档中的对齐方式。

默认值为[TableAlignment.LEFT](../../com.aspose.words/tablealignment\#LEFT).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[TableAlignment](../../com.aspose.words/tablealignment)常数。 |

### setAllowAutoFit(boolean value) {#setAllowAutoFit-boolean-}
```
public void setAllowAutoFit(boolean value)
```


允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适合其内容。

默认值是true 。

**M:Aspose.Words.Tables.Table.AutoFit(Aspose.Words.Tables.AutoFitBehavior)**

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setAllowCellSpacing(boolean value) {#setAllowCellSpacing-boolean-}
```
public void setAllowCellSpacing(boolean value)
```


设置“允许单元格之间的间距”选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | “允许单元格间距”选项。 |

### setBidi(boolean value) {#setBidi-boolean-}
```
public void setBidi(boolean value)
```


设置这是否是从右到左的表格。

为 true 时，此行中的单元格从右到左排列。

默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 这是否是从右到左的表格。 |

### setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders) {#setBorder-int-int-double-java.awt.Color-boolean-}
```
public void setBorder(int borderType, int lineStyle, double lineWidth, Color color, boolean isOverrideCellBorders)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| borderType | int |  |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |
| isOverrideCellBorders | boolean |  |

### setBorders(int lineStyle, double lineWidth, Color color) {#setBorders-int-double-java.awt.Color-}
```
public void setBorders(int lineStyle, double lineWidth, Color color)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| lineStyle | int |  |
| lineWidth | double |  |
| color | java.awt.Color |  |

### setBottomPadding(double value) {#setBottomPadding-double-}
```
public void setBottomPadding(double value)
```


设置要在单元格内容下方添加的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在单元格内容下方添加的空间量（以磅为单位）。 |

### setCellSpacing(double value) {#setCellSpacing-double-}
```
public void setCellSpacing(double value)
```


设置单元格之间的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 单元格之间的空间量（以磅为单位）。 |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的密钥。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setDescription(String value) {#setDescription-java.lang.String-}
```
public void setDescription(String value)
```


设置此表的说明。它提供表中包含的信息的替代文本表示。

默认值为空字符串。

此属性对符合 ISO/IEC 29500 的 DOCX 文档有意义（[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)）。当保存为 ISO/IEC 29500 之前的格式时，该属性将被忽略。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 此表的说明。 |

### setHorizontalAnchor(int value) {#setHorizontalAnchor-int-}
```
public void setHorizontalAnchor(int value)
```


获取应根据其计算浮动表的水平定位的基础对象。默认值为[RelativeHorizontalPosition.COLUMN](../../com.aspose.words/relativehorizontalposition\#COLUMN).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 计算浮动表水平定位的基础对象。该值必须是其中之一[RelativeHorizontalPosition](../../com.aspose.words/relativehorizontalposition)常数。 |

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


设置要添加到单元格内容左侧的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到单元格内容左侧的空间量（以磅为单位）。 |

### setPreferredWidth(PreferredWidth value) {#setPreferredWidth-com.aspose.words.PreferredWidth-}
```
public void setPreferredWidth(PreferredWidth value)
```


设置表格的首选宽度。

默认值为[PreferredWidth.AUTO](../../com.aspose.words/preferredwidth\#AUTO).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PreferredWidth](../../com.aspose.words/preferredwidth) | 表格的首选宽度。 |

### setRelativeHorizontalAlignment(int value) {#setRelativeHorizontalAlignment-int-}
```
public void setRelativeHorizontalAlignment(int value)
```


设置浮动表格相对水平对齐方式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 浮动表相对水平对齐。该值必须是其中之一[HorizontalAlignment](../../com.aspose.words/horizontalalignment)常数。 |

### setRelativeVerticalAlignment(int value) {#setRelativeVerticalAlignment-int-}
```
public void setRelativeVerticalAlignment(int value)
```


设置浮动表格相对垂直对齐方式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 浮动表相对垂直对齐。该值必须是其中之一[VerticalAlignment](../../com.aspose.words/verticalalignment)常数。 |

### setRightPadding(double value) {#setRightPadding-double-}
```
public void setRightPadding(double value)
```


设置要添加到单元格内容右侧的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 添加到单元格内容右侧的空间量（以磅为单位）。 |

### setShading(int texture, Color foregroundColor, Color backgroundColor) {#setShading-int-java.awt.Color-java.awt.Color-}
```
public void setShading(int texture, Color foregroundColor, Color backgroundColor)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| texture | int |  |
| foregroundColor | java.awt.Color |  |
| backgroundColor | java.awt.Color |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


设置应用于此表格的表格样式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | 应用于此表格的表格样式。 |

### setStyleIdentifier(int value) {#setStyleIdentifier-int-}
```
public void setStyleIdentifier(int value)
```


设置应用于此表格的表格样式的区域设置独立样式标识符。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应用于此表的表样式的区域设置独立样式标识符。该值必须是其中之一[StyleIdentifier](../../com.aspose.words/styleidentifier)常数。 |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


设置应用于此表格的表格样式的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于此表格的表格样式的名称。 |

### setStyleOptions(int value) {#setStyleOptions-int-}
```
public void setStyleOptions(int value)
```


设置指定表格样式如何应用于此表格的位标志。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 指定表格样式如何应用于此表格的位标志。该值必须是按位组合[TableStyleOptions](../../com.aspose.words/tablestyleoptions)常数。 |

### setTextWrapping(int value) {#setTextWrapping-int-}
```
public void setTextWrapping(int value)
```


套[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-)表。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | \{[getTextWrapping()](../../com.aspose.words/table\#getTextWrapping--) / [setTextWrapping(int)](../../com.aspose.words/table\#setTextWrapping-int-)表。该值必须是其中之一[TextWrapping](../../com.aspose.words/textwrapping)常数。 |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


设置此表的标题。它提供表中包含的信息的替代文本表示。

默认值为空字符串。

此属性对符合 ISO/IEC 29500 的 DOCX 文档有意义（[OoxmlCompliance](../../com.aspose.words/ooxmlcompliance)）。当保存为 ISO/IEC 29500 之前的格式时，该属性将被忽略。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 此表的标题。 |

### setTopPadding(double value) {#setTopPadding-double-}
```
public void setTopPadding(double value)
```


设置要在单元格内容上方添加的空间量（以磅为单位）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 在单元格内容上方添加的空间量（以磅为单位）。 |

### setVerticalAnchor(int value) {#setVerticalAnchor-int-}
```
public void setVerticalAnchor(int value)
```


获取应该从中计算浮动表的垂直定位的基础对象。默认值为[RelativeVerticalPosition.MARGIN](../../com.aspose.words/relativeverticalposition\#MARGIN).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 应该从中计算浮动表的垂直定位的基础对象。该值必须是其中之一[RelativeVerticalPosition](../../com.aspose.words/relativeverticalposition)常数。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


使用指定的保存选项将节点的内容导出为字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | 指定控制节点保存方式的选项。 |

**退货：**
java.lang.String - 指定格式的节点内容。
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

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
