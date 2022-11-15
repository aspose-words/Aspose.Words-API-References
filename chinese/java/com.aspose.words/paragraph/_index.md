---
title: Paragraph
second_title: Aspose.Words for Java API 参考
description: 代表一段文字。
type: docs
weight: 443
url: /zh/java/com.aspose.words/paragraph/
---

**遗产：**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Paragraph extends CompositeNode
```

代表一段文字。

要了解更多信息，请访问**Working with Paragraphs**文档文章。

[Paragraph](../../com.aspose.words/paragraph)是块级节点，可以是派生自的类的子节点[Story](../../com.aspose.words/story)或者[InlineStory](../../com.aspose.words/inlinestory).

[Paragraph](../../com.aspose.words/paragraph)可以包含任意数量的内联级节点和书签。

段落中可能出现的子节点的完整列表包括[BookmarkStart](../../com.aspose.words/bookmarkstart), [BookmarkEnd](../../com.aspose.words/bookmarkend), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote), [Run](../../com.aspose.words/run), [SpecialChar](../../com.aspose.words/specialchar), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [SmartTag](../../com.aspose.words/smarttag).

Microsoft Word 中的有效段落始终以段落分隔符结尾，最小有效段落仅由段落分隔符组成。这**Paragraph**类自动在末尾附加适当的段落分隔符，并且该字符不是子节点的一部分**Paragraph** 因此**Paragraph**可以为空。

不包含段落结尾[ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK)或单元格结尾[ControlChar.CELL](../../com.aspose.words/controlchar\#CELL)段落文本中的字符，因为在 Microsoft Word 中打开文档时，这可能会使段落无效。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [Paragraph(DocumentBase doc)](#Paragraph-com.aspose.words.DocumentBase-) | 初始化一个新的实例**Paragraph**班级。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接待来访者。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [appendField(int fieldType, boolean updateField)](#appendField-int-boolean-) |  |
| [appendField(String fieldCode)](#appendField-java.lang.String-) | 将 Word 字段附加到此段落。 |
| [appendField(String fieldCode, String fieldValue)](#appendField-java.lang.String-java.lang.String-) | 将 Word 字段附加到此段落。 |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | 获取指定对象类型的第一个祖先。 |
| [getBreakIsStyleSeparator()](#getBreakIsStyleSeparator--) | 如果此段落分隔符是样式分隔符，则为真。 |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取此节点所属的文档。 |
| [getEffectiveTabStops()](#getEffectiveTabStops--) | 返回应用于此段落的所有制表位的数组，包括由样式或列表间接应用的。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFrameFormat()](#getFrameFormat--) | 提供对段落格式属性的访问。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getListFormat()](#getListFormat--) | 提供对段落的列表格式属性的访问。 |
| [getListLabel()](#getListLabel--) | 得到一个[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)提供对本段列表编号值和格式的访问的对象。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟在该节点之后的节点。 |
| [getNodeType()](#getNodeType--) | 退货**NodeType.Paragraph**. |
| [getParagraphBreakFont()](#getParagraphBreakFont--) | 提供对段落分隔符的字体格式的访问。 |
| [getParagraphFormat()](#getParagraphFormat--) | 提供对段落格式属性的访问。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父级。 |
| [getParentSection()](#getParentSection--) | 检索父级[Section](../../com.aspose.words/section)的段落。 |
| [getParentStory()](#getParentStory--) | 检索父节级别的故事，可以是[Body](../../com.aspose.words/body)或者[HeaderFooter](../../com.aspose.words/headerfooter). |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在该节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在该节点中的文档部分的对象。 |
| [getRuns()](#getRuns--) | 提供对段落内文本片段的类型化集合的访问。 |
| [getText()](#getText--) | 获取此段落的文本，包括段落结束字符。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的引用节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 将指定节点插入到紧靠指定引用节点之前。 |
| [insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)](#insertField-int-boolean-com.aspose.words.Node-boolean-) |  |
| [insertField(String fieldCode, Node refNode, boolean isAfter)](#insertField-java.lang.String-com.aspose.words.Node-boolean-) | 在此段落中插入一个 Word 域。 |
| [insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)](#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-) | 在此段落中插入一个 Word 域。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。 |
| [isEndOfCell()](#isEndOfCell--) | 如果这段是最后一段则为真[Cell](../../com.aspose.words/cell);否则为假。 |
| [isEndOfDocument()](#isEndOfDocument--) | 如果此段是文档最后一节的最后一段，则为真。 |
| [isEndOfHeaderFooter()](#isEndOfHeaderFooter--) | 如果该段是该段中的最后一段，则为真**HeaderFooter**（正文故事）一个**Section**;否则为假。 |
| [isEndOfSection()](#isEndOfSection--) | 如果该段是该段中的最后一段，则为真**Body**（正文故事）一个**Section**;否则为假。 |
| [isFormatRevision()](#isFormatRevision--) | 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [isInCell()](#isInCell--) | 如果此段落是的直接子项，则为真[Cell](../../com.aspose.words/cell);否则为假。 |
| [isInsertRevision()](#isInsertRevision--) | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [isListItem()](#isListItem--) | 当段落是原始修订版中的项目符号列表或编号列表中的项目时为真。 |
| [isMoveFromRevision()](#isMoveFromRevision--) | 退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [isMoveToRevision()](#isMoveToRevision--) | 退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [iterator()](#iterator--) | 为该节点的子节点上的每个样式迭代提供支持。 |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | 加入段落中具有相同格式的运行。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的开头。 |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeAllChildren()](#removeAllChildren--) | 移除当前节点的所有子节点。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 删除指定的子节点。 |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Paragraph(DocumentBase doc) {#Paragraph-com.aspose.words.DocumentBase-}
```
public Paragraph(DocumentBase doc)
```


初始化一个新的实例**Paragraph**班级。

什么时候**Paragraph**已创建，它属于指定文档，但还不是文档的一部分，并且**ParentNode**一片空白。

追加**Paragraph**到文档，在要插入段落的故事上使用 InsertAfter 或 InsertBefore。

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
boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。调用 DocumentVisitor.VisitParagraphStart，然后为段落的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitParagraphEnd。
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
### appendField(int fieldType, boolean updateField) {#appendField-int-boolean-}
```
public Field appendField(int fieldType, boolean updateField)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**退货：**
[Field](../../com.aspose.words/field)
### appendField(String fieldCode) {#appendField-java.lang.String-}
```
public Field appendField(String fieldCode)
```


将 Word 字段附加到此段落。向该段落附加一个字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要追加的字段代码（不带花括号）。 |

**退货：**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示附加字段的对象。
### appendField(String fieldCode, String fieldValue) {#appendField-java.lang.String-java.lang.String-}
```
public Field appendField(String fieldCode, String fieldValue)
```


将 Word 字段附加到此段落。向该段落附加一个字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要追加的字段代码（不带花括号）。 |
| fieldValue | java.lang.String | 要附加的字段值。为没有值的字段传递 null。 |

**退货：**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示附加字段的对象。
### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




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

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| isCloneChildren | boolean | True 递归克隆指定节点下的子树； false 仅克隆节点本身。 |

**退货：**
[Node](../../com.aspose.words/node) - 克隆节点。
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
### getBreakIsStyleSeparator() {#getBreakIsStyleSeparator--}
```
public boolean getBreakIsStyleSeparator()
```


如果此段落分隔符是样式分隔符，则为真。样式分隔符允许一个段落由具有不同段落样式的部分组成。

**退货：**
boolean - 相应的布尔值。
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


获取此节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建并且尚未添加到树中，或者如果它已从树中删除也是如此。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getEffectiveTabStops() {#getEffectiveTabStops--}
```
public TabStop[] getEffectiveTabStops()
```


返回应用于此段落的所有制表位的数组，包括由样式或列表间接应用的。

**退货：**
com.aspose.words.TabStop[]
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的第一个孩子。
### getFrameFormat() {#getFrameFormat--}
```
public FrameFormat getFrameFormat()
```


提供对段落格式属性的访问。

**退货：**
[FrameFormat](../../com.aspose.words/frameformat) - 相应的[FrameFormat](../../com.aspose.words/frameformat)价值。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的最后一个孩子。
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


提供对段落的列表格式属性的访问。

**退货：**
[ListFormat](../../com.aspose.words/listformat) - 相应的[ListFormat](../../com.aspose.words/listformat)价值。
### getListLabel() {#getListLabel--}
```
public ListLabel getListLabel()
```


得到一个[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)提供对本段列表编号值和格式的访问的对象。

**退货：**
[ListLabel](../../com.aspose.words/listlabel) - 一个[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)提供对本段列表编号值和格式的访问的对象。
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


退货**NodeType.Paragraph**.

**退货：**
整数 -**NodeType.Paragraph** .返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getParagraphBreakFont() {#getParagraphBreakFont--}
```
public Font getParagraphBreakFont()
```


提供对段落分隔符的字体格式的访问。

**退货：**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


提供对段落格式属性的访问。

**退货：**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 相应的[ParagraphFormat](../../com.aspose.words/paragraphformat)价值。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父级。

如果一个节点刚刚被创建并且还没有被添加到树中，或者如果它已经被从树中移除，则父节点为空。

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 此节点的直接父节点。
### getParentSection() {#getParentSection--}
```
public Section getParentSection()
```


检索父级[Section](../../com.aspose.words/section)的段落。

**退货：**
[Section](../../com.aspose.words/section) - 相应的[Section](../../com.aspose.words/section)价值。
### getParentStory() {#getParentStory--}
```
public Story getParentStory()
```


检索父节级别的故事，可以是[Body](../../com.aspose.words/body)或者[HeaderFooter](../../com.aspose.words/headerfooter).

**退货：**
[Story](../../com.aspose.words/story) - 相应的[Story](../../com.aspose.words/story)价值。
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
### getRuns() {#getRuns--}
```
public RunCollection getRuns()
```


提供对段落内文本片段的类型化集合的访问。

**退货：**
[RunCollection](../../com.aspose.words/runcollection) - 相应的[RunCollection](../../com.aspose.words/runcollection)价值。
### getText() {#getText--}
```
public String getText()
```


获取此段落的文本，包括段落结束字符。

连接所有子节点的文本并附加段落字符的结尾，如下所示：

 *  如果该段是最后一段[Body](../../com.aspose.words/body)， 然后[ControlChar.SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK)(\\x000c) 被附加。
 *  如果该段是最后一段[Cell](../../com.aspose.words/cell)， 然后[ControlChar.CELL](../../com.aspose.words/controlchar\#CELL)(\\x0007) 被附加。
 *  对于所有其他段落[ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK)(\\r) 被附加。

返回的字符串包括所有控制字符和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货：**
java.lang.字符串
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
### insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter) {#insertField-int-boolean-com.aspose.words.Node-boolean-}
```
public Field insertField(int fieldType, boolean updateField, Node refNode, boolean isAfter)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |
| refNode | [Node](../../com.aspose.words/node) |  |
| isAfter | boolean |  |

**退货：**
[Field](../../com.aspose.words/field)
### insertField(String fieldCode, Node refNode, boolean isAfter) {#insertField-java.lang.String-com.aspose.words.Node-boolean-}
```
public Field insertField(String fieldCode, Node refNode, boolean isAfter)
```


在此段落中插入一个 Word 域。在此段落中插入一个字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要插入的域代码（不带花括号）。 |
| refNode | [Node](../../com.aspose.words/node) | 此段落内的引用节点（如果 refNode 为空，则附加到段落的末尾）。 |
| isAfter | boolean | 是在引用节点之后还是之前插入字段。 |

**退货：**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示插入字段的对象。
### insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter) {#insertField-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-}
```
public Field insertField(String fieldCode, String fieldValue, Node refNode, boolean isAfter)
```


在此段落中插入一个 Word 域。在此段落中插入一个字段。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要插入的域代码（不带花括号）。 |
| fieldValue | java.lang.String | 要插入的字段值。为没有值的字段传递 null。 |
| refNode | [Node](../../com.aspose.words/node) | 此段落内的引用节点（如果 refNode 为空，则附加到段落的末尾）。 |
| isAfter | boolean | 是在引用节点之后还是之前插入字段。 |

**退货：**
[Field](../../com.aspose.words/field) - 一个[Field](../../com.aspose.words/field)表示插入字段的对象。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货：**
boolean - True 因为这个节点可以有子节点。
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则为 True。
### isEndOfCell() {#isEndOfCell--}
```
public boolean isEndOfCell()
```


如果这段是最后一段则为真[Cell](../../com.aspose.words/cell);否则为假。

**退货：**
boolean - 相应的布尔值。
### isEndOfDocument() {#isEndOfDocument--}
```
public boolean isEndOfDocument()
```


如果此段是文档最后一节的最后一段，则为真。

**退货：**
boolean - 相应的布尔值。
### isEndOfHeaderFooter() {#isEndOfHeaderFooter--}
```
public boolean isEndOfHeaderFooter()
```


如果该段是该段中的最后一段，则为真**HeaderFooter**（正文故事）一个**Section**;否则为假。

**退货：**
boolean - 相应的布尔值。
### isEndOfSection() {#isEndOfSection--}
```
public boolean isEndOfSection()
```


如果该段是该段中的最后一段，则为真**Body**（正文故事）一个**Section**;否则为假。

**退货：**
boolean - 相应的布尔值。
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则为 True。
### isInCell() {#isInCell--}
```
public boolean isInCell()
```


如果此段落是的直接子项，则为真[Cell](../../com.aspose.words/cell);否则为假。

**退货：**
boolean - 相应的布尔值。
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则为 True。
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


当段落是原始修订版中的项目符号列表或编号列表中的项目时为真。

**退货：**
boolean - 相应的布尔值。
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。

**退货：**
布尔值 -**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。

**退货：**
布尔值 -**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。
### iterator() {#iterator--}
```
public Iterator iterator()
```


为该节点的子节点上的每个样式迭代提供支持。

**退货：**
java.util.迭代器
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


加入段落中具有相同格式的运行。

**退货：**
 int - 执行的连接数。什么时候**N**相邻的运行正在被加入，它们算作**N - 1**加入。
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
### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




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

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
