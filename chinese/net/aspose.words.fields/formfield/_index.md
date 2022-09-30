---
title: FormField
second_title: Aspose.Words for .NET API 参考
description: 表示单个表单域
type: docs
weight: 2460
url: /zh/net/aspose.words.fields/formfield/
---
## FormField class

表示单个表单域。

```csharp
public class FormField : SpecialChar
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | 如果对指定表单字段的引用在退出字段时自动更新，则为真。 |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | 获取或设置复选框的大小（以磅为单位）。仅在以下情况下生效[`IsCheckBoxExactSize`](./ischeckboxexactsize/)是真的。 |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | 获取或设置复选框表单域的选中状态。 该属性的默认值为 **错误的**. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | 获取或设置复选框表单域的默认值。 该属性的默认值为 **错误的**. |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | 提供对下拉表单字段项目的访问。 |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | 获取或设置在下拉表单字段中指定当前选定项的索引。 |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | 如果启用了表单字段，则为真。 |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | 返回或设置表单域的入口宏名称。 |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | 返回或设置表单域的退出宏名称。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | 返回或设置当表单域获得焦点并且用户按下 F1 时显示在消息框中的文本。 |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | 获取或设置指示文本框大小是自动还是明确指定的布尔值。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 如果此节点可以包含其他节点，则返回 true。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果启用更改跟踪时在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪时将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回 **真的**如果启用更改跟踪时此对象在 Microsoft Word 中被移动（删除）。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回 **真的**如果启用更改跟踪时在 Microsoft Word 中移动（插入）此对象。 |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | 文本字段的最大长度。长度不限时为零。 |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | 获取或设置表单字段名称。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧跟此节点的节点。 |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | 返回 **NodeType.FormField**. |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | 指定当表单域获得焦点并且用户按下 F1 时消息框中显示的文本的来源。 |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | 指定表单域获得焦点时在状态栏中显示的文本的来源。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph/)这个节点的. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧接在此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个 **范围**表示此节点中包含的文档部分的对象。 |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | 获取或设置表示此表单域结果的字符串。 |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | 返回或设置表单域获得焦点时在状态栏中显示的文本。 |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | 获取或设置文本表单域的默认字符串或计算表达式。 |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | 返回或设置文本表单域的文本格式。 |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | 获取或设置文本表单域的类型。 |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | 返回表单字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(DocumentVisitor) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| override [GetText](../../aspose.words/specialchar/gettext/)() | 获取此节点代表的特殊字符。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据前序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父级中移除自身。 |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | 删除完整的表单域，而不仅仅是表单域特殊字符。 |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(object) | 应用指定的文本格式[`TextInputFormat`](./textinputformat/)并将值存储在[`Result`](./result/). |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出为字符串。 |

### 评论

Microsoft Word 提供以下表单域：复选框、文本输入和下拉列表（组合框）。

**表单域**是一个内联节点，只能是 **段落**.

**表单域**在文档中由一个特殊字符和 表示为一行文本中的一个字符。

Word文档中一个完整的表单域是一个复杂的结构，由几个 个节点表示：域开始、FORMTEXT等域代码、表单域数据、域分隔符、 域结果、域结束和书签。以编程方式在 Word 文档中创建表单域 use [`DocumentBuilder.InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/), [`DocumentBuilder.InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/)和 [`DocumentBuilder.InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) which 确保所有表单字段节点都以正确的顺序和合适的状态创建。

### 例子

显示如何格式化整个 FormField，包括字段值。

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[0];
formField.Font.Bold = true;
formField.Font.Size = 24;
formField.Font.Color = Color.Red;

formField.Result = "Aspose.FormField";

doc = DocumentHelper.SaveOpen(doc);

Run formFieldRun = doc.FirstSection.Body.FirstParagraph.Runs[1];

Assert.AreEqual("Aspose.FormField", formFieldRun.Text);
Assert.AreEqual(true, formFieldRun.Font.Bold);
Assert.AreEqual(24, formFieldRun.Font.Size);
Assert.AreEqual(Color.Red.ToArgb(), formFieldRun.Font.Color.ToArgb());
```

显示如何插入组合框。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// 表单域将以“select”html标签的形式出现。
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### 也可以看看

* class [SpecialChar](../../aspose.words/specialchar/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
