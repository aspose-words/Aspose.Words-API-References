---
title: FormField Class
linktitle: FormField
articleTitle: FormField
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FormField 类，轻松创建和管理文档中的可自定义表单字段，以增强用户交互。
type: docs
weight: 3030
url: /zh/net/aspose.words.fields/formfield/
---
## FormField class

代表单个表单字段。

要了解更多信息，请访问[使用表单字段](https://docs.aspose.com/words/net/working-with-form-fields/)文档文章。

```csharp
public class FormField : SpecialChar
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | 如果在退出指定表单字段时自动更新对字段的引用，则为 True。 |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | 获取或设置复选框的大小（以磅为单位）。仅在以下情况下有效：[`IsCheckBoxExactSize`](./ischeckboxexactsize/)是`真的`. |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | 获取或设置复选框表单字段的选中状态。 此属性的默认值为`错误的`. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | 获取或设置复选框表单字段的默认值。 此属性的默认值为`错误的`. |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | 提供对下拉表单字段项目的访问。 |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | 获取或设置指定下拉表单字段中当前选定项的索引。 |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | 如果表单字段已启用，则为真。 |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | 返回或设置表单字段的入口宏名称。 |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | 返回或设置表单字段的退出宏名称。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | 返回或设置当表单字段具有焦点并且用户按下 F1 时显示在消息框中的文本。 |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | 获取或设置布尔值，指示文本框的大小是自动的还是明确指定的。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果此节点可以包含其他节点。 |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下 Microsoft Word 中的对象格式发生更改，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | 文本字段的最大长度。长度不受限制时，为零。 |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | 获取或设置表单字段名称。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | 返回FormField. |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | 指定当表单字段具有焦点并且用户按下 F1 时显示在消息框中的文本的来源。 |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | 指定当表单字段具有焦点时在状态栏中显示的文本的来源。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | 获取或设置表示此表单字段结果的字符串。 |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | 返回或设置当表单字段具有焦点时在状态栏中显示的文本。 |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | 获取或设置文本表单字段的默认字符串或计算表达式。 |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | 返回或设置文本表单字段的文本格式。 |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | 获取或设置文本表单字段的类型。 |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | 返回表单字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| override [GetText](../../aspose.words/specialchar/gettext/)() | 获取此节点代表的特殊字符。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | 删除整个表单字段，而不仅仅是表单字段特殊字符。 |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(*object*) | 应用指定的文本格式[`TextInputFormat`](./textinputformat/)并将值存储在[`Result`](./result/). |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

Microsoft Word 提供以下表单字段：复选框、文本输入和下拉菜单（组合框）。

`FormField`是内联节点，并且只能是[`Paragraph`](../../aspose.words/paragraph/)。

`FormField`在文档中用特殊字符 and 表示，该字符位于文本行内的字符内。

Word 文档中完整的表单字段是一个复杂的结构，由多个 节点表示：字段起始、字段代码（例如 FORMTEXT）、表单字段数据、字段分隔符、 字段结果、字段结束和一个书签。要以编程方式在 Word 文档中创建表单字段，请使用 [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/), [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/)and [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/)which 确保所有表单字段节点都按照正确的顺序并处于合适的状态创建。

## 例子

展示如何格式化整个 FormField，包括字段值。

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

// 表单字段将以“select”html标签的形式出现。
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### 也可以看看

* class [SpecialChar](../../aspose.words/specialchar/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
