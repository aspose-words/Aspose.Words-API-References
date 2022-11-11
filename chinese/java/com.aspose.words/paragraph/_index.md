---
title: Paragraph
second_title: Aspose.Words for Java API 参考
description:代表一段文字。
type: docs
weight: 443
url: /zh/java/com.aspose.words/paragraph/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class Paragraph extends CompositeNode
```

代表一段文字。

要了解更多信息，请访问**Working with Paragraphs**文档文章。

[Paragraph](../../com.aspose.words/paragraph)是块级节点，可以是派生自的类的子节点[Story](../../com.aspose.words/story)或者[InlineStory](../../com.aspose.words/inlinestory).

[Paragraph](../../com.aspose.words/paragraph)可以包含任意数量的内联级节点和书签。

段落中可能出现的子节点的完整列表包括[BookmarkStart](../../com.aspose.words/bookmarkstart), [BookmarkEnd](../../com.aspose.words/bookmarkend), [字段Start](../../com.aspose.words/fieldstart), [字段Separator](../../com.aspose.words/fieldseparator), [字段End](../../com.aspose.words/fieldend), [Form字段](../../com.aspose.words/formfield), [Comment](../../com.aspose.words/comment), [Footnote](../../com.aspose.words/footnote), [Run](../../com.aspose.words/run), [SpecialChar](../../com.aspose.words/specialchar), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [SmartTag](../../com.aspose.words/smarttag).

Microsoft Word 中的有效段落始终以段落分隔符结尾，最小有效段落仅包含段落分隔符。这**Paragraph**类自动在末尾附加适当的分节符，并且该字符不是子节点的一部分**Paragraph**，因此一个**Paragraph**可以为空。

不包括段落结尾[ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK)或单元格结尾[ControlChar.CELL](../../com.aspose.words/controlchar\#CELL)段落文本中的字符，因为在 Microsoft Word 中打开文档时，这可能会使段落无效。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [Paragraph(DocumentBase doc)](#Paragraph-com.aspose.words.DocumentBase-) | 初始化一个新的实例**Paragraph**班级。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [append字段(int field类型, boolean update字段)](#append字段-int-boolean-) |  |
| [append字段(String fieldCode)](#append字段-java.lang.String-) | 将 Word 字段附加到此段落。 |
| [append字段(String fieldCode, String fieldValue)](#append字段-java.lang.String-java.lang.String-) | 将 Word 字段附加到此段落。 |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getBreakIsStyleSeparator()](#getBreakIsStyleSeparator--) | 如果此段落分隔符是样式分隔符，则为真。 |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getEffectiveTabStops()](#getEffectiveTabStops--) | 返回应用于此段落的所有制表位的数组，包括由样式或列表间接应用的。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFrameFormat()](#getFrameFormat--) | 提供对段落格式属性的访问。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getListFormat()](#getListFormat--) | 提供对段落的列表格式属性的访问。 |
| [getListLabel()](#getListLabel--) | 得到一个[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)提供对该段落的列表编号值和格式的访问的对象。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) | 退货**Node类型.Paragraph**. |
| [getParagraphBreakFont()](#getParagraphBreakFont--) | 提供对分段符的字体格式的访问。 |
| [getParagraphFormat()](#getParagraphFormat--) | 提供对段落格式属性的访问。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getParentSection()](#getParentSection--) | 检索父级[Section](../../com.aspose.words/section)该段的。 |
| [getParentStory()](#getParentStory--) | 检索可以是的父节级故事[Body](../../com.aspose.words/body)或者[HeaderFooter](../../com.aspose.words/headerfooter). |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getRuns()](#getRuns--) | 提供对段落内文本片段的类型化集合的访问。 |
| [getText()](#getText--) | 获取此段落的文本，包括段落结尾字符。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
| [insert字段(int field类型, boolean update字段, Node refNode, boolean isAfter)](#insert字段-int-boolean-com.aspose.words.Node-boolean-) |  |
| [insert字段(String fieldCode, Node refNode, boolean isAfter)](#insert字段-java.lang.String-com.aspose.words.Node-boolean-) | 在此段落中插入一个 Word 字段。 |
| [insert字段(String fieldCode, String fieldValue, Node refNode, boolean isAfter)](#insert字段-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-) | 在此段落中插入一个 Word 字段。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [isEndOfCell()](#isEndOfCell--) | 如果本段是最后一段，则为真[Cell](../../com.aspose.words/cell);否则为假。 |
| [isEndOfDocument()](#isEndOfDocument--) | 如果此段落是文档最后一节中的最后一段，则为真。 |
| [isEndOfHeaderFooter()](#isEndOfHeaderFooter--) | 如果本段是最后一段，则为真**HeaderFooter**（正文故事）**Section**;否则为假。 |
| [isEndOfSection()](#isEndOfSection--) | 如果本段是最后一段，则为真**Body**（正文故事）**Section**;否则为假。 |
| [isFormatRevision()](#isFormatRevision--) | 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [isInCell()](#isInCell--) | 如果此段落是直接子级，则为真[Cell](../../com.aspose.words/cell);否则为假。 |
| [isInsertRevision()](#isInsertRevision--) | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [isListItem()](#isListItem--) | 当段落是原始修订中的项目符号或编号列表中的项目时为真。 |
| [isMoveFromRevision()](#isMoveFromRevision--) | 退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [isMoveToRevision()](#isMoveToRevision--) | 退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [iterator()](#iterator--) | 为在此节点的子节点上的每个样式迭代提供支持。 |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | 连接在段落中以相同的格式运行。 |
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

什么时候**Paragraph**已创建，它属于指定的文档，但还不是文档的一部分，并且**ParentNode**一片空白。

追加**Paragraph**在要插入段落的故事上使用 InsertAfter 或 InsertBefore 到文档中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | 所有者文件。 |

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
boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。调用 DocumentVisitor.VisitParagraphStart，然后为段落的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitParagraphEnd。
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
### append字段(int field类型, boolean update字段) {#append字段-int-boolean-}
```
public 字段 append字段(int field类型, boolean update字段)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field类型 | int |  |
| update字段 | boolean |  |

**退货:**
[字段](../../com.aspose.words/field)
### append字段(String fieldCode) {#append字段-java.lang.String-}
```
public 字段 append字段(String fieldCode)
```


将 Word 字段附加到此段落。将一个字段附加到此段落。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要附加的域代码（不带花括号）。 |

**退货:**
[字段](../../com.aspose.words/field) - 一个[字段](../../com.aspose.words/field)表示附加字段的对象。
### append字段(String fieldCode, String fieldValue) {#append字段-java.lang.String-java.lang.String-}
```
public 字段 append字段(String fieldCode, String fieldValue)
```


将 Word 字段附加到此段落。将一个字段附加到此段落。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要附加的域代码（不带花括号）。 |
| fieldValue | java.lang.String | 要附加的字段值。为没有值的字段传递 null。 |

**退货:**
[字段](../../com.aspose.words/field) - 一个[字段](../../com.aspose.words/field)表示附加字段的对象。
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
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
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
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
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
### getBreakIsStyleSeparator() {#getBreakIsStyleSeparator--}
```
public boolean getBreakIsStyleSeparator()
```


如果此段落分隔符是样式分隔符，则为真。样式分隔符允许一个段落由具有不同段落样式的部分组成。

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
### getContainer() {#getContainer--}
```
public CompositeNode getContainer()
```




**退货:**
[CompositeNode](../../com.aspose.words/compositenode)
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
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

**退货:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**退货:**
java.lang.Object
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
### getEffectiveTabStops() {#getEffectiveTabStops--}
```
public TabStop[] getEffectiveTabStops()
```


返回应用于此段落的所有制表位的数组，包括由样式或列表间接应用的。

**退货:**
com.aspose.words.TabStop[]
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的第一个子节点。
### getFrameFormat() {#getFrameFormat--}
```
public FrameFormat getFrameFormat()
```


提供对段落格式属性的访问。

**退货:**
[FrameFormat](../../com.aspose.words/frameformat) - 相应的[FrameFormat](../../com.aspose.words/frameformat)价值。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的最后一个子节点。
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


提供对段落的列表格式属性的访问。

**退货:**
[ListFormat](../../com.aspose.words/listformat) - 相应的[ListFormat](../../com.aspose.words/listformat)价值。
### getListLabel() {#getListLabel--}
```
public ListLabel getListLabel()
```


得到一个[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)提供对该段落的列表编号值和格式的访问的对象。

**退货:**
[ListLabel](../../com.aspose.words/listlabel) - 一个[getListLabel()](../../com.aspose.words/paragraph\#getListLabel--)提供对该段落的列表编号值和格式的访问的对象。
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


退货**Node类型.Paragraph**.

**退货:**
诠释 -**Node类型.Paragraph** .返回值是以下之一[Node类型](../../com.aspose.words/nodetype)常数。
### getParagraphBreakFont() {#getParagraphBreakFont--}
```
public Font getParagraphBreakFont()
```


提供对分段符的字体格式的访问。

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


提供对段落格式属性的访问。

**退货:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 相应的[ParagraphFormat](../../com.aspose.words/paragraphformat)价值。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父节点。

如果一个节点刚刚创建但尚未添加到树中，或者它已从树中删除，则父节点为空。

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 该节点的直接父节点。
### getParentSection() {#getParentSection--}
```
public Section getParentSection()
```


检索父级[Section](../../com.aspose.words/section)该段的。

**退货:**
[Section](../../com.aspose.words/section) - 相应的[Section](../../com.aspose.words/section)价值。
### getParentStory() {#getParentStory--}
```
public Story getParentStory()
```


检索可以是的父节级故事[Body](../../com.aspose.words/body)或者[HeaderFooter](../../com.aspose.words/headerfooter).

**退货:**
[Story](../../com.aspose.words/story) - 相应的[Story](../../com.aspose.words/story)价值。
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
### getRuns() {#getRuns--}
```
public RunCollection getRuns()
```


提供对段落内文本片段的类型化集合的访问。

**退货:**
[RunCollection](../../com.aspose.words/runcollection) - 相应的[RunCollection](../../com.aspose.words/runcollection)价值。
### getText() {#getText--}
```
public String getText()
```


获取此段落的文本，包括段落结尾字符。

连接所有子节点的文本，并附加段落结尾字符，如下所示：

 *  如果段落是最后一段[Body](../../com.aspose.words/body)， 然后[ControlChar.SECTION\_BREAK](../../com.aspose.words/controlchar\#SECTION-BREAK)(\\x000c) 被附加。
 *  如果段落是最后一段[Cell](../../com.aspose.words/cell)， 然后[ControlChar.CELL](../../com.aspose.words/controlchar\#CELL)(\\x0007) 被附加。
 *  对于所有其他段落[ControlChar.PARAGRAPH\_BREAK](../../com.aspose.words/controlchar\#PARAGRAPH-BREAK)(\\r) 被附加。

返回的字符串包括所有控制和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货:**
java.lang.String
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
### insert字段(int field类型, boolean update字段, Node refNode, boolean isAfter) {#insert字段-int-boolean-com.aspose.words.Node-boolean-}
```
public 字段 insert字段(int field类型, boolean update字段, Node refNode, boolean isAfter)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| field类型 | int |  |
| update字段 | boolean |  |
| refNode | [Node](../../com.aspose.words/node) |  |
| isAfter | boolean |  |

**退货:**
[字段](../../com.aspose.words/field)
### insert字段(String fieldCode, Node refNode, boolean isAfter) {#insert字段-java.lang.String-com.aspose.words.Node-boolean-}
```
public 字段 insert字段(String fieldCode, Node refNode, boolean isAfter)
```


在此段落中插入一个 Word 字段。在此段落中插入一个字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要插入的域代码（不带花括号）。 |
| refNode | [Node](../../com.aspose.words/node) | 此段落内的引用节点（如果 refNode 为空，则附加到段落的末尾）。 |
| isAfter | boolean | 是在引用节点之后还是之前插入字段。 |

**退货:**
[字段](../../com.aspose.words/field) - 一个[字段](../../com.aspose.words/field)表示插入字段的对象。
### insert字段(String fieldCode, String fieldValue, Node refNode, boolean isAfter) {#insert字段-java.lang.String-java.lang.String-com.aspose.words.Node-boolean-}
```
public 字段 insert字段(String fieldCode, String fieldValue, Node refNode, boolean isAfter)
```


在此段落中插入一个 Word 字段。在此段落中插入一个字段。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | java.lang.String | 要插入的域代码（不带花括号）。 |
| fieldValue | java.lang.String | 要插入的字段值。为没有值的字段传递 null。 |
| refNode | [Node](../../com.aspose.words/node) | 此段落内的引用节点（如果 refNode 为空，则附加到段落的末尾）。 |
| isAfter | boolean | 是在引用节点之后还是之前插入字段。 |

**退货:**
[字段](../../com.aspose.words/field) - 一个[字段](../../com.aspose.words/field)表示插入字段的对象。
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


返回 true，因为此节点可以有子节点。

**退货:**
boolean - True 因为这个节点可以有子节点。
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。

**退货:**
boolean - 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则为 True。
### isEndOfCell() {#isEndOfCell--}
```
public boolean isEndOfCell()
```


如果本段是最后一段，则为真[Cell](../../com.aspose.words/cell);否则为假。

**退货:**
boolean - 对应的布尔值。
### isEndOfDocument() {#isEndOfDocument--}
```
public boolean isEndOfDocument()
```


如果此段落是文档最后一节中的最后一段，则为真。

**退货:**
boolean - 对应的布尔值。
### isEndOfHeaderFooter() {#isEndOfHeaderFooter--}
```
public boolean isEndOfHeaderFooter()
```


如果本段是最后一段，则为真**HeaderFooter**（正文故事）**Section**;否则为假。

**退货:**
boolean - 对应的布尔值。
### isEndOfSection() {#isEndOfSection--}
```
public boolean isEndOfSection()
```


如果本段是最后一段，则为真**Body**（正文故事）**Section**;否则为假。

**退货:**
boolean - 对应的布尔值。
### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。

**退货:**
boolean - 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则为真。
### isInCell() {#isInCell--}
```
public boolean isInCell()
```


如果此段落是直接子级，则为真[Cell](../../com.aspose.words/cell);否则为假。

**退货:**
boolean - 对应的布尔值。
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

**退货:**
boolean - 如果在启用更改跟踪时将此对象插入 Microsoft Word，则为真。
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


当段落是原始修订中的项目符号或编号列表中的项目时为真。

**退货:**
boolean - 对应的布尔值。
### isMoveFromRevision() {#isMoveFromRevision--}
```
public boolean isMoveFromRevision()
```


退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。

**退货:**
布尔值 -**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。
### isMoveToRevision() {#isMoveToRevision--}
```
public boolean isMoveToRevision()
```


退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。

**退货:**
布尔值 -**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。
### iterator() {#iterator--}
```
public Iterator iterator()
```


为在此节点的子节点上的每个样式迭代提供支持。

**退货:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


连接在段落中以相同的格式运行。

**退货:**
 int - 执行的连接数。什么时候**N**相邻的运行正在被加入，它们算作**N - 1**加入。
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




### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数:**
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

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
