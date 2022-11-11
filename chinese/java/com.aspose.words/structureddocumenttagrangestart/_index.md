---
title: StructuredDocumentTagRangeStart
second_title: Aspose.Words for Java API Reference
description: 表示接受多节内容的范围结构化文档标签的开始。
type: docs
weight: 535
url: /zh/java/com.aspose.words/structureddocumenttagrangestart/
---

**遗产:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node)

**所有实现的接口:**
[com.aspose.words.IStructuredDocumentTag](../../com.aspose.words/istructureddocumenttag), java.lang.Iterable
```
public class StructuredDocumentTagRangeStart extends Node implements IStructuredDocumentTag, Iterable
```

代表一个开始**ranged**接受多节内容的结构化文档标签。也可以看看[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend).

要了解更多信息，请访问**Structured Document Tags or Content Control**文档文章。

可以是直系子女[Body](../../com.aspose.words/body)节点**only**.
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [StructuredDocumentTagRangeStart(DocumentBase doc, int type)](#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) |  |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node-) | 将指定节点添加到 stdContent 范围的末尾。 |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAncestor(int ancestor类型)](#getAncestor-int-) |  |
| [getAncestor(班级 ancestor类型)](#getAncestor-java.lang.班级-) | 获取指定对象类型的第一个祖先。 |
| [getChildNodes()](#getChildNodes--) | 获取此范围开始节点和范围结束节点之间的所有节点。 |
| [getChildNodes(int node类型, boolean isDeep)](#getChildNodes-int-boolean-) |  |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取结构化文档标签的颜色。 |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDocument()](#getDocument--) | 获取该节点所属的文档。 |
| [getId()](#getId--) | 为此结构化文档标签指定一个唯一的只读持久数字 ID。 |
| [getLastChild()](#getLastChild--) | 获取 stdContent 范围中的最后一个子项。 |
| [getLevel()](#getLevel--) | 获取此结构化文档标记范围开始出现在文档树中的级别。 |
| [getLockContentControl()](#getLockContentControl--) | 当设置为 true 时，此属性将禁止用户删除此结构化文档标记。 |
| [getLockContents()](#getLockContents--) | 当设置为 true 时，此属性将禁止用户编辑此结构化文档标记的内容。 |
| [getNextSibling()](#getNextSibling--) | 获取紧跟此节点的节点。 |
| [getNode类型()](#getNode类型--) |  |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父节点。 |
| [getPlaceholder()](#getPlaceholder--) | 获取[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此结构化文档标记运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-)元素为真。 |
| [getPlaceholderName()](#getPlaceholderName--) | 获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。 |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在此节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在此节点中的文档部分的对象。 |
| [getRangeEnd()](#getRangeEnd--) | 如果 StructuredDocumentTag 是范围结构化文档标记，则指定范围结束。 |
| [getSdt类型()](#getSdt类型--) | 获取此结构化文档标签的类型。 |
| [getTag()](#getTag--) | 指定与当前结构化文档标签节点关联的标签。 |
| [getText()](#getText--) | 获取此节点及其所有子节点的文本。 |
| [getTitle()](#getTitle--) | 指定与此结构化文档标记关联的友好名称。 |
| [getWordOpenXML()](#getWordOpenXML--) | 获取一个字符串，该字符串表示包含在[SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC)格式。 |
| [getXmlMapping()](#getXmlMapping--) | 获取一个对象，该对象表示此结构化文档标记范围到当前文档的自定义 XML 部分中的 XML 数据的映射。 |
| [hashCode()](#hashCode--) |  |
| [isComposite()](#isComposite--) | 如果此节点可以包含其他节点，则返回 true。 |
| [isRanged()](#isRanged--) |  |
| [isShowingPlaceholderText()](#isShowingPlaceholderText--) | 指定是否应将此结构化文档标签的内容解释为包含占位符文本（与结构化文档标签内的常规文本内容相反）。 |
| [isShowingPlaceholderText(boolean value)](#isShowingPlaceholderText-boolean-) | 指定是否应将此结构化文档标签的内容解释为包含占位符文本（与结构化文档标签内的常规文本内容相反）。 |
| [iterator()](#iterator--) | 为在此节点的子节点上的每个样式迭代提供支持。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [node类型ToString(int node类型)](#node类型ToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeAllChildren()](#removeAllChildren--) | 删除此范围开始节点和范围结束节点之间的所有节点。 |
| [removeSelfOnly()](#removeSelfOnly--) | 删除结构化文档标记的此范围开始和适当范围结束节点，但将其内容保留在文档树内。 |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置结构化文档标签的颜色。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setLockContentControl(boolean value)](#setLockContentControl-boolean-) | 当设置为 true 时，此属性将禁止用户删除此结构化文档标记。 |
| [setLockContents(boolean value)](#setLockContents-boolean-) | 当设置为 true 时，此属性将禁止用户编辑此结构化文档标记的内容。 |
| [setPlaceholderName(String value)](#setPlaceholderName-java.lang.String-) | 获取或设置名称[BuildingBlock](../../com.aspose.words/buildingblock)包含占位符文本。 |
| [setTag(String value)](#setTag-java.lang.String-) | 指定与当前结构化文档标签节点关联的标签。 |
| [setTitle(String value)](#setTitle-java.lang.String-) | 指定与此结构化文档标记关联的友好名称。 |
| [structuredDocumentTagNode()](#structuredDocumentTagNode--) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### StructuredDocumentTagRangeStart(DocumentBase doc, int type) {#StructuredDocumentTagRangeStart-com.aspose.words.DocumentBase-int-}
```
public StructuredDocumentTagRangeStart(DocumentBase doc, int type)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| doc | [DocumentBase](../../com.aspose.words/documentbase) |  |
| type | int |  |

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
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) |  |

**退货:**
布尔值
### appendChild(Node newChild) {#appendChild-com.aspose.words.Node-}
```
public Node appendChild(Node newChild)
```


将指定节点添加到 stdContent 范围的末尾。

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
### getChildNodes() {#getChildNodes--}
```
public NodeCollection getChildNodes()
```


获取此范围开始节点和范围结束节点之间的所有节点。

**退货:**
[NodeCollection](../../com.aspose.words/nodecollection) - 此范围开始节点和范围结束节点之间的所有节点。
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
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


获取该节点所属的文档。

该节点始终属于一个文档，即使它刚刚创建但尚未添加到树中，或者已从树中删除。

**退货:**
[DocumentBase](../../com.aspose.words/documentbase) - 该节点所属的文档。
### getId() {#getId--}
```
public int getId()
```


为此结构化文档标签指定一个唯一的只读持久数字 ID。

id 属性应遵循以下规则：

 *  仅当整个文档被克隆时，文档才应保留结构化文档标签 ID[Document.deepClone()](../../com.aspose.words/document\#deepClone--).
 *  期间[DocumentBase.importNode(com.aspose.words.Node, boolean)](../../com.aspose.words/documentbase\#importNode-com.aspose.words.Node--boolean-)如果导入不会与目标文档中的其他结构化文档标签 Id 发生冲突，则应保留 Id。
 *  如果多个结构化文档标签节点为 Id 属性指定了相同的十进制数值，则文档中的第一个结构化文档标签应保持此原始 Id，并且所有后续结构化文档标签节点应在文档被分配时分配新的标识符。加载。
 *  在独立结构化文档标签期间**M:Aspose.Words.Markup.StructuredDocumentTag.Clone(System.Boolean,Aspose.Words.INodeCloningListener)**操作将为克隆的结构化文档标签节点生成新的唯一 ID。
 *  如果在源文档中没有指定 Id，则结构化文档标签节点应在加载文档时分配一个新的唯一标识符。

**退货:**
int - 对应的 int 值。
### getLastChild() {#getLastChild--}
```
public Node getLastChild()
```


获取 stdContent 范围中的最后一个子项。如果没有最后一个子节点，则返回 null。

**退货:**
[Node](../../com.aspose.words/node) - stdContent 范围内的最后一个子项。
### getLevel() {#getLevel--}
```
public int getLevel()
```


获取此结构化文档标记范围开始出现在文档树中的级别。

**退货:**
 int - 此结构化文档标记范围开始出现在文档树中的级别。返回值是以下之一[MarkupLevel](../../com.aspose.words/markuplevel)常数。
### getLockContentControl() {#getLockContentControl--}
```
public boolean getLockContentControl()
```


当设置为 true 时，此属性将禁止用户删除此结构化文档标记。

**退货:**
boolean - 对应的布尔值。
### getLockContents() {#getLockContents--}
```
public boolean getLockContents()
```


当设置为 true 时，此属性将禁止用户编辑此结构化文档标记的内容。

**退货:**
boolean - 对应的布尔值。
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


获取此节点的类型。

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
### getPlaceholder() {#getPlaceholder--}
```
public BuildingBlock getPlaceholder()
```


获取[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此结构化文档标记运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-)元素为真。可以为 null，表示占位符不适用于此结构化文档标签。

**退货:**
[BuildingBlock](../../com.aspose.words/buildingblock) - 这[BuildingBlock](../../com.aspose.words/buildingblock)包含应在此结构化文档标记运行内容为空时显示的占位符文本，关联的映射 XML 元素为空，如通过[getXmlMapping()](../../com.aspose.words/structureddocumenttagrangestart\#getXmlMapping--)元素或[isShowingPlaceholderText()](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText--) / [isShowingPlaceholderText(boolean)](../../com.aspose.words/structureddocumenttagrangestart\#isShowingPlaceholderText-boolean-)元素为真。
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
### getRangeEnd() {#getRangeEnd--}
```
public StructuredDocumentTagRangeEnd getRangeEnd()
```


如果 StructuredDocumentTag 是范围结构化文档标记，则指定范围结束。否则返回 null。

**退货:**
[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) - 相应的[StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend)价值。
### getSdt类型() {#getSdt类型--}
```
public int getSdt类型()
```


获取此结构化文档标签的类型。

**退货:**
 int - 此结构化文档标签的类型。返回值是以下之一[Sdt类型](../../com.aspose.words/sdttype)常数。
### getTag() {#getTag--}
```
public String getTag()
```


指定与当前结构化文档标签节点关联的标签。不能为空。标签是任意字符串，应用程序可以将其与结构化文档标签相关联，以便在不提供可见友好名称的情况下对其进行识别。

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


指定与此结构化文档标记关联的友好名称。不能为空。

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


获取一个对象，该对象表示此结构化文档标记范围到当前文档的自定义 XML 部分中的 XML 数据的映射。您可以使用[XmlMapping.setMapping(com.aspose.words.CustomXmlPart, java.lang.String, java.lang.String)](../../com.aspose.words/xmlmapping\#setMapping-com.aspose.words.CustomXmlPart--java.lang.String--java.lang.String-)此对象的方法将结构化文档标记范围映射到 XML 数据。

**退货:**
[XmlMapping](../../com.aspose.words/xmlmapping) 表示此结构化文档标记范围到当前文档的自定义 XML 部分中的 XML 数据的映射的对象。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


如果此节点可以包含其他节点，则返回 true。 (31110,6)

**退货:**
boolean - 如果此节点可以包含其他节点，则为真。
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


指定是否应将此结构化文档标签的内容解释为包含占位符文本（与结构化文档标签内的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

**退货:**
boolean - 对应的布尔值。
### isShowingPlaceholderText(boolean value) {#isShowingPlaceholderText-boolean-}
```
public void isShowingPlaceholderText(boolean value)
```


指定是否应将此结构化文档标签的内容解释为包含占位符文本（与结构化文档标签内的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

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


删除此范围开始节点和范围结束节点之间的所有节点。

### removeSelfOnly() {#removeSelfOnly--}
```
public void removeSelfOnly()
```


删除结构化文档标记的此范围开始和适当范围结束节点，但将其内容保留在文档树内。

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

### setLockContentControl(boolean value) {#setLockContentControl-boolean-}
```
public void setLockContentControl(boolean value)
```


当设置为 true 时，此属性将禁止用户删除此结构化文档标记。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setLockContents(boolean value) {#setLockContents-boolean-}
```
public void setLockContents(boolean value)
```


当设置为 true 时，此属性将禁止用户编辑此结构化文档标记的内容。

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

### setTag(String value) {#setTag-java.lang.String-}
```
public void setTag(String value)
```


指定与当前结构化文档标签节点关联的标签。不能为空。标签是任意字符串，应用程序可以将其与结构化文档标签相关联，以便在不提供可见友好名称的情况下对其进行识别。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


指定与此结构化文档标记关联的友好名称。不能为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

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
