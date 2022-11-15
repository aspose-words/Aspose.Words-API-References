---
title: FormField
second_title: Aspose.Words for Java API 参考
description: 表示单个表单字段。
type: docs
weight: 296
url: /zh/java/com.aspose.words/formfield/
---

**遗产：**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.Inline](../../com.aspose.words/inline), [com.aspose.words.SpecialChar](../../com.aspose.words/specialchar)
```
public class FormField extends SpecialChar
```

表示单个表单字段。

要了解更多信息，请访问**Working with Form Fields**文档文章。

Microsoft Word 提供以下表单域：复选框、文本输入和下拉列表（组合框）。

**FormField**是一个内联节点，只能是**Paragraph**.

**FormField**在文档中由一个特殊字符表示，并定位为一行文本中的一个字符。

Word文档中一个完整的表单域是一个复杂的结构，由几个节点表示：域开始、域代码如FORMTEXT、表单域数据、域分隔符、域结果、域结束和一个书签。要以编程方式在 Word 文档中创建表单域，请使用[DocumentBuilder.insertCheckBox(java.lang.String, boolean, int)](../../com.aspose.words/documentbuilder\#insertCheckBox-java.lang.String--boolean--int-), **M:Aspose.Words.DocumentBuilder.InsertTextInput(System.String,Aspose.Words.Fields.TextFormFieldType,System.String,System.String,System.Int32)**和[DocumentBuilder.insertComboBox(java.lang.String, java.lang.String[], int)](../../com.aspose.words/documentbuilder\#insertComboBox-java.lang.String--java.lang.String----int-)这确保所有表单字段节点都以正确的顺序和适当的状态创建。
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
| [getCalculateOnExit()](#getCalculateOnExit--) | 如果在退出该字段时自动更新对指定表单字段的引用，则为真。 |
| [getCheckBoxSize()](#getCheckBoxSize--) | 获取复选框的大小（以磅为单位）。 |
| [getChecked()](#getChecked--) | 获取复选框表单域的选中状态。 |
| [getClass()](#getClass--) |  |
| [getCustomNodeId()](#getCustomNodeId--) | 指定自定义节点标识符。 |
| [getDefault()](#getDefault--) | 获取复选框表单域的默认值。 |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) | 获取此节点所属的文档。 |
| [getDocument_IInline()](#getDocument-IInline--) |  |
| [getDropDownItems()](#getDropDownItems--) | 提供对下拉表单字段项目的访问。 |
| [getDropDownSelectedIndex()](#getDropDownSelectedIndex--) | 获取指定下拉表单字段中当前选定项目的索引。 |
| [getEnabled()](#getEnabled--) | 如果启用了表单域，则为真。 |
| [getEntryMacro()](#getEntryMacro--) | 获取表单域的入口宏名称。 |
| [getExitMacro()](#getExitMacro--) | 获取表单域的退出宏名称。 |
| [getFont()](#getFont--) | 提供对此对象的字体格式的访问。 |
| [getHelpText()](#getHelpText--) | 获取当表单域具有焦点并且用户按下 F1 时消息框中显示的文本。 |
| [getMaxLength()](#getMaxLength--) | 文本字段的最大长度。 |
| [getName()](#getName--) | 获取表单域名称。 |
| [getNextSibling()](#getNextSibling--) | 获取紧跟在该节点之后的节点。 |
| [getNodeType()](#getNodeType--) | 退货**NodeType.FormField**. |
| [getOwnHelp()](#getOwnHelp--) | 指定当表单域具有焦点并且用户按 F1 时消息框中显示的文本的来源。 |
| [getOwnStatus()](#getOwnStatus--) | 指定当表单域具有焦点时状态栏中显示的文本的来源。 |
| [getParentNode()](#getParentNode--) | 获取此节点的直接父级。 |
| [getParentParagraph()](#getParentParagraph--) | 检索父级[Paragraph](../../com.aspose.words/paragraph)这个节点的。 |
| [getParentParagraph_IInline()](#getParentParagraph-IInline--) |  |
| [getPreviousSibling()](#getPreviousSibling--) | 获取紧接在该节点之前的节点。 |
| [getRange()](#getRange--) | 返回一个**Range**表示包含在该节点中的文档部分的对象。 |
| [getResult()](#getResult--) | 获取表示此表单域结果的字符串。 |
| [getStatusText()](#getStatusText--) | 获取当表单域具有焦点时状态栏中显示的文本。 |
| [getText()](#getText--) | 获取此节点表示的特殊字符。 |
| [getTextInputDefault()](#getTextInputDefault--) | 获取文本表单域的默认字符串或计算表达式。 |
| [getTextInputFormat()](#getTextInputFormat--) | 获取文本表单域的文本格式。 |
| [getTextInputType()](#getTextInputType--) | 获取文本表单域的类型。 |
| [getType()](#getType--) | 返回表单字段类型。 |
| [hashCode()](#hashCode--) |  |
| [isCheckBoxExactSize()](#isCheckBoxExactSize--) | 获取布尔值，该值指示文本框的大小是自动的还是显式指定的。 |
| [isCheckBoxExactSize(boolean value)](#isCheckBoxExactSize-boolean-) | 设置布尔值，指示文本框的大小是自动的还是明确指定的。 |
| [isComposite()](#isComposite--) | 如果此节点可以包含其他节点，则返回 true。 |
| [isDeleteRevision()](#isDeleteRevision--) | 如果启用更改跟踪时此对象在 Microsoft Word 中被删除，则返回 true。 |
| [isFormatRevision()](#isFormatRevision--) | 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [isInsertRevision()](#isInsertRevision--) | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [isMoveFromRevision()](#isMoveFromRevision--) | 退货**true**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [isMoveToRevision()](#isMoveToRevision--) | 退货**true**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取下一个节点。 |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node-) | 根据前序树遍历算法获取上一个节点。 |
| [remove()](#remove--) | 从父级中移除自身。 |
| [removeField()](#removeField--) | 删除整个表单域，而不仅仅是表单域特殊字符。 |
| [removeMoveRevisions()](#removeMoveRevisions--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setCalculateOnExit(boolean value)](#setCalculateOnExit-boolean-) | 如果在退出该字段时自动更新对指定表单字段的引用，则为真。 |
| [setCheckBoxSize(double value)](#setCheckBoxSize-double-) | 以磅为单位设置复选框的大小。 |
| [setChecked(boolean value)](#setChecked-boolean-) | 设置复选框表单域的选中状态。 |
| [setCustomNodeId(int value)](#setCustomNodeId-int-) | 指定自定义节点标识符。 |
| [setDefault(boolean value)](#setDefault-boolean-) | 设置复选框表单域的默认值。 |
| [setDropDownSelectedIndex(int value)](#setDropDownSelectedIndex-int-) | 设置指定下拉表单字段中当前所选项目的索引。 |
| [setEnabled(boolean value)](#setEnabled-boolean-) | 如果启用了表单域，则为真。 |
| [setEntryMacro(String value)](#setEntryMacro-java.lang.String-) | 为表单字段设置条目宏名称。 |
| [setExitMacro(String value)](#setExitMacro-java.lang.String-) | 为表单字段设置退出宏名称。 |
| [setHelpText(String value)](#setHelpText-java.lang.String-) | 设置当表单域具有焦点并且用户按下 F1 时消息框中显示的文本。 |
| [setMaxLength(int value)](#setMaxLength-int-) | 文本字段的最大长度。 |
| [setName(String value)](#setName-java.lang.String-) | 设置表单字段名称。 |
| [setOwnHelp(boolean value)](#setOwnHelp-boolean-) | 指定当表单域具有焦点并且用户按 F1 时消息框中显示的文本的来源。 |
| [setOwnStatus(boolean value)](#setOwnStatus-boolean-) | 指定当表单域具有焦点时状态栏中显示的文本的来源。 |
| [setResult(String value)](#setResult-java.lang.String-) | 设置表示此表单域结果的字符串。 |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStatusText(String value)](#setStatusText-java.lang.String-) | 设置当表单域具有焦点时状态栏中显示的文本。 |
| [setTextInputDefault(String value)](#setTextInputDefault-java.lang.String-) | 设置文本表单域的默认字符串或计算表达式。 |
| [setTextInputFormat(String value)](#setTextInputFormat-java.lang.String-) | 设置文本表单域的文本格式。 |
| [setTextInputType(int value)](#setTextInputType-int-) | 设置文本表单字段的类型。 |
| [setTextInputValue(Object newValue)](#setTextInputValue-java.lang.Object-) | 应用指定的文本格式[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-)并将值存储在[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-). |
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

调用 DocumentVisitor.VisitFormField。

有关更多信息，请参阅访问者设计模式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | 将访问节点的访问者。 |

**退货：**
boolean - 如果访问者请求停止枚举，则为 False。
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
### getCalculateOnExit() {#getCalculateOnExit--}
```
public boolean getCalculateOnExit()
```


如果在退出该字段时自动更新对指定表单字段的引用，则为真。

环境**CalculateOnExit**仅影响在 Microsoft Word 中打开文档时表单域的行为。 Aspose.Words 从不更新对表单字段的引用。

**退货：**
boolean - 相应的布尔值。
### getCheckBoxSize() {#getCheckBoxSize--}
```
public double getCheckBoxSize()
```


获取复选框的大小（以磅为单位）。只有当[isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-)是真的。

仅适用于复选框表单域。

**退货：**
double - 复选框的大小（以磅为单位）。
### getChecked() {#getChecked--}
```
public boolean getChecked()
```


获取复选框表单域的选中状态。此属性的默认值为**false**.

仅适用于复选框表单域。

**退货：**
boolean - 复选框表单域的选中状态。
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
### getDefault() {#getDefault--}
```
public boolean getDefault()
```


获取复选框表单域的默认值。此属性的默认值为**false**.

仅适用于复选框表单域。

**退货：**
boolean - 复选框表单字段的默认值。
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
### getDropDownItems() {#getDropDownItems--}
```
public DropDownItemCollection getDropDownItems()
```


提供对下拉表单字段项目的访问。

Microsoft Word 允许下拉表单字段中最多有 25 个项目。

**退货：**
[DropDownItemCollection](../../com.aspose.words/dropdownitemcollection) - 相应的[DropDownItemCollection](../../com.aspose.words/dropdownitemcollection)价值。
### getDropDownSelectedIndex() {#getDropDownSelectedIndex--}
```
public int getDropDownSelectedIndex()
```


获取指定下拉表单字段中当前选定项目的索引。

**退货：**
int - 指定下拉表单字段中当前选定项目的索引。
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


如果启用了表单域，则为真。

如果启用了表单字段，则可以在填写表单时更改其内容。

**退货：**
boolean - 相应的布尔值。
### getEntryMacro() {#getEntryMacro--}
```
public String getEntryMacro()
```


获取表单域的入口宏名称。

当表单域在 Microsoft Word 中获得焦点时，入口宏就会运行。

Microsoft Word 允许最多包含 32 个字符的字符串。

**退货：**
java.lang.String - 表单字段的条目宏名称。
### getExitMacro() {#getExitMacro--}
```
public String getExitMacro()
```


获取表单域的退出宏名称。

当表单域在 Microsoft Word 中失去焦点时，退出宏就会运行。

Microsoft Word 允许最多包含 32 个字符的字符串。

**退货：**
java.lang.String - 表单字段的退出宏名称。
### getFont() {#getFont--}
```
public Font getFont()
```


提供对此对象的字体格式的访问。

**退货：**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getHelpText() {#getHelpText--}
```
public String getHelpText()
```


获取当表单域具有焦点并且用户按下 F1 时消息框中显示的文本。

如果 OwnHelp 属性设置为 True，则 HelpText 指定文本字符串值。如果 OwnHelp 设置为 False，HelpText 指定包含表单域帮助文本的自动图文集条目的名称。

Microsoft Word 允许最多包含 255 个字符的字符串。

**退货：**
java.lang.String - 当表单域获得焦点并且用户按下 F1 时在消息框中显示的文本。
### getMaxLength() {#getMaxLength--}
```
public int getMaxLength()
```


文本字段的最大长度。长度不受限制时为零。

**退货：**
int - 相应的 int 值。
### getName() {#getName--}
```
public String getName()
```


获取表单域名称。 Microsoft Word 允许最多包含 20 个字符的字符串。

**退货：**
java.lang.String - 表单字段名称。
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


退货**NodeType.FormField**.

**退货：**
整数 -**NodeType.FormField** .返回值是其中之一[NodeType](../../com.aspose.words/nodetype)常数。
### getOwnHelp() {#getOwnHelp--}
```
public boolean getOwnHelp()
```


指定当表单域具有焦点并且用户按 F1 时消息框中显示的文本的来源。

如果为 True，则显示 HelpText 属性指定的文本。如果为 False，则显示 HelpText 属性指定的自动图文集条目中的文本。

**退货：**
boolean - 相应的布尔值。
### getOwnStatus() {#getOwnStatus--}
```
public boolean getOwnStatus()
```


指定当表单域具有焦点时状态栏中显示的文本的来源。

如果为真，则显示 StatusText 属性指定的文本。如果为 false，则显示 StatusText 属性指定的自动图文集条目的文本。

**退货：**
boolean - 相应的布尔值。
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
### getResult() {#getResult--}
```
public String getResult()
```


获取表示此表单域结果的字符串。

对于文本表单字段，结果是字段中的文本。

对于复选框表单字段，结果可以是“1”或“0”以指示选中或未选中。

对于下拉表单字段，结果是在下拉列表中选择的字符串。

环境[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-)对于文本表单域不应用指定的文本格式[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-).如果要设置值并应用格式，请使用[setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield\#setTextInputValue-java.lang.Object-)方法。

对于文本表单字段[getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-)如果值为 null 则应用值。

**退货：**
java.lang.String - 表示此表单字段结果的字符串。
### getStatusText() {#getStatusText--}
```
public String getStatusText()
```


获取当表单域具有焦点时状态栏中显示的文本。

如果 OwnStatus 属性设置为 true，则 StatusText 属性指定状态栏文本。如果 OwnStatus 属性设置为 false，则 StatusText 属性指定包含表单域状态栏文本的自动图文集条目的名称。

Microsoft Word 允许最多包含 138 个字符的字符串。

**退货：**
java.lang.String - 当表单域获得焦点时在状态栏中显示的文本。
### getText() {#getText--}
```
public String getText()
```


获取此节点表示的特殊字符。

**退货：**
java.lang.String - 包含此节点表示的字符的字符串。
### getTextInputDefault() {#getTextInputDefault--}
```
public String getTextInputDefault()
```


获取文本表单域的默认字符串或计算表达式。

该属性的含义取决于[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-)财产。

什么时候[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-)是[TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype\#REGULAR)或者[TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype\#NUMBER)此字符串指定文本表单字段的默认字符串。该字符串是当表单域为空时 Microsoft Word 将在文档中显示的内容。

什么时候[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-)是[TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype\#CALCULATED), 然后这个字符串包含要计算的表达式。表达式需要是根据 Microsoft Word 公式字段要求有效的公式。当您使用该属性设置一个新表达式时，Aspose.Words 会自动计算公式结果并将其插入到表单域中。

Microsoft Word 允许最多包含 255 个字符的字符串。

**退货：**
java.lang.String - 文本表单域的默认字符串或计算表达式。
### getTextInputFormat() {#getTextInputFormat--}
```
public String getTextInputFormat()
```


获取文本表单域的文本格式。

如果文本表单字段包含常规文本，则有效格式字符串为“”、“UPPERCASE”、“LOWERCASE”、“FIRST CAPITAL”和“TITLE CASE”。字符串不区分大小写。

如果文本表单字段包含数字或日期/时间值，则有效格式字符串为数字或日期和时间格式字符串。

Microsoft Word 允许最多包含 64 个字符的字符串。

**退货：**
java.lang.String - 文本表单域的文本格式。
### getTextInputType() {#getTextInputType--}
```
public int getTextInputType()
```


获取文本表单域的类型。

**退货：**
 int - 文本表单字段的类型。返回值是其中之一[TextFormFieldType](../../com.aspose.words/textformfieldtype)常数。
### getType() {#getType--}
```
public int getType()
```


返回表单字段类型。

**退货：**
int - 表单字段类型。返回值是其中之一[FieldType](../../com.aspose.words/fieldtype)常数。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isCheckBoxExactSize() {#isCheckBoxExactSize--}
```
public boolean isCheckBoxExactSize()
```


获取布尔值，该值指示文本框的大小是自动的还是显式指定的。

仅适用于复选框表单域。

**退货：**
boolean - 布尔值，指示文本框的大小是自动的还是明确指定的。
### isCheckBoxExactSize(boolean value) {#isCheckBoxExactSize-boolean-}
```
public void isCheckBoxExactSize(boolean value)
```


设置布尔值，指示文本框的大小是自动的还是明确指定的。

仅适用于复选框表单域。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 布尔值，指示文本框的大小是自动的还是明确指定的。 |

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

### removeField() {#removeField--}
```
public void removeField()
```


删除整个表单域，而不仅仅是表单域特殊字符。如果存在与表单域关联的书签，则不会删除该书签。

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

### setCalculateOnExit(boolean value) {#setCalculateOnExit-boolean-}
```
public void setCalculateOnExit(boolean value)
```


如果在退出该字段时自动更新对指定表单字段的引用，则为真。

环境**CalculateOnExit**仅影响在 Microsoft Word 中打开文档时表单域的行为。 Aspose.Words 从不更新对表单字段的引用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCheckBoxSize(double value) {#setCheckBoxSize-double-}
```
public void setCheckBoxSize(double value)
```


以磅为单位设置复选框的大小。只有当[isCheckBoxExactSize()](../../com.aspose.words/formfield\#isCheckBoxExactSize--) / [isCheckBoxExactSize(boolean)](../../com.aspose.words/formfield\#isCheckBoxExactSize-boolean-)是真的。

仅适用于复选框表单域。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 复选框的大小（以磅为单位）。 |

### setChecked(boolean value) {#setChecked-boolean-}
```
public void setChecked(boolean value)
```


设置复选框表单域的选中状态。此属性的默认值为**false**.

仅适用于复选框表单域。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 复选框表单域的选中状态。 |

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

### setDefault(boolean value) {#setDefault-boolean-}
```
public void setDefault(boolean value)
```


设置复选框表单域的默认值。此属性的默认值为**false**.

仅适用于复选框表单域。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 复选框表单域的默认值。 |

### setDropDownSelectedIndex(int value) {#setDropDownSelectedIndex-int-}
```
public void setDropDownSelectedIndex(int value)
```


设置指定下拉表单字段中当前所选项目的索引。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 指定下拉表单字段中当前选定项目的索引。 |

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


如果启用了表单域，则为真。

如果启用了表单字段，则可以在填写表单时更改其内容。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setEntryMacro(String value) {#setEntryMacro-java.lang.String-}
```
public void setEntryMacro(String value)
```


为表单字段设置条目宏名称。

当表单域在 Microsoft Word 中获得焦点时，入口宏就会运行。

Microsoft Word 允许最多包含 32 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 表单域的入口宏名称。 |

### setExitMacro(String value) {#setExitMacro-java.lang.String-}
```
public void setExitMacro(String value)
```


为表单字段设置退出宏名称。

当表单域在 Microsoft Word 中失去焦点时，退出宏就会运行。

Microsoft Word 允许最多包含 32 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 表单域的退出宏名称。 |

### setHelpText(String value) {#setHelpText-java.lang.String-}
```
public void setHelpText(String value)
```


设置当表单域具有焦点并且用户按下 F1 时消息框中显示的文本。

如果 OwnHelp 属性设置为 True，则 HelpText 指定文本字符串值。如果 OwnHelp 设置为 False，HelpText 指定包含表单域帮助文本的自动图文集条目的名称。

Microsoft Word 允许最多包含 255 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 当表单域获得焦点并且用户按 F1 时，消息框中显示的文本。 |

### setMaxLength(int value) {#setMaxLength-int-}
```
public void setMaxLength(int value)
```


文本字段的最大长度。长度不受限制时为零。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置表单字段名称。 Microsoft Word 允许最多包含 20 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 表单字段名称。 |

### setOwnHelp(boolean value) {#setOwnHelp-boolean-}
```
public void setOwnHelp(boolean value)
```


指定当表单域具有焦点并且用户按 F1 时消息框中显示的文本的来源。

如果为 True，则显示 HelpText 属性指定的文本。如果为 False，则显示 HelpText 属性指定的自动图文集条目中的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setOwnStatus(boolean value) {#setOwnStatus-boolean-}
```
public void setOwnStatus(boolean value)
```


指定当表单域具有焦点时状态栏中显示的文本的来源。

如果为真，则显示 StatusText 属性指定的文本。如果为 false，则显示 StatusText 属性指定的自动图文集条目的文本。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


设置表示此表单域结果的字符串。

对于文本表单字段，结果是字段中的文本。

对于复选框表单字段，结果可以是“1”或“0”以指示选中或未选中。

对于下拉表单字段，结果是在下拉列表中选择的字符串。

环境[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-)对于文本表单域不应用指定的文本格式[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-).如果要设置值并应用格式，请使用[setTextInputValue(java.lang.Object)](../../com.aspose.words/formfield\#setTextInputValue-java.lang.Object-)方法。

对于文本表单字段[getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-)如果值为 null 则应用值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 表示此表单字段结果的字符串。 |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStatusText(String value) {#setStatusText-java.lang.String-}
```
public void setStatusText(String value)
```


设置当表单域具有焦点时状态栏中显示的文本。

如果 OwnStatus 属性设置为 true，则 StatusText 属性指定状态栏文本。如果 OwnStatus 属性设置为 false，则 StatusText 属性指定包含表单域状态栏文本的自动图文集条目的名称。

Microsoft Word 允许最多包含 138 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 表单域具有焦点时状态栏中显示的文本。 |

### setTextInputDefault(String value) {#setTextInputDefault-java.lang.String-}
```
public void setTextInputDefault(String value)
```


设置文本表单域的默认字符串或计算表达式。

该属性的含义取决于[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-)财产。

什么时候[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-)是[TextFormFieldType.REGULAR](../../com.aspose.words/textformfieldtype\#REGULAR)或者[TextFormFieldType.NUMBER](../../com.aspose.words/textformfieldtype\#NUMBER)此字符串指定文本表单字段的默认字符串。该字符串是当表单域为空时 Microsoft Word 将在文档中显示的内容。

什么时候[getTextInputType()](../../com.aspose.words/formfield\#getTextInputType--) / [setTextInputType(int)](../../com.aspose.words/formfield\#setTextInputType-int-)是[TextFormFieldType.CALCULATED](../../com.aspose.words/textformfieldtype\#CALCULATED), 然后这个字符串包含要计算的表达式。表达式需要是根据 Microsoft Word 公式字段要求有效的公式。当您使用该属性设置一个新表达式时，Aspose.Words 会自动计算公式结果并将其插入到表单域中。

Microsoft Word 允许最多包含 255 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文本表单域的默认字符串或计算表达式。 |

### setTextInputFormat(String value) {#setTextInputFormat-java.lang.String-}
```
public void setTextInputFormat(String value)
```


设置文本表单域的文本格式。

如果文本表单字段包含常规文本，则有效格式字符串为“”、“UPPERCASE”、“LOWERCASE”、“FIRST CAPITAL”和“TITLE CASE”。字符串不区分大小写。

如果文本表单字段包含数字或日期/时间值，则有效格式字符串为数字或日期和时间格式字符串。

Microsoft Word 允许最多包含 64 个字符的字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文本表单域的文本格式。 |

### setTextInputType(int value) {#setTextInputType-int-}
```
public void setTextInputType(int value)
```


设置文本表单字段的类型。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 文本表单域的类型。该值必须是其中之一[TextFormFieldType](../../com.aspose.words/textformfieldtype)常数。 |

### setTextInputValue(Object newValue) {#setTextInputValue-java.lang.Object-}
```
public void setTextInputValue(Object newValue)
```


应用指定的文本格式[getTextInputFormat()](../../com.aspose.words/formfield\#getTextInputFormat--) / [setTextInputFormat(java.lang.String)](../../com.aspose.words/formfield\#setTextInputFormat-java.lang.String-)并将值存储在[getResult()](../../com.aspose.words/formfield\#getResult--) / [setResult(java.lang.String)](../../com.aspose.words/formfield\#setResult-java.lang.String-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newValue | java.lang.Object | 可以是字符串、数字或 DateTime 对象。这[getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-)如果 newValue 为 null 则应用该值。 |

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
