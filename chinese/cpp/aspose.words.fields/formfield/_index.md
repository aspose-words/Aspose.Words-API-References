---
title: "Aspose::Words::Fields::FormField 类"
linktitle: "FormField"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FormField 类。表示单个表单字段。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 112000
url: /zh/cpp/aspose.words.fields/formfield/
---
## FormField class


表示单个表单字段。要了解更多信息，请访问 [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/) 文档文章。

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_CalculateOnExit](./get_calculateonexit/)() | 如果对指定表单字段的引用在每次退出字段时自动更新，则为 True。 |
| [get_CheckBoxSize](./get_checkboxsize/)() | 获取或设置复选框的大小（以点为单位）。仅在 [IsCheckBoxExactSize](./get_ischeckboxexactsize/) 为 **true** 时生效。 |
| [get_Checked](./get_checked/)() | 获取或设置复选框表单字段的选中状态。此属性的默认值为 **false**。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_Default](./get_default/)() | 获取或设置复选框表单字段的默认值。此属性的默认值为 **false**。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_DropDownItems](./get_dropdownitems/)() | 提供对下拉表单字段项的访问。 |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | 获取指定下拉表单字段中当前选中项的索引。 |
| [get_Enabled](./get_enabled/)() | 如果表单字段已启用，则为 True。 |
| [get_EntryMacro](./get_entrymacro/)() | 返回或设置表单字段的入口宏名称。 |
| [get_ExitMacro](./get_exitmacro/)() | 返回或设置表单字段的退出宏名称。 |
| [get_Font](../../aspose.words/inline/get_font/)() | 提供对该对象字体格式的访问。 |
| [get_HelpText](./get_helptext/)() | 返回或设置当表单字段获得焦点且用户按下 F1 时在消息框中显示的文本。 |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | 获取或设置布尔值，以指示文本框的大小是自动的还是显式指定的。 |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | 如果在启用更改跟踪时，Microsoft Word 中对象的格式被更改，则返回 true。 |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_MaxLength](./get_maxlength/)() | 文本字段的最大长度。若长度不受限制，则为零。 |
| [get_Name](./get_name/)() | 获取或设置表单字段名称。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [FormField](../../aspose.words/nodetype/)。 |
| [get_OwnHelp](./get_ownhelp/)() | 指定当表单字段获得焦点且用户按下 F1 时在消息框中显示的文本来源。 |
| [get_OwnStatus](./get_ownstatus/)() | 指定当表单字段获得焦点时在状态栏中显示的文本来源。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | 检索此节点的父级 [Paragraph](../../aspose.words/paragraph/)。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_Result](./get_result/)() | 获取或设置表示此表单字段结果的字符串。 |
| [get_StatusText](./get_statustext/)() | 获取或设置当表单字段获得焦点时显示在状态栏中的文本。 |
| [get_TextInputDefault](./get_textinputdefault/)() | 获取或设置文本表单字段的默认字符串或计算表达式。 |
| [get_TextInputFormat](./get_textinputformat/)() | 获取或设置文本表单字段的文本格式。 |
| [get_TextInputType](./get_textinputtype/)() | 获取文本表单字段的类型。 |
| [get_Type](./get_type/)() | 返回表单字段的类型。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | 获取此节点表示的特殊字符。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [RemoveField](./removefield/)() | 删除整个表单字段，而不仅仅是表单字段的特殊字符。 |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | 用于 [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/) 的设置器。 |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | 用于 [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/) 的设置器。 |
| [set_Checked](./set_checked/)(bool) | 用于 [Aspose::Words::Fields::FormField::get_Checked](./get_checked/) 的设置器。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_Default](./set_default/)(bool) | 用于 [Aspose::Words::Fields::FormField::get_Default](./get_default/) 的设置器。 |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | 设置指定下拉表单字段中当前选中项的索引。 |
| [set_Enabled](./set_enabled/)(bool) | 如果表单字段已启用，则为 True。 |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/) 的设置器。 |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/) 的设置器。 |
| [set_HelpText](./set_helptext/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/) 的设置器。 |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | 用于 [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/) 的设置器。 |
| [set_MaxLength](./set_maxlength/)(int32_t) | 文本字段的最大长度。若长度不受限制，则为零。 |
| [set_Name](./set_name/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_Name](./get_name/) 的设置器。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | 用于 [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/) 的设置器。 |
| [set_OwnStatus](./set_ownstatus/)(bool) | 用于 [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/) 的设置器。 |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_Result](./get_result/) 的设置器。 |
| [set_StatusText](./set_statustext/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/) 的设置器。 |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/) 的设置器。 |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | 用于 [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/) 的设置器。 |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | 设置文本表单字段的类型。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | 应用在 [TextInputFormat](./get_textinputformat/) 中指定的文本格式，并将值存储在 [Result](./get_result/) 中。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


Microsoft Word 提供以下表单字段：复选框、文本输入和下拉列表（组合框）。

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Word 文档中的完整表单字段是由多个节点构成的复杂结构：字段开始、字段代码（如 FORMTEXT）、表单字段数据、字段分隔符、字段结果、字段结束以及书签。要以编程方式在 Word 文档中创建表单字段，请使用 [InsertCheckBox()](../)、[InsertTextInput()](../) 和 [InsertComboBox()](../)，它们可确保所有表单字段节点以正确的顺序和适当的状态创建。

## 示例



展示如何插入组合框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// 表单字段将以 "select" HTML 标签的形式出现。
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


展示如何格式化整个 [FormField](./)，包括字段值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(0);
formField->get_Font()->set_Bold(true);
formField->get_Font()->set_Size(24);
formField->get_Font()->set_Color(System::Drawing::Color::get_Red());

formField->set_Result(u"Aspose.FormField");

doc = Aspose::Words::ApiExamples::DocumentHelper::SaveOpen(doc);

System::SharedPtr<Aspose::Words::Run> formFieldRun = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1);

ASSERT_EQ(u"Aspose.FormField", formFieldRun->get_Text());
ASPOSE_ASSERT_EQ(true, formFieldRun->get_Font()->get_Bold());
ASPOSE_ASSERT_EQ(24, formFieldRun->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), formFieldRun->get_Font()->get_Color().ToArgb());
```

## 另见

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
