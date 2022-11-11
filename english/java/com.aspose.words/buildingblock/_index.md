---
title: BuildingBlock
second_title: Aspose.Words for Java API 参考
description: 表示词汇表文档条目，例如 Building Block 自动图文集或自动更正条目。
type: docs
weight: 41
url: /zh/java/com.aspose.words/buildingblock/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode)
```
public class BuildingBlock extends CompositeNode
```

表示词汇表文档条目，例如 Building Block、自动图文集或自动更正条目。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

[BuildingBlock](../../com.aspose.words/buildingblock)只能包含[Section](../../com.aspose.words/section)节点。

[BuildingBlock](../../com.aspose.words/buildingblock)只能是[GlossaryDocument](../../com.aspose.words/glossarydocument).

您可以创建新的构建块并将它们插入到词汇表文档中。您可以修改或删除现有的构建块。您可以在文档之间复制或移动构建基块。您可以将构建块的内容插入到文档中。

对应于**docPart**, **docPartPr**和**docPartBody**OOXML 中的元素。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [BuildingBlock(GlossaryDocument glossaryDoc)](#BuildingBlock-com.aspose.words.GlossaryDocument-) | 初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接受访客。 |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getBehavior()](#getBehavior--) | 指定将构建块的内容插入主文档时应应用的行为。 |
| [getCategory()](#getCategory--) | 指定构建块的二级分类。 |
| [getChild(int node类型, int index, boolean isDeep)](#getChild-int-int-boolean-) |  |
| [getChildNodes()](#getChildNodes--) | 获取此节点的所有直接子节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getContainer()](#getContainer--) |  |
| [getCount()](#getCount--) | 获取此节点的直接子节点数。 |
| [getCurrentNode()](#getCurrentNode--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [get描述()](#get描述--) | 获取与此构建块关联的描述。 |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getFirstChild()](#getFirstChild--) | 获取节点的第一个子节点。 |
| [getFirstSection()](#getFirstSection--) | 获取构建块中的第一部分。 |
| [getGallery()](#getGallery--) | 为分类或用户界面排序指定构建块的第一级分类。 |
| [getGuid()](#getGuid--) | 获取唯一标识此构建块的标识符（128 位 GUID）。 |
| [getLastChild()](#getLastChild--) | 获取节点的最后一个子节点。 |
| [getLastSection()](#getLastSection--) | 获取构建块中的最后一个部分。 |
| [getName()](#getName--) | 获取此构建块的名称。 |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node-) |  |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) | 返回[Node类型.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK)价值。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getSections()](#getSections--) | 返回表示构建块中所有部分的集合。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [get类型()](#get类型--) | 指定构建块类型。 |
| [hasChildNodes()](#hasChildNodes--) | 如果此节点有任何子节点，则返回 true。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node-) | 返回子节点数组中指定子节点的索引。 |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之后立即插入指定的节点。 |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node-) | 在指定的参考节点之前插入指定的节点。 |
| [isComposite()](#isComposite--) | 返回 true，因为此节点可以有子节点。 |
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
| [removeSmartTags()](#removeSmartTags--) | 删除所有[SmartTag](../../com.aspose.words/smarttag)当前节点的后代节点。 |
| [selectNodes(String xpath)](#selectNodes-java.lang.String-) | 选择与 XPath 表达式匹配的节点列表。 |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String-) | 选择与 XPath 表达式匹配的第一个节点。 |
| [setBehavior(int value)](#setBehavior-int-) | 指定将构建块的内容插入主文档时应应用的行为。 |
| [setCategory(String value)](#setCategory-java.lang.String-) | 指定构建块的二级分类。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [set描述(String value)](#set描述-java.lang.String-) | 设置与此构建块关联的描述。 |
| [setGallery(int value)](#setGallery-int-) | 为分类或用户界面排序指定构建块的第一级分类。 |
| [setGuid(UUID value)](#setGuid-java.util.UUID-) | 设置唯一标识此构建块的标识符（128 位 GUID）。 |
| [setName(String value)](#setName-java.lang.String-) | 设置此构建块的名称。 |
| [set类型(int value)](#set类型-int-) | 指定构建块类型。 |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BuildingBlock(GlossaryDocument glossaryDoc) {#BuildingBlock-com.aspose.words.GlossaryDocument-}
```
public BuildingBlock(GlossaryDocument glossaryDoc)
```


初始化此类的新实例。

什么时候[BuildingBlock](../../com.aspose.words/buildingblock)已创建，它属于指定的词汇表文档，但还不是词汇表文档的一部分，并且[Node.getParentNode()](../../com.aspose.words/node\#getParentNode--)一片空白 。

追加[BuildingBlock](../../com.aspose.words/buildingblock)到一个[GlossaryDocument](../../com.aspose.words/glossarydocument)利用[CompositeNode.appendChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#appendChild-com.aspose.words.Node-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| glossaryDoc | [GlossaryDocument](../../com.aspose.words/glossarydocument) | 所有者文件。 |

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
boolean - 如果所有节点都被访问，则为真；如果 DocumentVisitor 在访问所有节点之前停止操作，则返回 false。

来电[DocumentVisitor.visitBuildingBlockStart(com.aspose.words.BuildingBlock)](../../com.aspose.words/documentvisitor\#visitBuildingBlockStart-com.aspose.words.BuildingBlock-) ，然后调用[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-)对于此构建块的所有子节点，然后调用[DocumentVisitor.visitBuildingBlockEnd(com.aspose.words.BuildingBlock)](../../com.aspose.words/documentvisitor\#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-).

注意：当您通过一个访问者执行一个构建块节点及其子节点[Document](../../com.aspose.words/document).如果要在构建块上执行访问者，则需要执行访问者[GlossaryDocument](../../com.aspose.words/glossarydocument)或致电[accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).
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
### getBehavior() {#getBehavior--}
```
public int getBehavior()
```


指定将构建块的内容插入主文档时应应用的行为。

**退货:**
int - 对应的 int 值。返回值是以下之一[BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior)常数。
### getCategory() {#getCategory--}
```
public String getCategory()
```


指定构建块的二级分类。

Microsoft Word 用户界面中的构建块被排列成画廊。每个[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-)可以有多个类别。一个内的每个块[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-)有个[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

不能为 null，也不能为空字符串。

对应于**docPartPr.category.name** OOXML 中的元素。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
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
### get描述() {#get描述--}
```
public String get描述()
```


获取与此构建块关联的描述。

描述可能包含任何字符串内容，通常是附加信息。

不能为 null ，但可以为空字符串。

对应于**docPartPr.description** OOXML 中的元素。

**退货:**
java.lang.String - 与此构建块关联的描述。
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取该节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建但尚未添加到树中，或者已从树中删除。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getFirstChild() {#getFirstChild--}
```
public Node getFirstChild()
```


获取节点的第一个子节点。如果没有第一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的第一个子节点。
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


获取构建块中的第一部分。如果没有节，则返回 null。

**退货:**
[Section](../../com.aspose.words/section) - 构建块的第一部分。
### getGallery() {#getGallery--}
```
public int getGallery()
```


为分类或用户界面排序指定构建块的第一级分类。

Microsoft Word 用户界面中的构建块被排列成画廊。每个[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-)可以有多个类别。一个内的每个块[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-)有个[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

对应于**docPartPr.category.gallery** OOXML 中的元素。

**退货:**
int - 对应的 int 值。返回值是以下之一[BuildingBlockGallery](../../com.aspose.words/buildingblockgallery)常数。
### getGuid() {#getGuid--}
```
public UUID getGuid()
```


获取唯一标识此构建块的标识符（128 位 GUID）。

应用程序可以使用它来唯一地引用构建块，而不管由于本地化而导致的不同命名。

对应于**docPartPr.guid** OOXML 中的元素。

**退货:**
java.util.UUID - 唯一标识此构建块的标识符（128 位 GUID）。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取节点的最后一个子节点。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - 节点的最后一个子节点。
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


获取构建块中的最后一个部分。如果没有节，则返回 null。

**退货:**
[Section](../../com.aspose.words/section) 构建块的最后一部分。
### getName() {#getName--}
```
public String getName()
```


获取此构建块的名称。

名称可以包含任何字符串内容，通常是友好的标识符。多个构建块可以具有相同的名称。

不能为 null，也不能为空字符串。

对应于**docPartPr.name** OOXML 中的元素。

**退货:**
java.lang.String - 此构建块的名称。
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


返回[Node类型.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK)价值。

**退货:**
诠释 - 的[Node类型.BUILDING\_BLOCK](../../com.aspose.words/nodetype\#BUILDING-BLOCK)价值。返回值是以下之一[Node类型](../../com.aspose.words/nodetype)常数。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父节点。

如果一个节点刚刚创建但尚未添加到树中，或者它已从树中删除，则父节点为空。

**退货:**
[CompositeNode](../../com.aspose.words/compositenode) - 该节点的直接父节点。
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
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


返回表示构建块中所有部分的集合。

**退货:**
[SectionCollection](../../com.aspose.words/sectioncollection) 代表构建块中所有部分的集合。
### getText() {#getText--}
```
public String getText()
```


获取此节点及其所有子节点的文本。

返回的字符串包括所有控制和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货:**
java.lang.String
### get类型() {#get类型--}
```
public int get类型()
```


指定构建块类型。

构建基块类型会影响 Microsoft Word 中构建基块的可见性和行为。

对应于**docPartPr.types** OOXML 中的元素。

**退货:**
int - 对应的 int 值。返回值是以下之一[BuildingBlock类型](../../com.aspose.words/buildingblocktype)常数。
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
### setBehavior(int value) {#setBehavior-int-}
```
public void setBehavior(int value)
```


指定将构建块的内容插入主文档时应应用的行为。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[BuildingBlockBehavior](../../com.aspose.words/buildingblockbehavior)常数。 |

### setCategory(String value) {#setCategory-java.lang.String-}
```
public void setCategory(String value)
```


指定构建块的二级分类。

Microsoft Word 用户界面中的构建块被排列成画廊。每个[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-)可以有多个类别。一个内的每个块[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-)有个[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

不能为 null，也不能为空字符串。

对应于**docPartPr.category.name** OOXML 中的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

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

### set描述(String value) {#set描述-java.lang.String-}
```
public void set描述(String value)
```


设置与此构建块关联的描述。

描述可能包含任何字符串内容，通常是附加信息。

不能为 null ，但可以为空字符串。

对应于**docPartPr.description** OOXML 中的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 与此构建块关联的描述。 |

### setGallery(int value) {#setGallery-int-}
```
public void setGallery(int value)
```


为分类或用户界面排序指定构建块的第一级分类。

Microsoft Word 用户界面中的构建块被排列成画廊。每个[getGallery()](../../com.aspose.words/buildingblock\#getGallery--) / [setGallery(int)](../../com.aspose.words/buildingblock\#setGallery-int-)可以有多个类别。一个内的每个块[getCategory()](../../com.aspose.words/buildingblock\#getCategory--) / [setCategory(java.lang.String)](../../com.aspose.words/buildingblock\#setCategory-java.lang.String-)有个[getName()](../../com.aspose.words/buildingblock\#getName--) / [setName(java.lang.String)](../../com.aspose.words/buildingblock\#setName-java.lang.String-).

对应于**docPartPr.category.gallery** OOXML 中的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[BuildingBlockGallery](../../com.aspose.words/buildingblockgallery)常数。 |

### setGuid(UUID value) {#setGuid-java.util.UUID-}
```
public void setGuid(UUID value)
```


设置唯一标识此构建块的标识符（128 位 GUID）。

应用程序可以使用它来唯一地引用构建块，而不管由于本地化而导致的不同命名。

对应于**docPartPr.guid** OOXML 中的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.UUID | 唯一标识此构建块的标识符（128 位 GUID）。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置此构建块的名称。

名称可以包含任何字符串内容，通常是友好的标识符。多个构建块可以具有相同的名称。

不能为 null，也不能为空字符串。

对应于**docPartPr.name** OOXML 中的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 此构建块的名称。 |

### set类型(int value) {#set类型-int-}
```
public void set类型(int value)
```


指定构建块类型。

构建基块类型会影响 Microsoft Word 中构建基块的可见性和行为。

对应于**docPartPr.types** OOXML 中的元素。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[BuildingBlock类型](../../com.aspose.words/buildingblocktype)常数。 |

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
