---
title: DocumentBase
second_title: Aspose.Words for Java API 参考
description: 为 Word 文档的主文档和词汇表文档提供抽象基类。
type: docs
weight: 121
url: /zh/java/com.aspose.words/documentbase/
---

**遗产：**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public abstract class DocumentBase extends CompositeNode
```

为 Word 文档的主文档和词汇表文档提供抽象基类。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

 Aspose.Words 将 Word 文档表示为节点树。[DocumentBase](../../com.aspose.words/documentbase)是包含文档所有其他节点的树的根节点。

[DocumentBase](../../com.aspose.words/documentbase)还存储文档范围的信息，例如[getStyles()](../../com.aspose.words/documentbase\#getStyles--)和[getLists()](../../com.aspose.words/documentbase\#getLists--)树节点可能会引用。
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接待来访者。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | 获取指定对象类型的第一个祖先。 |
| [getBackgroundShape()](#getBackgroundShape--) | 获取文档的背景形状。 |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [getClass()](#getClass--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDocument()](#getDocument--) |  |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFontInfos()](#getFontInfos--) | 提供对本文档中使用的字体属性的访问。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLists()](#getLists--) | 提供对文档中使用的列表格式的访问。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟在该节点之后的节点。 |
| [getNodeChangingCallback()](#getNodeChangingCallback--) | 在文档中插入或删除节点时调用。 |
| [getNodeType()](#getNodeType--) | 获取此节点的类型。 |
| [getPageColor()](#getPageColor--) | 获取文档的页面颜色。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父级。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在该节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在该节点中的文档部分的对象。 |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | 允许控制外部资源的加载方式。 |
| [getStyles()](#getStyles--) | 返回文档中定义的样式集合。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getWarningCallback()](#getWarningCallback--) | 当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean-) | 将节点从另一个文档导入到当前文档。 |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int-) |  |
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
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape-) | 设置文档的背景形状。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-) | 在文档中插入或删除节点时调用。 |
| [setPageColor(Color value)](#setPageColor-java.awt.Color-) | 设置文档的页面颜色。 |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | 允许控制外部资源的加载方式。 |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | 当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。 |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public abstract boolean accept(DocumentVisitor visitor)
```


接待来访者。

枚举此节点及其所有子节点。每个节点调用 DocumentVisitor 上的相应方法。

有关更多信息，请参阅访问者设计模式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货：**
boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。
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
### getBackgroundShape() {#getBackgroundShape--}
```
public Shape getBackgroundShape()
```


获取文档的背景形状。可以为空。

Microsoft Word 只允许具有其[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--)财产等于[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE)用作文档的背景形状。

Microsoft Word 仅支持背景形状的填充属性。所有其他属性都将被忽略。

将此属性设置为非空值还将设置[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-)为真。

**退货：**
[Shape](../../com.aspose.words/shape) - 文档的背景形状。
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
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取此节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建并且尚未添加到树中，或者如果它已从树中删除也是如此。

**退货：**
[DocumentBase](../../com.aspose.words/documentbase)
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的第一个孩子。
### getFontInfos() {#getFontInfos--}
```
public FontInfoCollection getFontInfos()
```


提供对本文档中使用的字体属性的访问。

该字体定义集合按原样从文档中加载。在某些文档中，字体定义可能是可选的、缺失的或不完整的。

不要依赖此集合来确定文档中使用了特定字体。您应该只使用此集合来获取有关文档中可能使用的字体的信息。

**退货：**
[FontInfoCollection](../../com.aspose.words/fontinfocollection) - 相应的[FontInfoCollection](../../com.aspose.words/fontinfocollection)价值。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货：**
[Node](../../com.aspose.words/node) - 节点的最后一个孩子。
### getLists() {#getLists--}
```
public ListCollection getLists()
```


提供对文档中使用的列表格式的访问。

有关更多信息，请参阅[ListCollection](../../com.aspose.words/listcollection)班级。

**退货：**
[ListCollection](../../com.aspose.words/listcollection) - 相应的[ListCollection](../../com.aspose.words/listcollection)价值。
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
### getNodeChangingCallback() {#getNodeChangingCallback--}
```
public INodeChangingCallback getNodeChangingCallback()
```


在文档中插入或删除节点时调用。

**退货：**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback) - 相应的[INodeChangingCallback](../../com.aspose.words/inodechangingcallback)价值。
### getNodeType() {#getNodeType--}
```
public abstract int getNodeType()
```


获取此节点的类型。

**退货：**
 int - 此节点的类型。返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getPageColor() {#getPageColor--}
```
public Color getPageColor()
```


获取文档的页面颜色。此属性是[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

此属性提供了一种为文档指定纯色页面颜色的简单方法。设置此属性会创建并设置一个适当的[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

如果未设置页面颜色（例如，文档中没有背景形状），则返回零颜色。

**退货：**
java.awt.Color - 文档的页面颜色。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父级。

如果一个节点刚刚被创建并且还没有被添加到树中，或者如果它已经被从树中移除，则父节点为空。

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 此节点的直接父节点。
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
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


允许控制外部资源的加载方式。

**退货：**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - 相应的[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback)价值。
### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


返回文档中定义的样式集合。

有关更多信息，请参阅[StyleCollection](../../com.aspose.words/stylecollection)班级。

**退货：**
[StyleCollection](../../com.aspose.words/stylecollection) 文档中定义的样式集合。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制字符和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货：**
java.lang.字符串
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。文档可能在其存在的任何阶段产生警告，因此尽早设置警告回调以避免警告丢失非常重要。例如这样的属性[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--)实际构建稍后用于渲染的文档布局，如果为稍后的渲染调用指定警告回调，布局警告可能会丢失。

**退货：**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。
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
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean-}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


将节点从另一个文档导入到当前文档。

将节点从另一个文档导入到当前文档。

此方法使用[ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode\#USE-DESTINATION-STYLES)解决格式化的选项。

导入节点会创建属于导入文档的源节点的副本。返回的节点没有父节点。源节点未更改或从原始文档中删除。

在将来自另一个文档的节点插入到该文档之前，必须导入它。在导入过程中，特定于文档的属性（例如对样式和列表的引用）将从原始文档转换为导入文档。节点导入后，可以使用插入到文档中的适当位置[CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-)或者[CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-).

如果源节点已经属于目标文档，则只需创建源节点的深度克隆。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) | 正在导入的节点。 |
| isImportChildren | boolean | True 递归导入所有子节点；否则，假的。 |

**退货：**
[Node](../../com.aspose.words/node) 属于当前文档的克隆节点。
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int-}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**退货：**
[Node](../../com.aspose.words/node)
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
### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape-}
```
public void setBackgroundShape(Shape value)
```


设置文档的背景形状。可以为空。

Microsoft Word 只允许具有其[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--)财产等于[ShapeType.RECTANGLE](../../com.aspose.words/shapetype\#RECTANGLE)用作文档的背景形状。

Microsoft Word 仅支持背景形状的填充属性。所有其他属性都将被忽略。

将此属性设置为非空值还将设置[ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions\#getDisplayBackgroundShape--) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions\#setDisplayBackgroundShape-boolean-)为真。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | 文档的背景形状。 |

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

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback-}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


在文档中插入或删除节点时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback) | 相应的[INodeChangingCallback](../../com.aspose.words/inodechangingcallback)价值。 |

### setPageColor(Color value) {#setPageColor-java.awt.Color-}
```
public void setPageColor(Color value)
```


设置文档的页面颜色。此属性是[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

此属性提供了一种为文档指定纯色页面颜色的简单方法。设置此属性会创建并设置一个适当的[getBackgroundShape()](../../com.aspose.words/documentbase\#getBackgroundShape--) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase\#setBackgroundShape-com.aspose.words.Shape-).

如果未设置页面颜色（例如，文档中没有背景形状），则返回零颜色。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 文档的页面颜色。 |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


允许控制外部资源的加载方式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) | 相应的[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback)价值。 |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


当检测到可能导致数据或格式保真度丢失的问题时，在各种文档处理过程中调用。文档可能在其存在的任何阶段产生警告，因此尽早设置警告回调以避免警告丢失非常重要。例如这样的属性[Document.getPageCount()](../../com.aspose.words/document\#getPageCount--)实际构建稍后用于渲染的文档布局，如果为稍后的渲染调用指定警告回调，布局警告可能会丢失。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | 相应的[IWarningCallback](../../com.aspose.words/iwarningcallback)价值。 |

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
