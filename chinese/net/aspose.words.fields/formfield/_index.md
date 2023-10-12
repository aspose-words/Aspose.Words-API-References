---
title: Class FormField
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FormField 班级. 代表单个表单字段
type: docs
weight: 2620
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
| [CalculateOnExit](../../aspose.words.fields/formfield/calculateonexit/) { get; set; } | 如果每当退出指定表单字段时都会自动更新该字段的引用，则为 True。 |
| [CheckBoxSize](../../aspose.words.fields/formfield/checkboxsize/) { get; set; } | 获取或设置复选框的大小（以磅为单位）。仅当[`IsCheckBoxExactSize`](./ischeckboxexactsize/)是`真的`. |
| [Checked](../../aspose.words.fields/formfield/checked/) { get; set; } | 获取或设置复选框表单字段的选中状态。 该属性的默认值为`错误的`. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [Default](../../aspose.words.fields/formfield/default/) { get; set; } | 获取或设置复选框表单字段的默认值。 此属性的默认值为`错误的`. |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [DropDownItems](../../aspose.words.fields/formfield/dropdownitems/) { get; } | 提供对下拉表单字段的项目的访问。 |
| [DropDownSelectedIndex](../../aspose.words.fields/formfield/dropdownselectedindex/) { get; set; } | 获取或设置指定下拉表单字段中当前所选项目的索引。 |
| [Enabled](../../aspose.words.fields/formfield/enabled/) { get; set; } | 如果启用了表单字段，则为 True。 |
| [EntryMacro](../../aspose.words.fields/formfield/entrymacro/) { get; set; } | 返回或设置表单字段的条目宏名称。 |
| [ExitMacro](../../aspose.words.fields/formfield/exitmacro/) { get; set; } | 返回或设置表单字段的退出宏名称。 |
| [Font](../../aspose.words/inline/font/) { get; } | 提供对此对象的字体格式的访问。 |
| [HelpText](../../aspose.words.fields/formfield/helptext/) { get; set; } | 返回或设置当表单字段获得焦点并且用户按 F1 时消息框中显示的文本。 |
| [IsCheckBoxExactSize](../../aspose.words.fields/formfield/ischeckboxexactsize/) { get; set; } | 获取或设置布尔值，该值指示文本框的大小是自动还是显式指定。 |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | 返回`真的`如果该节点可以包含其他节点. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中更改了对象的格式，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | 返回`真的`如果启用更改跟踪时在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [MaxLength](../../aspose.words.fields/formfield/maxlength/) { get; set; } | 文本字段的最大长度。长度不受限制时为零。 |
| [Name](../../aspose.words.fields/formfield/name/) { get; set; } | 获取或设置表单字段名称。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words.fields/formfield/nodetype/) { get; } | 返回FormField. |
| [OwnHelp](../../aspose.words.fields/formfield/ownhelp/) { get; set; } | 指定当表单域获得焦点并且用户按 F1 时消息框中显示的文本来源。 |
| [OwnStatus](../../aspose.words.fields/formfield/ownstatus/) { get; set; } | 指定当表单字段获得焦点时状态栏中显示的文本来源。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | 检索父级[`Paragraph`](../../aspose.words/paragraph/)此节点的. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../../aspose.words/range/)表示此节点中包含的文档部分的对象。 |
| [Result](../../aspose.words.fields/formfield/result/) { get; set; } | 获取或设置表示此表单字段结果的字符串。 |
| [StatusText](../../aspose.words.fields/formfield/statustext/) { get; set; } | 返回或设置当表单字段获得焦点时状态栏中显示的文本。 |
| [TextInputDefault](../../aspose.words.fields/formfield/textinputdefault/) { get; set; } | 获取或设置文本表单字段的默认字符串或计算表达式。 |
| [TextInputFormat](../../aspose.words.fields/formfield/textinputformat/) { get; set; } | 返回或设置文本表单字段的文本格式。 |
| [TextInputType](../../aspose.words.fields/formfield/textinputtype/) { get; set; } | 获取或设置文本表单字段的类型。 |
| [Type](../../aspose.words.fields/formfield/type/) { get; } | 返回表单字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words.fields/formfield/accept/)(DocumentVisitor) | 接受访客。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | 获取指定的第一个祖先[`NodeType`](../../aspose.words/nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | 获取指定对象类型的第一个祖先。 |
| override [GetText](../../aspose.words/specialchar/gettext/)() | 获取该节点代表的特殊字符。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | 根据先序树遍历算法获取下一个节点。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveField](../../aspose.words.fields/formfield/removefield/)() | 删除整个表单字段，而不仅仅是表单字段特殊字符。 |
| [SetTextInputValue](../../aspose.words.fields/formfield/settextinputvalue/)(object) | 应用中指定的文本格式[`TextInputFormat`](./textinputformat/)并将值存储在[`Result`](./result/). |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | 使用指定的保存选项将节点的内容导出到字符串中。 |

### 评论

Microsoft Word 提供以下表单字段：复选框、文本输入和下拉列表（组合框）。

`FormField`是一个内联节点并且只能是[`Paragraph`](../../aspose.words/paragraph/)。

`FormField`在文档中由特殊字符 and 表示，定位为文本行中的字符。

Word文档中完整的表单字段是由几个 个节点表示的复杂结构：字段开始、字段代码（例如FORMTEXT）、表单字段数据、字段分隔符、 字段结果、字段结束和书签。要以编程方式在 Word 文档中创建表单字段，请使用 [`InsertCheckBox`](../../aspose.words/documentbuilder/insertcheckbox/), [`InsertTextInput`](../../aspose.words/documentbuilder/inserttextinput/)和 [`InsertComboBox`](../../aspose.words/documentbuilder/insertcombobox/) which 确保所有表单字段节点都以正确的顺序和合适的状态创建。

### 例子

演示如何格式化整个 FormField，包括字段值。

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

演示如何插入组合框。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// 表单字段将以“select”html 标签的形式出现。
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### 也可以看看

* class [SpecialChar](../../aspose.words/specialchar/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


