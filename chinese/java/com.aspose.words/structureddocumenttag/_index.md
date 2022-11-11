---
title: StructuredDocumentTag
second_title: Aspose.Words for Java API Reference
description: 表示文档中的结构化文档标签 SDT 或内容控件。
type: docs
weight: 532
url: /zh/java/com.aspose.words/structureddocumenttag/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)

**所有实现的接口:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag)
```
public class StructuredDocumentTag extends CompositeNode implements IStructuredDocumentTag
```

表示文档中的结构化文档标签（SDT 或内容控件）。

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。

结构化文档标签 (SDT) 允许将客户定义的语义及其行为和外观嵌入到文档中。

在这个版本中，Aspose.Words 提供了许多公共方法和属性来操纵行为和内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).将 SDT 节点映射到文档中的自定义 XML 包可以使用[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--)财产。

[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)可能出现在文档中的以下位置：

 *  块级 - 在段落和表格中，作为 a 的子级[Body](../../com.aspose.words/body), [HeaderFooter](../../com.aspose.words/headerfooter), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote)或一个[Shape](../../com.aspose.words/shape)节点。
 *  行级 - 在表中的行中，作为[Table](../../com.aspose.words/table)节点。
 *  单元格级别 - 在表格行中的单元格中，作为[Row](../../com.aspose.words/row)节点。
 *  Inline-level - 在里面的内联内容中，作为一个子级[Paragraph](../../com.aspose.words/paragraph).
 *  嵌套在另一个里面[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [StructuredDocumentTag(DocumentBase doc, int type, int level)](#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [clear()](#clear--) | 清除此结构化文档标记的内容并显示占位符（如果已定义）。 |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getAppearance()](#getAppearance--) | 获取/设置结构化文档标签的外观。 |
| [getBuildingBlockCategory()](#getBuildingBlockCategory--) | 为此指定构建块的类别**SDT**节点。 |
| [getBuildingBlockGallery()](#getBuildingBlockGallery--) | 为此指定构建块的类型**SDT**. |
| [getCalendar类型()](#getCalendar类型--) | 为此指定日历的类型**SDT**. |
| [getChecked()](#getChecked--) | 获取/设置复选框的当前状态**SDT**. |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取结构化文档标签的颜色。 |
| [getContainer()](#getContainer--) |  |
| [getContentsFont()](#getContentsFont--) | 将应用于输入的文本的字体格式**SDT**. |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDateDisplayFormat()](#getDateDisplayFormat--) | 表示日期显示格式的字符串。 |
| [getDateDisplayLocale()](#getDateDisplayLocale--) | 允许设置/获取在此显示的日期的语言格式**SDT**. |
| [getDateStorageFormat()](#getDateStorageFormat--) | 获取/设置日期 SDT 的日期存储格式，当**SDT**绑定到文档数据存储中的 XML 节点。 |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getEndCharacterFont()](#getEndCharacterFont--) | 将应用于输入文本的最后一个字符的字体格式**SDT**. |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFullDate()](#getFullDate--) | 指定上次输入的完整日期和时间**SDT**. |
| [getId()](#getId--) | 为此指定一个唯一的只读持久数字 ID**SDT**. |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLevel()](#getLevel--) | 获取此级别**SDT**出现在文档树中。 |
| [getLevel_IMarkupNode()](#getLevel-IMarkupNode--) |  |
| [getListItems()](#getListItems--) | 获取[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection)与此相关**SDT**. |
| [getLockContentControl()](#getLockContentControl--) | 当设置为 true 时，此属性将禁止用户删除此**SDT**. |
| [getLockContents()](#getLockContents--) | 当设置为 true 时，此属性将禁止用户编辑此内容**SDT**. |
| [getMultiline()](#getMultiline--) | 指定这是否**SDT**允许多行文本。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) | 退货**Node类型.StructuredDocumentTag**. |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getPlaceholder()](#getPlaceholder--) | 获取[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此 SDT 运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-)元素为真。 |
| [getPlaceholderName()](#getPlaceholderName--) | 获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getSdt类型()](#getSdt类型--) | 获取 this 的类型**Structured document tag**. |
| [getStyle()](#getStyle--) | 获取结构化文档标签的样式。 |
| [getStyleName()](#getStyleName--) | 获取应用于结构化文档标签的样式名称。 |
| [getTag()](#getTag--) | 指定与当前 SDT 节点关联的标签。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTitle()](#getTitle--) | 指定与此关联的友好名称**SDT**. |
| [getWordOpenXML()](#getWordOpenXML--) | 获取一个字符串，该字符串表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。 |
| [getXmlMapping()](#getXmlMapping--) | 获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据的映射。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [isRanged()](#isRanged--) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | 指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。 |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | 指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。 |
| [isTemporary()](#isTemporary--) | 指定这是否**SDT**当其内容被修改时，应从 WordProcessingML 文档中删除。 |
| [isTemporary(boolean value)](#isTemporary-boolean-) | 指定这是否**SDT**当其内容被修改时，应从 WordProcessingML 文档中删除。 |
| [iterator()](#iterator--) | 为在此节点的子节点上的每个样式迭代提供支持。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [node类型ToString(int node类型)](#node类型ToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 移除指定的子节点。 |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeSelfOnly()](#removeSelfOnly--) | 仅删除此 SDT 节点本身，但将其内容保留在文档树中。 |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setAppearance(int value)](#setAppearance-int-) | 获取/设置结构化文档标签的外观。 |
| [setBuildingBlockCategory(String value)](#setBuildingBlockCategory-java.lang.String-) | 为此指定构建块的类别**SDT**节点。 |
| [setBuildingBlockGallery(String value)](#setBuildingBlockGallery-java.lang.String-) | 为此指定构建块的类型**SDT**. |
| [setCalendar类型(int value)](#setCalendar类型-int-) | 为此指定日历的类型**SDT**. |
| [setChecked(boolean value)](#setChecked-boolean-) | 获取/设置复选框的当前状态**SDT**. |
| [setCheckedSymbol(int characterCode, String fontName)](#setCheckedSymbol-int-java.lang.String-) | 设置用于表示复选框内容控件的选中状态的符号。 |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置结构化文档标签的颜色。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setDateDisplayFormat(String value)](#setDateDisplayFormat-java.lang.String-) | 表示日期显示格式的字符串。 |
| [setDateDisplayLocale(int value)](#setDateDisplayLocale-int-) | 允许设置/获取在此显示的日期的语言格式**SDT**. |
| [setDateStorageFormat(int value)](#setDateStorageFormat-int-) | 获取/设置日期 SDT 的日期存储格式，当**SDT**绑定到文档数据存储中的 XML 节点。 |
| [setFullDate(Date value)](#setFullDate-java.util.Date-) | 指定上次输入的完整日期和时间**SDT**. |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | 当设置为 true 时，此属性将禁止用户删除此**SDT**. |
| [setLockContents(boolean value)](#setLockContents-boolean-) | 当设置为 true 时，此属性将禁止用户编辑此内容**SDT**. |
| [setMultiline(boolean value)](#setMultiline-boolean-) | 指定这是否**SDT**允许多行文本。 |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) | 获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。 |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStyle(Style value)](#setStyle-com.aspose.words.Style-) | 设置结构化文档标签的样式。 |
| [setStyleName(String value)](#setStyleName-java.lang.String-) | 设置应用于结构化文档标签的样式名称。 |
| [setTag(String value)](#setTag-java.lang.String-) | 指定与当前 SDT 节点关联的标签。 |
| [setTitle(String value)](#setTitle-java.lang.String-) | 指定与此关联的友好名称**SDT**. |
| [setUncheckedSymbol(int characterCode, String fontName)](#setUncheckedSymbol-int-java.lang.String-) | 设置用于表示复选框内容控件的未选中状态的符号。 |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### StructuredDocumentTag(DocumentBase doc, int type, int level) {#StructuredDocumentTag-com.aspose.words.DocumentBase-int-int-}
```
public StructuredDocumentTag(DocumentBase doc, int type, int level)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| type | int |  |
| level | int |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


接受访客。

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货:**
 boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。来电[DocumentVisitor.visitStructuredDocumentTagStart(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor\#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-) ，然后调用[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-)用于智能标签的所有子节点并调用[DocumentVisitor.visitStructuredDocumentTagEnd(com.aspose.words.StructuredDocumentTag)](../../com.aspose.words/documentvisitor\#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-)在最后。
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


将指定节点添加到此节点的子节点列表的末尾。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 添加的节点。
### clear() {#clear--}
```
public void clear()
```


清除此结构化文档标记的内容并显示占位符（如果已定义）。

如果结构化文档标签有修订，则无法清除它的内容。

如果此结构化文档标记映射到自定义 XML（使用[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--)属性），被引用的 XML 节点被清除。

### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True 递归克隆指定节点下的子树； false 仅克隆节点本身。 |

**退货:**
[Node](../../com.aspose.words/node) - 克隆的节点。
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
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getAncestor(int ancestor类型) {#getAncestor-int-}
```
public CompositeNode getAncestor(int ancestor类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestor类型 | int |  |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getAncestor(班级 ancestor类型) {#getAncestor-java.lang.班级-}
```
public CompositeNode getAncestor(班级 ancestor类型)
```


获取指定对象类型的第一个祖先。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| ancestor类型 | java.lang.班级 | 要检索的祖先的对象类型。 |

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 指定类型的祖先，如果没有找到该类型的祖先，则返回 null。

如果祖先类型等于祖先类型或从祖先类型派生，则祖先类型匹配。
### getAppearance() {#getAppearance--}
```
public int getAppearance()
```


获取/设置结构化文档标签的外观。

**退货:**
int - 对应的 int 值。返回值是以下之一[SdtAppearance](../../com.aspose.words/sdtappearance)常数。
### getBuildingBlockCategory() {#getBuildingBlockCategory--}
```
public String getBuildingBlockCategory()
```


为此指定构建块的类别**SDT**节点。不能为空。

访问此属性仅适用于[Sdt类型.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY)和[Sdt类型.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ)SDT 类型。它是只读的**SDT**文档部件类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getBuildingBlockGallery() {#getBuildingBlockGallery--}
```
public String getBuildingBlockGallery()
```


为此指定构建块的类型**SDT**.不能为空。

访问此属性仅适用于[Sdt类型.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY)和[Sdt类型.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ)SDT 类型。它是只读的**SDT**文档部件类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getCalendar类型() {#getCalendar类型--}
```
public int getCalendar类型()
```


为此指定日历的类型**SDT** .默认为[SdtCalendar类型.DEFAULT](../../com.aspose.words/sdtcalendartype\#DEFAULT)

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
int - 对应的 int 值。返回值是以下之一[SdtCalendar类型](../../com.aspose.words/sdtcalendartype)常数。
### getChecked() {#getChecked--}
```
public boolean getChecked()
```


获取/设置复选框的当前状态**SDT**.此属性的默认值为 false。

访问此属性仅适用于[Sdt类型.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
boolean - 对应的布尔值。
### getChild(int node类型, int index, boolean isDeep) {#getChild-int-int-boolean-}
```
public Node getChild(int node类型, int index, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |
| index | int |  |
| isDeep | boolean |  |

**退货:**
[Node](../../com.aspose.words/node)
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


获取此节点的所有直接子节点。

笔记，[getChildNodes()](../../com.aspose.words/compositenode\#getChildNodes--)相当于调用 GetChildNodes(Node类型.Any, false) 并在每次访问时创建并返回一个新集合。

如果没有子节点，则此属性返回一个空集合。

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection) - 该节点的所有直接子节点。
### getChildNodes(int node类型, boolean isDeep) {#getChildNodes-int-boolean-}
```
public NodeCollection getChildNodes(int node类型, boolean isDeep)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |
| isDeep | boolean |  |

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection)
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColor() {#getColor--}
```
public Color getColor()
```


获取结构化文档标签的颜色。

**退货:**
java.awt.Color - 结构化文档标签的颜色。
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
### getContentsFont() {#getContentsFont--}
```
public Font getContentsFont()
```


将应用于输入的文本的字体格式**SDT**.

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getCount() {#getCount--}
```
public int getCount()
```


获取此节点的直接子节点数。

**退货:**
int - 此节点的直接子节点数。
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```




**退货:**
[Node](../../com.aspose.words/node)
### getCustomNodeId() {#getCustomNodeId--}
```
public int getCustomNodeId()
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的键。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**退货:**
int - 对应的 int 值。
### getDateDisplayFormat() {#getDateDisplayFormat--}
```
public String getDateDisplayFormat()
```


表示日期显示格式的字符串。不能为空。英语（美国）的日期是“mm/dd/yyyy”

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getDateDisplayLocale() {#getDateDisplayLocale--}
```
public int getDateDisplayLocale()
```


允许设置/获取在此显示的日期的语言格式**SDT**.

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
int - 对应的 int 值。
### getDateStorageFormat() {#getDateStorageFormat--}
```
public int getDateStorageFormat()
```


获取/设置日期 SDT 的日期存储格式，当**SDT**绑定到文档数据存储中的 XML 节点。默认值为[SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat\#DATE-TIME)

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
int - 对应的 int 值。返回值是以下之一[SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat)常数。
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取该节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建但尚未添加到树中，或者已从树中删除。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getEndCharacterFont() {#getEndCharacterFont--}
```
public Font getEndCharacterFont()
```


将应用于输入文本的最后一个字符的字体格式**SDT**.

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的第一个子节点。
### getFullDate() {#getFullDate--}
```
public Date getFullDate()
```


指定上次输入的完整日期和时间**SDT**.

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
java.util.Date - 对应的 java.util.Date 值。
### getId() {#getId--}
```
public int getId()
```


为此指定一个唯一的只读持久数字 ID**SDT**.

id 属性应遵循以下规则：

 *  仅当克隆整个文档时，文档才应保留 SDT id[Document.deepClone()](../../com.aspose.words/document\#deepClone--).
 *  期间[DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-)如果导入不会与目标文档中的其他 SDT Id 发生冲突，则应保留 Id。
 *  如果多个 SDT 节点为 Id 属性指定相同的十进制数字值，则文档中的第一个 SDT 应保持此原始 Id，并且所有后续 SDT 节点应在加载文档时为其分配新的标识符。
 *  在独立 SDT 期间**M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)**操作将为克隆的 SDT 节点生成新的唯一 ID。
 *  如果源文档中未指定 Id，则 SDT 节点应在加载文档时分配一个新的唯一标识符。

**退货:**
int - 对应的 int 值。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的最后一个子节点。
### getLevel() {#getLevel--}
```
public int getLevel()
```


获取此级别**SDT**出现在文档树中。

**退货:**
 int - 这个级别**SDT**出现在文档树中。返回值是以下之一[MarkupLevel](../../com.aspose.words/markuplevel)常数。
### getLevel_IMarkupNode() {#getLevel-IMarkupNode--}
```
public int getLevel_IMarkupNode()
```




**退货:**
整数
### getListItems() {#getListItems--}
```
public SdtListItemCollection getListItems()
```


获取[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection)与此相关**SDT**.

访问此属性仅适用于[Sdt类型.COMBO\_BOX](../../com.aspose.words/sdttype\#COMBO-BOX)或者[Sdt类型.DROP\_DOWN\_LIST](../../com.aspose.words/sdttype\#DROP-DOWN-LIST) SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection) -\{[SdtListItemCollection](../../com.aspose.words/sdtlistitemcollection)与此相关**SDT**.
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


当设置为 true 时，此属性将禁止用户删除此**SDT**.

**退货:**
boolean - 对应的布尔值。
### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


当设置为 true 时，此属性将禁止用户编辑此内容**SDT**.

**退货:**
boolean - 对应的布尔值。
### getMultiline() {#getMultiline--}
```
public boolean getMultiline()
```


指定这是否**SDT**允许多行文本。

访问此属性仅适用于[Sdt类型.RICH\_TEXT](../../com.aspose.words/sdttype\#RICH-TEXT)和[Sdt类型.PLAIN\_TEXT](../../com.aspose.words/sdttype\#PLAIN-TEXT)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**退货:**
boolean - 对应的布尔值。
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node-}
```
public Node getNextMatchingNode(Node curNode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node) |  |

**退货:**
[Node](../../com.aspose.words/node)
### getNextSibling() {#getNextSibling--}
```
public Node getNextSibling()
```


获取紧跟此节点的节点。如果没有下一个节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 紧跟该节点的节点。
### getNode类型() {#getNode类型--}
```
public int getNode类型()
```


退货**Node类型.StructuredDocumentTag**.

**退货:**
诠释 -**Node类型.StructuredDocumentTag** .返回值是以下之一[Node类型](../../com.aspose.words/nodetype)常数。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父节点。

如果一个节点刚刚创建但尚未添加到树中，或者它已从树中删除，则父节点为空。

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 该节点的直接父节点。
### getPlaceholder() {#getPlaceholder--}
```
public BuildingBlock getPlaceholder()
```


获取[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此 SDT 运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-)元素为真。可以为 null，表示占位符不适用于此 Sdt。

**退货:**
[BuildingBlock](../../com.aspose.words/buildingblock) - 这[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此 SDT 运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/structureddocumenttag\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttag\#isShowingPlaceholderText-boolean-)元素为真。
### getPlaceholderName() {#getPlaceholderName--}
```
public String getPlaceholderName()
```


获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。

具有此名称的 BuildingBlock[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-)必须出现在[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-)否则会发生 java.lang.IllegalStateException。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getPreviousSibling() {#getPreviousSibling--}
```
public Node getPreviousSibling()
```


获取紧接在此节点之前的节点。如果没有前面的节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 紧接在此节点之前的节点。
### getRange() {#getRange--}
```
public Range getRange()
```


返回一个**Range**表示包含在此节点中的文档部分的对象。

**退货:**
[Range](../../com.aspose.words/range) - 一个**Range**表示包含在此节点中的文档部分的对象。
### getSdt类型() {#getSdt类型--}
```
public int getSdt类型()
```


获取 this 的类型**Structured document tag**.

**退货:**
 int - 这个的类型**Structured document tag** .返回值是以下之一[Sdt类型](../../com.aspose.words/sdttype)常数。
### getStyle() {#getStyle--}
```
public Style getStyle()
```


获取结构化文档标签的样式。仅有的[Style类型.CHARACTER](../../com.aspose.words/styletype\#CHARACTER)风格或[Style类型.PARAGRAPH](../../com.aspose.words/styletype\#PARAGRAPH)可以设置链接字符样式的样式。

**退货:**
[Style](../../com.aspose.words/style) - 结构化文档标签的样式。
### getStyleName() {#getStyleName--}
```
public String getStyleName()
```


获取应用于结构化文档标签的样式名称。

**退货:**
java.lang.String - 应用于结构化文档标签的样式名称。
### getTag() {#getTag--}
```
public String getTag()
```


指定与当前 SDT 节点关联的标签。不能为空。标记是应用程序可以与 SDT 关联的任意字符串，以便在不提供可见友好名称的情况下识别它。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货:**
java.lang.String
### getTitle() {#getTitle--}
```
public String getTitle()
```


指定与此关联的友好名称**SDT**.不能为空。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getWordOpenXML() {#getWordOpenXML--}
```
public String getWordOpenXML()
```


获取一个字符串，该字符串表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。

**退货:**
 java.lang.String - 一个字符串，表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。
### getXmlMapping() {#getXmlMapping--}
```
public XmlMapping getXmlMapping()
```


获取一个对象，该对象表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据的映射。您可以使用[XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-)此对象的方法将结构化文档标记映射到 XML 数据。

**退货:**
[XmlMapping](../../com.aspose.words/xmlmapping) - 表示此结构化文档标记到当前文档的自定义 XML 部分中的 XML 数据的映射的对象。
### hasChildNodes() {#hasChildNodes--}
```
public boolean hasChildNodes()
```


如果此节点有任何子节点，则返回 true。

**退货:**
boolean - 如果此节点有任何子节点，则为真。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### indexOf(Node child) {#indexOf-com.aspose.words.Node-}
```
public int indexOf(Node child)
```


返回子节点数组中指定子节点的索引。如果在子节点中未找到该节点，则返回 -1。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node) |  |

**退货:**
整数
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertAfter(Node newChild, Node refChild)
```


在指定的参考节点之后立即插入指定的节点。

如果 refChild 为 null，则在子节点列表的开头插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newNode 放在 refNode 之后。 |

**退货:**
[Node](../../com.aspose.words/node) - 插入的节点。
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node-}
```
public Node insertBefore(Node newChild, Node refChild)
```


在指定的参考节点之前插入指定的节点。

如果 refChild 为 null，则在子节点列表的末尾插入 newChild。

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要插入的节点。 |
| refChild | [Node](../../com.aspose.words/node) | 作为参考节点的节点。 newChild 放置在此节点之前。 |

**退货:**
[Node](../../com.aspose.words/node) - 插入的节点。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货:**
boolean - True 因为这个节点可以有子节点。
### isRanged() {#isRanged--}
```
public boolean isRanged()
```


如果此实例是范围结构化文档标记，则返回 true。

**退货:**
布尔值
### isShowingPlaceholderText() {#isShowingPlaceholderText--}
```
public boolean isShowingPlaceholderText()
```


指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

**退货:**
boolean - 对应的布尔值。
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public void isShowingPlaceholderText(boolean value)
```


指定此内容是否**SDT**应被解释为包含占位符文本（与 SDT 中的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### isTemporary() {#isTemporary--}
```
public boolean isTemporary()
```


指定这是否**SDT**当其内容被修改时，应从 WordProcessingML 文档中删除。

**退货:**
boolean - 对应的布尔值。
### isTemporary(boolean value) {#isTemporary-boolean-}
```
public void isTemporary(boolean value)
```


指定这是否**SDT**当其内容被修改时，应从 WordProcessingML 文档中删除。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### iterator() {#iterator--}
```
public Iterator iterator()
```


为在此节点的子节点上的每个样式迭代提供支持。

**退货:**
java.util.Iterator
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node-}
```
public Node nextPreOrder(Node rootNode)
```


根据前序树遍历算法获取下一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶部节点（极限）。 |

**退货:**
[Node](../../com.aspose.words/node) - 预购订单中的下一个节点。如果到达 rootNode，则为 Null。
### node类型ToString(int node类型) {#node类型ToString-int-}
```
public static String node类型ToString(int node类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| node类型 | int |  |

**退货:**
java.lang.String
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

如果 newChild 已经在树中，则首先将其移除。

如果要插入的节点是从另一个文档创建的，您应该使用**M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)**将节点导入当前文档。然后可以将导入的节点插入到当前文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node) | 要添加的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 添加的节点。
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node-}
```
public Node previousPreOrder(Node rootNode)
```


根据前序树遍历算法获取上一个节点。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node) | 遍历的顶部节点（极限）。 |

**退货:**
[Node](../../com.aspose.words/node) - 预购订单中的上一个节点。如果到达 rootNode，则为 Null。
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


移除指定的子节点。

删除节点后，oldChild 的父级设置为 null。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node) | 要移除的节点。 |

**退货:**
[Node](../../com.aspose.words/node) - 删除的节点。
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeSelfOnly() {#removeSelfOnly--}
```
public void removeSelfOnly()
```


仅删除此 SDT 节点本身，但将其内容保留在文档树中。

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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货:**
[NodeList](../../com.aspose.words/nodelist) - 与 XPath 查询匹配的节点列表。
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String-}
```
public Node selectSingleNode(String xpath)
```


选择与 XPath 表达式匹配的第一个节点。

目前仅支持带有元素名称的表达式。不支持使用属性名称的表达式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| xpath | java.lang.String | XPath 表达式。 |

**退货:**
[Node](../../com.aspose.words/node) - 与 XPath 查询匹配的第一个节点，如果未找到匹配节点，则为 null。
### setAppearance(int value) {#setAppearance-int-}
```
public void setAppearance(int value)
```


获取/设置结构化文档标签的外观。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[SdtAppearance](../../com.aspose.words/sdtappearance)常数。 |

### setBuildingBlockCategory(String value) {#setBuildingBlockCategory-java.lang.String-}
```
public void setBuildingBlockCategory(String value)
```


为此指定构建块的类别**SDT**节点。不能为空。

访问此属性仅适用于[Sdt类型.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY)和[Sdt类型.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ)SDT 类型。它是只读的**SDT**文档部件类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setBuildingBlockGallery(String value) {#setBuildingBlockGallery-java.lang.String-}
```
public void setBuildingBlockGallery(String value)
```


为此指定构建块的类型**SDT**.不能为空。

访问此属性仅适用于[Sdt类型.BUILDING\_BLOCK\_GALLERY](../../com.aspose.words/sdttype\#BUILDING-BLOCK-GALLERY)和[Sdt类型.DOC\_PART\_OBJ](../../com.aspose.words/sdttype\#DOC-PART-OBJ)SDT 类型。它是只读的**SDT**文档部件类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setCalendar类型(int value) {#setCalendar类型-int-}
```
public void setCalendar类型(int value)
```


为此指定日历的类型**SDT** .默认为[SdtCalendar类型.DEFAULT](../../com.aspose.words/sdtcalendartype\#DEFAULT)

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[SdtCalendar类型](../../com.aspose.words/sdtcalendartype)常数。 |

### setChecked(boolean value) {#setChecked-boolean-}
```
public void setChecked(boolean value)
```


获取/设置复选框的当前状态**SDT**.此属性的默认值为 false。

访问此属性仅适用于[Sdt类型.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCheckedSymbol(int characterCode, String fontName) {#setCheckedSymbol-int-java.lang.String-}
```
public void setCheckedSymbol(int characterCode, String fontName)
```


设置用于表示复选框内容控件的选中状态的符号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| characterCode | int | 指定符号的字符代码。 |
| fontName | java.lang.String | 包含符号的字体的名称。

访问此方法仅适用于[Sdt类型.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT 类型。

对于所有其他 SDT 类型，将发生异常。|

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


设置结构化文档标签的颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 结构化文档标签的颜色。 |

### setCustomNodeId(int value) {#setCustomNodeId-int-}
```
public void setCustomNodeId(int value)
```


指定自定义节点标识符。

默认为零。

这个标识符可以任意设置和使用。例如，作为获取外部数据的键。

重要说明，指定的值不会保存到输出文件中，并且仅在节点生命周期内存在。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setDateDisplayFormat(String value) {#setDateDisplayFormat-java.lang.String-}
```
public void setDateDisplayFormat(String value)
```


表示日期显示格式的字符串。不能为空。英语（美国）的日期是“mm/dd/yyyy”

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setDateDisplayLocale(int value) {#setDateDisplayLocale-int-}
```
public void setDateDisplayLocale(int value)
```


允许设置/获取在此显示的日期的语言格式**SDT**.

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setDateStorageFormat(int value) {#setDateStorageFormat-int-}
```
public void setDateStorageFormat(int value)
```


获取/设置日期 SDT 的日期存储格式，当**SDT**绑定到文档数据存储中的 XML 节点。默认值为[SdtDateStorageFormat.DATE\_TIME](../../com.aspose.words/sdtdatestorageformat\#DATE-TIME)

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[SdtDateStorageFormat](../../com.aspose.words/sdtdatestorageformat)常数。 |

### setFullDate(Date value) {#setFullDate-java.util.Date-}
```
public void setFullDate(Date value)
```


指定上次输入的完整日期和时间**SDT**.

访问此属性仅适用于[Sdt类型.DATE](../../com.aspose.words/sdttype\#DATE)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 对应的 java.util.Date 值。 |

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


当设置为 true 时，此属性将禁止用户删除此**SDT**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


当设置为 true 时，此属性将禁止用户编辑此内容**SDT**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setMultiline(boolean value) {#setMultiline-boolean-}
```
public void setMultiline(boolean value)
```


指定这是否**SDT**允许多行文本。

访问此属性仅适用于[Sdt类型.RICH\_TEXT](../../com.aspose.words/sdttype\#RICH-TEXT)和[Sdt类型.PLAIN\_TEXT](../../com.aspose.words/sdttype\#PLAIN-TEXT)SDT 类型。

对于所有其他 SDT 类型，将发生异常。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPlaceholderName(String value) {#setPlaceholderName-java.lang.String-}
```
public void setPlaceholderName(String value)
```


获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。

具有此名称的 BuildingBlock[BuildingBlock.getName()](../../com.aspose.words/buildingblock\#getName--) / [BuildingBlock.setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-)必须出现在[Document.getGlossaryDocument()](../../com.aspose.words/document\#getGlossaryDocument--) / [Document.setGlossaryDocument(com.aspose.words.GlossaryDocument)](../../com.aspose.words/document\#setGlossaryDocument-com.aspose.words.GlossaryDocument-)否则会发生 java.lang.IllegalStateException。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStyle(Style value) {#setStyle-com.aspose.words.Style-}
```
public void setStyle(Style value)
```


设置结构化文档标签的样式。仅有的[Style类型.CHARACTER](../../com.aspose.words/styletype\#CHARACTER)风格或[Style类型.PARAGRAPH](../../com.aspose.words/styletype\#PARAGRAPH)可以设置链接字符样式的样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | 结构化文档标签的样式。 |

### setStyleName(String value) {#setStyleName-java.lang.String-}
```
public void setStyleName(String value)
```


设置应用于结构化文档标签的样式名称。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于结构化文档标签的样式名称。 |

### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


指定与当前 SDT 节点关联的标签。不能为空。标记是应用程序可以与 SDT 关联的任意字符串，以便在不提供可见友好名称的情况下识别它。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


指定与此关联的友好名称**SDT**.不能为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setUncheckedSymbol(int characterCode, String fontName) {#setUncheckedSymbol-int-java.lang.String-}
```
public void setUncheckedSymbol(int characterCode, String fontName)
```


设置用于表示复选框内容控件的未选中状态的符号。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| characterCode | int | 指定符号的字符代码。 |
| fontName | java.lang.String | 包含符号的字体的名称。

访问此方法仅适用于[Sdt类型.CHECKBOX](../../com.aspose.words/sdttype\#CHECKBOX) SDT 类型。

对于所有其他 SDT 类型，将发生异常。|

### structuredDocumentTagNode() {#structuredDocumentTagNode--}
```
public Node structuredDocumentTagNode()
```


返回实现此接口的 Node 对象。

**退货:**
[Node](../../com.aspose.words/node)
### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions-}
```
public String toString(SaveOptions saveOptions)
```


使用指定的保存选项将节点的内容导出为字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | 指定控制节点保存方式的选项。 |

**退货:**
java.lang.String - 指定格式的节点内容。
### toString(int saveFormat) {#toString-int-}
```
public String toString(int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

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
