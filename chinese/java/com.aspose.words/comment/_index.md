---
title: Comment
second_title: Aspose.Words for Java API 参考
description:表示注释文本的容器。
type: docs
weight: 76
url: /zh/java/com.aspose.words/comment/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.InlineStory](../../com.aspose.words/inlinestory)
```
public class Comment extends InlineStory
```

表示注释文本的容器。

要了解更多信息，请访问**Working with Comments**文档文章。

注释是锚定到文本区域或文本位置的注释。评论可以包含任意数量的块级内容。

如果一个[Comment](../../com.aspose.words/comment)对象自己出现，评论被锚定到[Comment](../../com.aspose.words/comment)目的。

要将注释锚定到文本区域，需要三个对象：[Comment](../../com.aspose.words/comment), [CommentRangeStart](../../com.aspose.words/commentrangestart)和[CommentRangeEnd](../../com.aspose.words/commentrangeend) .所有三个对象都需要共享相同的[getId()](../../com.aspose.words/comment\#getId--)价值。

[Comment](../../com.aspose.words/comment)是一个内联级节点，只能是[Paragraph](../../com.aspose.words/paragraph).

[Comment](../../com.aspose.words/comment)可以包含[Paragraph](../../com.aspose.words/paragraph)和[Table](../../com.aspose.words/table)子节点。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [Comment(DocumentBase doc)](#Comment-com.aspose.words.DocumentBase-) | 初始化一个新的实例**Comment**班级。 |
| [Comment(DocumentBase doc, String author, String initial, Date dateTime)](#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date-) | 初始化一个新的实例**Comment**班级。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
| [addReply(String author, String initial, Date dateTime, String text)](#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String-) | 添加对此评论的回复。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [ensureMinimum()](#ensureMinimum--) | 如果最后一个孩子不是段落，则创建并附加一个空段落。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor()](#getAncestor--) | 返回父评论对象。 |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getAuthor()](#getAuthor--) | 获取评论的作者姓名。 |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDateTime()](#getDateTime--) | 获取发表评论的日期和时间。 |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getDone()](#getDone--) | 获取指示评论已被标记为完成的标志。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstParagraph()](#getFirstParagraph--) | 获取故事的第一段。 |
| [getFont()](#getFont--) | 提供对此对象的锚字符的字体格式的访问。 |
| [getId()](#getId--) | 获取评论标识符。 |
| [getIdInternal()](#getIdInternal--) |  |
| [getInitial()](#getInitial--) | 获取与特定评论关联的用户的姓名缩写。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastParagraph()](#getLastParagraph--) | 获取故事的最后一段。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) | 退货**Node类型.Comment**. |
| [getParagraphs()](#getParagraphs--) | 获取作为故事的直接子级的段落的集合。 |
| [getParentIdInternal()](#getParentIdInternal--) |  |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getParentParagraph()](#getParentParagraph--) | 检索父级[Paragraph](../../com.aspose.words/paragraph)这个节点的。 |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getReplies()](#getReplies--) | 返回一个集合[Comment](../../com.aspose.words/comment)作为指定注释的直接子级的对象。 |
| [getStory类型()](#getStory类型--) | 退货**Story类型.Comments**. |
| [getTables()](#getTables--) | 获取作为故事的直接子级的表的集合。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
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
| [removeAllReplies()](#removeAllReplies--) | 删除对此评论的所有回复。 |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node-) | 移除指定的子节点。 |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeReply(Comment reply)](#removeReply-com.aspose.words.Comment-) | 删除对此评论的指定回复。 |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | 设置评论的作者姓名。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setDateTime(Date value)](#setDateTime-java.util.Date-) | 获取发表评论的日期和时间。 |
| [setDone(boolean value)](#setDone-boolean-) | 设置标志，指示评论已被标记为完成。 |
| [setIdInternal(int value)](#setIdInternal-int-) |  |
| [setInitial(String value)](#setInitial-java.lang.String-) | 设置与特定评论关联的用户的首字母。 |
| [setParentIdInternal(int value)](#setParentIdInternal-int-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setText(String text)](#setText-java.lang.String-) | 这是一种方便的方法，可以轻松设置评论的文本。 |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### Comment(DocumentBase doc) {#Comment-com.aspose.words.DocumentBase-}
```
public Comment(DocumentBase doc)
```


初始化一个新的实例**Comment**班级。

什么时候**Comment**已创建，它属于指定的文档，但还不是文档的一部分，并且**ParentNode**一片空白。

追加**Comment**在要插入注释的段落上使用 InsertAfter 或 InsertBefore 到文档。

创建评论后，不要忘记设置它[getAuthor()](../../com.aspose.words/comment\#getAuthor--) / [setAuthor(java.lang.String)](../../com.aspose.words/comment\#setAuthor-java.lang.String-), [getInitial()](../../com.aspose.words/comment\#getInitial--) / [setInitial(java.lang.String)](../../com.aspose.words/comment\#setInitial-java.lang.String-)和[getDateTime()](../../com.aspose.words/comment\#getDateTime--) / [setDateTime(java.util.Date)](../../com.aspose.words/comment\#setDateTime-java.util.Date-)特性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | 所有者文件。 |

### Comment(DocumentBase doc, String author, String initial, Date dateTime) {#Comment-com.aspose.words.DocumentBase-java.lang.String-java.lang.String-java.util.Date-}
```
public Comment(DocumentBase doc, String author, String initial, Date dateTime)
```


初始化一个新的实例**Comment**班级。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) | 所有者文件。 |
| author | java.lang.String | 评论的作者姓名。不能为空。 |
| initial | java.lang.String | 评论的作者姓名缩写。不能为空。 |
| dateTime | java.util.Date | 评论的日期和时间。 |

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
 boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。来电[DocumentVisitor.visitCommentStart(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor\#visitCommentStart-com.aspose.words.Comment-) ，然后调用[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-)对于评论和调用的所有子节点[DocumentVisitor.visitCommentEnd(com.aspose.words.Comment)](../../com.aspose.words/documentvisitor\#visitCommentEnd-com.aspose.words.Comment-)在最后。
### addReply(String author, String initial, Date dateTime, String text) {#addReply-java.lang.String-java.lang.String-java.util.Date-java.lang.String-}
```
public Comment addReply(String author, String initial, Date dateTime, String text)
```


添加对此评论的回复。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| author | java.lang.String | 回复的作者姓名。 |
| initial | java.lang.String | 回复的作者姓名缩写。 |
| dateTime | java.util.Date | 回复的日期和时间。 |
| text | java.lang.String | 回复文字。 |

**退货:**
[Comment](../../com.aspose.words/comment) 创建的[Comment](../../com.aspose.words/comment)回复的节点。由于现有的 MS Office 限制，文档中只允许 1 级回复。如果在现有的回复注释上调用此方法，则会引发 java.lang.IllegalStateException 类型的异常。
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
### getAncestor() {#getAncestor--}
```
public Comment getAncestor()
```


返回父评论对象。为顶级注释返回 null。

**退货:**
[Comment](../../com.aspose.words/comment) - 父评论对象。
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
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


获取评论的作者姓名。

不能为空。

默认为空字符串。

**退货:**
java.lang.String - 评论的作者姓名。
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
### getDateTime() {#getDateTime--}
```
public Date getDateTime()
```


获取发表评论的日期和时间。

默认值为 03.01.0001。

**退货:**
java.util.Date - 发表评论的日期和时间。
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
### getDone() {#getDone--}
```
public boolean getDone()
```


获取指示评论已被标记为完成的标志。

**退货:**
boolean - 指示评论已被标记为完成的标志。
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
### getId() {#getId--}
```
public int getId()
```


获取评论标识符。

注释标识符允许将注释锚定到文档中的文本区域。该区域必须使用[CommentRangeStart](../../com.aspose.words/commentrangestart)和[CommentRangeEnd](../../com.aspose.words/commentrangeend)对象共享相同的标识符值作为[Comment](../../com.aspose.words/comment)目的。

在查找[CommentRangeStart](../../com.aspose.words/commentrangestart)和[CommentRangeEnd](../../com.aspose.words/commentrangeend)链接到此评论的节点。

注释标识符在整个文档中应该是唯一的，并且 Aspose.Words 在加载、保存和组合文档时会自动维护注释标识符。

**退货:**
int - 评论标识符。
### getIdInternal() {#getIdInternal--}
```
public int getIdInternal()
```




**退货:**
整数
### getInitial() {#getInitial--}
```
public String getInitial()
```


获取与特定评论关联的用户的姓名缩写。

不能为空。

默认为空字符串。

**退货:**
java.lang.String - 与特定评论相关联的用户姓名首字母。
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


退货**Node类型.Comment**.

**退货:**
诠释 -**Node类型.Comment** .返回值是以下之一[Node类型](../../com.aspose.words/nodetype)常数。
### getParagraphs() {#getParagraphs--}
```
public ParagraphCollection getParagraphs()
```


获取作为故事的直接子级的段落的集合。

**退货:**
[ParagraphCollection](../../com.aspose.words/paragraphcollection) - 作为故事直接子级的段落集合。
### getParentIdInternal() {#getParentIdInternal--}
```
public int getParentIdInternal()
```




**退货:**
整数
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
### getReplies() {#getReplies--}
```
public CommentCollection getReplies()
```


返回一个集合[Comment](../../com.aspose.words/comment)作为指定注释的直接子级的对象。

**退货:**
[CommentCollection](../../com.aspose.words/commentcollection) - 集合[Comment](../../com.aspose.words/comment)作为指定注释的直接子级的对象。
### getStory类型() {#getStory类型--}
```
public int getStory类型()
```


退货**Story类型.Comments**.

**退货:**
诠释 -**Story类型.Comments** .返回值是以下之一[Story类型](../../com.aspose.words/storytype)常数。
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

### removeAllReplies() {#removeAllReplies--}
```
public void removeAllReplies()
```


删除对此评论的所有回复。回复的所有组成节点将从文档中删除。

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




### removeReply(Comment reply) {#removeReply-com.aspose.words.Comment-}
```
public void removeReply(Comment reply)
```


删除对此评论的指定回复。回复的所有组成节点将从文档中删除。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| reply | [Comment](../../com.aspose.words/comment) | 删除回复的评论节点。 |

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
### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


设置评论的作者姓名。

不能为空。

默认为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 评论的作者姓名。 |

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

### setDateTime(Date value) {#setDateTime-java.util.Date-}
```
public void setDateTime(Date value)
```


获取发表评论的日期和时间。

默认值为 03.01.0001。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 发表评论的日期和时间。 |

### setDone(boolean value) {#setDone-boolean-}
```
public void setDone(boolean value)
```


设置标志，指示评论已被标记为完成。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示评论已被标记为完成的标志。 |

### setIdInternal(int value) {#setIdInternal-int-}
```
public void setIdInternal(int value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setInitial(String value) {#setInitial-java.lang.String-}
```
public void setInitial(String value)
```


设置与特定评论关联的用户的首字母。

不能为空。

默认为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 与特定评论相关联的用户姓名缩写。 |

### setParentIdInternal(int value) {#setParentIdInternal-int-}
```
public void setParentIdInternal(int value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setText(String text) {#setText-java.lang.String-}
```
public void setText(String text)
```


这是一种方便的方法，可以轻松设置评论的文本。

此方法允许从字符串中快速设置注释文本。字符串可以包含分段符，这将在评论中相应地创建文本段落。如果您想在评论中插入更复杂的元素，例如书签或表格或应用丰富的格式，那么您需要使用适当的节点类来构建评论文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | java.lang.String | 评论的新文本。 |

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
