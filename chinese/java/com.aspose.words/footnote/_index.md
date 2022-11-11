---
title: Footnote
second_title: Aspose.Words for Java API Reference
description: 表示脚注或尾注文本的容器。
type: docs
weight: 291
url: /zh/java/com.aspose.words/footnote/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory)
```
public class Footnote extends InlineStory
```

表示脚注或尾注文本的容器。

要了解更多信息，请访问**Working with Footnote and Endnote**文档文章。

这**Footnote**类用于表示 Word 文档中的脚注和尾注。

**Footnote**是一个内联级节点，只能是**Paragraph**.

**Footnote**可以包含**Paragraph**和**Table**子节点。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [Footnote(DocumentBase doc, int footnote类型)](#Footnote-com.aspose.words.DocumentBase-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [ensureMinimum()](#ensureMinimum--) | 如果最后一个孩子不是段落，则创建并附加一个空段落。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstParagraph()](#getFirstParagraph--) | 获取故事的第一段。 |
| [getFont()](#getFont--) | 提供对此对象的锚字符的字体格式的访问。 |
| [getFootnote类型()](#getFootnote类型--) | 返回一个值，该值指定这是脚注还是尾注。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastParagraph()](#getLastParagraph--) | 获取故事的最后一段。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) | 退货**Node类型.Footnote**. |
| [getParagraphs()](#getParagraphs--) | 获取作为故事的直接子级的段落的集合。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getParentParagraph()](#getParentParagraph--) | 检索父级[Paragraph](../../com.aspose.words/paragraph)这个节点的。 |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getReferenceMark()](#getReferenceMark--) | 获取/设置用于此脚注的自定义参考标记。 |
| [getStory类型()](#getStory类型--) | 退货**Story类型.Footnotes**或者**Story类型.Endnotes**. |
| [getTables()](#getTables--) | 获取作为故事的直接子级的表的集合。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
| [isAuto()](#isAuto--) | 保存一个值，该值指定这是自动编号的脚注还是带有用户定义的自定义参考标记的脚注。 |
| [isAuto(boolean value)](#isAuto-boolean-) | 保存一个值，该值指定这是自动编号的脚注还是带有用户定义的自定义参考标记的脚注。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [isInsertRevision()](#isInsertRevision--) | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [isMoveFromRevision()](#isMoveFromRevision--) | 退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [isMoveToRevision()](#isMoveToRevision--) | 退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
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
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setReferenceMark(String value)](#setReferenceMark-java.lang.String-) | 获取/设置用于此脚注的自定义参考标记。 |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Footnote(DocumentBase doc, int footnote类型) {#Footnote-com.aspose.words.DocumentBase-int-}
```
public Footnote(DocumentBase doc, int footnote类型)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| footnote类型 | int |  |

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
boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。调用 DocumentVisitor.VisitFootnoteStart，然后为脚注的所有子节点调用 Accept，最后调用 DocumentVisitor.VisitFootnoteEnd。
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
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


如果最后一个孩子不是段落，则创建并附加一个空段落。

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
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

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
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

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
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**退货:**
[DocumentBase](../../com.aspose.words/documentbase)
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的第一个子节点。
### getFirstParagraph() {#getFirstParagraph--}
```
public Paragraph getFirstParagraph()
```


获取故事的第一段。

**退货:**
[Paragraph](../../com.aspose.words/paragraph) - 故事的第一段。
### getFont() {#getFont--}
```
public Font getFont()
```


提供对此对象的锚字符的字体格式的访问。

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getFootnote类型() {#getFootnote类型--}
```
public int getFootnote类型()
```


返回一个值，该值指定这是脚注还是尾注。

**退货:**
 int - 指定这是脚注还是尾注的值。返回值是以下之一[Footnote类型](../../com.aspose.words/footnotetype)常数。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的最后一个子节点。
### getLastParagraph() {#getLastParagraph--}
```
public Paragraph getLastParagraph()
```


获取故事的最后一段。

**退货:**
[Paragraph](../../com.aspose.words/paragraph) - 故事的最后一段。
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


退货**Node类型.Footnote**.

**退货:**
诠释 -**Node类型.Footnote** .返回值是以下之一[Node类型](../../com.aspose.words/nodetype)常数。
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


获取作为故事的直接子级的段落的集合。

**退货:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - 作为故事直接子级的段落集合。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父节点。

如果一个节点刚刚创建但尚未添加到树中，或者它已从树中删除，则父节点为空。

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 该节点的直接父节点。
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


检索父级[Paragraph](../../com.aspose.words/paragraph)这个节点的。

**退货:**
[Paragraph](../../com.aspose.words/paragraph) - 相应的[Paragraph](../../com.aspose.words/paragraph)价值。
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**退货:**
[Paragraph](../../com.aspose.words/paragraph)
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
### getReferenceMark() {#getReferenceMark--}
```
public String getReferenceMark()
```


获取/设置用于此脚注的自定义参考标记。默认值为**empty string**，表示使用自动编号的脚注。

如果此属性设置为**empty string**或为空，则[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-)属性将自动设置为 true，如果设置为其他任何值，则[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-)将设置为假。

RTF 格式只能存储 1 个符号作为自定义参考标记，因此在导出时只会写入第一个符号，其他符号将被丢弃。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getStory类型() {#getStory类型--}
```
public int getStory类型()
```


退货**Story类型.Footnotes**或者**Story类型.Endnotes**.

**退货:**
诠释 -**Story类型.Footnotes**或者**Story类型.Endnotes** .返回值是以下之一[Story类型](../../com.aspose.words/storytype)常数。
### getTables() {#getTables--}
```
public TableCollection getTables()
```


获取作为故事的直接子级的表的集合。

**退货:**
[TableCollection](../../com.aspose.words/tablecollection) 作为故事直接子级的表格集合。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

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
### isAuto() {#isAuto--}
```
public boolean isAuto()
```


保存一个值，该值指定这是自动编号的脚注还是带有用户定义的自定义参考标记的脚注。[getReferenceMark()](../../com.aspose.words/footnote\#getReferenceMark--) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote\#setReferenceMark-java.lang.String-)如果 IsAuto 设置为 false，则使用空字符串初始化。

**退货:**
boolean - 对应的布尔值。
### isAuto(boolean value) {#isAuto-boolean-}
```
public void isAuto(boolean value)
```


保存一个值，该值指定这是自动编号的脚注还是带有用户定义的自定义参考标记的脚注。[getReferenceMark()](../../com.aspose.words/footnote\#getReferenceMark--) / [setReferenceMark(java.lang.String)](../../com.aspose.words/footnote\#setReferenceMark-java.lang.String-)如果 IsAuto 设置为 false，则使用空字符串初始化。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

**退货:**
boolean - 如果在启用更改跟踪时将此对象插入 Microsoft Word，则为真。
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

### setReferenceMark(String value) {#setReferenceMark-java.lang.String-}
```
public void setReferenceMark(String value)
```


获取/设置用于此脚注的自定义参考标记。默认值为**empty string**，表示使用自动编号的脚注。

如果此属性设置为**empty string**或为空，则[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-)属性将自动设置为 true，如果设置为其他任何值，则[isAuto()](../../com.aspose.words/footnote\#isAuto--) / [isAuto(boolean)](../../com.aspose.words/footnote\#isAuto-boolean-)将设置为假。

RTF 格式只能存储 1 个符号作为自定义参考标记，因此在导出时只会写入第一个符号，其他符号将被丢弃。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |
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
