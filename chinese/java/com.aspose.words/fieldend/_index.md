---
title: FieldEnd
second_title: Aspose.Words for Java API 参考
description: 表示文档中 Word 字段的结尾。
type: docs
weight: 186
url: /zh/java/com.aspose.words/fieldend/
---

**遗产：**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar), [com.aspose.words.FieldChar](../../com.aspose.words/fieldchar)
```
public class FieldEnd extends FieldChar
```

表示文档中 Word 字段的结尾。

要了解更多信息，请访问**Working with Fields**文档文章。

[FieldEnd](../../com.aspose.words/fieldend)是一个内联级节点，由[ControlChar.FIELD\_END\_CHAR](../../com.aspose.words/controlchar\#FIELD-END-CHAR)文档中的控制字符。

[FieldEnd](../../com.aspose.words/fieldend)只能是孩子[Paragraph](../../com.aspose.words/paragraph).

Microsoft Word 文档中的完整字段是由字段起始字符、字段代码、字段分隔符、字段结果和字段结束字符组成的复杂结构。有些字段只有字段开始、字段代码和字段结束。

要轻松地将新字段插入文档，请使用[DocumentBuilder.insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-)方法。
## 方法

| 方法 | 描述 |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | 接待来访者。 |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [dd()](#dd--) |  |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean-) | 创建节点的副本。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [getAncestor(int ancestorType)](#getAncestor-int-) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class-) | 获取指定对象类型的第一个祖先。 |
| [getClass()](#getClass--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取此节点所属的文档。 |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getField()](#getField--) | 返回字段 char 的字段。 |
| [getFieldType()](#getFieldType--) | 返回字段的类型。 |
| [getFont()](#getFont--) | 提供对此对象的字体格式的访问。 |
| [getNextSibling()](#getNextSibling--) | 获取紧跟在该节点之后的节点。 |
| [getNodeType()](#getNodeType--) | 退货[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END). |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父级。 |
| [getParentParagraph()](#getParentParagraph--) | 检索父级[Paragraph](../../com.aspose.words/paragraph)这个节点的。 |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在该节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在该节点中的文档部分的对象。 |
| [getText()](#getText--) | 获取此节点表示的特殊字符。 |
| [hasSeparator()](#hasSeparator--) | 退货**true**如果此字段有分隔符。 |
| [hashCode()](#hashCode--) |  |
| [isComposite()](#isComposite--) | 如果此节点可以包含其他节点，则返回 true。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。 |
| [isDirty()](#isDirty--) | 获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isDirty(boolean value)](#isDirty-boolean-) | 设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [isFormatRevision()](#isFormatRevision--) | 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [isInsertRevision()](#isInsertRevision--) | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [isLocked()](#isLocked--) | 获取父字段是否已锁定（不应重新计算其结果）。 |
| [isLocked(boolean value)](#isLocked-boolean-) | 设置父字段是否被锁定（不应重新计算其结果）。 |
| [isMoveFromRevision()](#isMoveFromRevision--) | 退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [isMoveToRevision()](#isMoveToRevision--) | 退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions-) | 使用指定的保存选项将节点的内容导出为字符串。 |
| [toString(int saveFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


接待来访者。

来电[DocumentVisitor.visitFieldEnd(com.aspose.words.FieldEnd)](../../com.aspose.words/documentvisitor\#visitFieldEnd-com.aspose.words.FieldEnd-).

有关更多信息，请参阅访问者设计模式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货：**
布尔值 -**False**如果访问者请求枚举停止。
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
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
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
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |

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
### getDocument_IInline() {#getDocument-IInline--}
```
public DocumentBase getDocument_IInline()
```




**退货：**
[DocumentBase](../../com.aspose.words/documentbase)
### getField() {#getField--}
```
public Field getField()
```


返回字段 char 的字段。一个新的[Field](../../com.aspose.words/field)每次调用该方法时都会创建对象。

**退货：**
[Field](../../com.aspose.words/field) - 字段字符的字段。
### getFieldType() {#getFieldType--}
```
public int getFieldType()
```


返回字段的类型。

**退货：**
 int - 字段的类型。返回值是其中之一[FieldType](../../com.aspose.words/fieldtype)常数。
### getFont() {#getFont--}
```
public Font getFont()
```


提供对此对象的字体格式的访问。

**退货：**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
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


退货[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END).

**退货：**
整数 -\{[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END) .返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getParentNode() {#getParentNode--}
```
public CompositeNode getParentNode()
```


获取此节点的直接父级。

如果一个节点刚刚被创建并且还没有被添加到树中，或者如果它已经被从树中移除，则父节点为空。

**退货：**
[CompositeNode](../../com.aspose.words/compositenode) - 此节点的直接父节点。
### getParentParagraph() {#getParentParagraph--}
```
public Paragraph getParentParagraph()
```


检索父级[Paragraph](../../com.aspose.words/paragraph)这个节点的。

**退货：**
[Paragraph](../../com.aspose.words/paragraph) - 相应的[Paragraph](../../com.aspose.words/paragraph)价值。
### getParentParagraph_IInline() {#getParentParagraph-IInline--}
```
public Paragraph getParentParagraph_IInline()
```




**退货：**
[Paragraph](../../com.aspose.words/paragraph)
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
### getText() {#getText--}
```
public String getText()
```


获取此节点表示的特殊字符。

**退货：**
java.lang.String - 包含此节点表示的字符的字符串。
### hasSeparator() {#hasSeparator--}
```
public boolean hasSeparator()
```


退货**true**如果此字段有分隔符。

**退货：**
布尔值 -**true**如果此字段有分隔符。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isComposite() {#isComposite--}
```
public boolean isComposite()
```


如果此节点可以包含其他节点，则返回 true。 (31110,6)

**退货：**
boolean - 如果此节点可以包含其他节点则为真。
### isDeleteRevision() {#isDeleteRevision--}
```
public boolean isDeleteRevision()
```


如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则为 True。
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


获取字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。

**退货：**
布尔值 - 由于对文档进行的其他修改，该字段的当前结果是否不再正确（陈旧）。
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 由于对文档进行的其他修改，字段的当前结果是否不再正确（陈旧）。 |

### isFormatRevision() {#isFormatRevision--}
```
public boolean isFormatRevision()
```


如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则为 True。
### isInsertRevision() {#isInsertRevision--}
```
public boolean isInsertRevision()
```


如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。

**退货：**
布尔值 - 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则为 True。
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


获取父字段是否已锁定（不应重新计算其结果）。

**退货：**
boolean - 父字段是否被锁定（不应重新计算其结果）。
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


设置父字段是否被锁定（不应重新计算其结果）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 父字段是否被锁定（不应重新计算其结果）。 |

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

### removeMoveRevisions() {#removeMoveRevisions--}
```
public void removeMoveRevisions()
```




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |

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

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontAttr | int |  |
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
