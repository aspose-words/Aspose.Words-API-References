---
title: "Aspose::Words::Fields::FieldMacroButton 类"
linktitle: "FieldMacroButton"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldMacroButton 类。实现 MACROBUTTON 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 65000
url: /zh/cpp/aspose.words.fields/fieldmacrobutton/
---
## FieldMacroButton class


实现 MACROBUTTON 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldMacroButton : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IMergeFieldSurrogate
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_DisplayText](./get_displaytext/)() | 获取或设置显示为\"按钮\"的文本，该按钮用于运行宏或命令。 |
| [get_End](./get_end/)() override | 获取表示字段结束的节点。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_MacroName](./get_macroname/)() | 获取或设置要运行的宏或命令的名称。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](./get_separator/)() override | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](./get_start/)() override | 获取表示字段起始的节点。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_DisplayText](./set_displaytext/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldMacroButton::get_DisplayText](./get_displaytext/)。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_MacroName](./set_macroname/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldMacroButton::get_MacroName](./get_macroname/)。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 备注


允许运行宏或命令。

在 Aspose.Words 中，此字段也可以充当合并字段。

## 示例



展示如何使用 MACROBUTTON 字段，通过点击运行文档的宏。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_TRUE(doc->get_HasMacros());

// 插入一个 MACROBUTTON 字段，并在 MacroName 属性中按名称引用文档的某个宏。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"MyMacro");
field->set_DisplayText(System::String(u"Double click to run macro: ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field->GetFieldCode());

// 使用该属性引用\"ViewZoom200\"，这是 Microsoft Word 附带的宏。
// 我们可以通过 View -> Macros（下拉）-> View Macros 找到所有其他宏。
// 在该菜单中，从 “Macros in:” 下拉列表中选择 “Word Commands”。
// 如果我们的文档包含一个与内置宏同名的自定义宏，
// 我们的宏将是 MACROBUTTON 字段运行的宏。
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldMacroButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldMacroButton, true));
field->set_MacroName(u"ViewZoom200");
field->set_DisplayText(System::String(u"Run ") + field->get_MacroName());

ASSERT_EQ(u" MACROBUTTON  ViewZoom200 Run ViewZoom200", field->GetFieldCode());

// 将文档另存为启用宏的文档类型。
doc->Save(get_ArtifactsDir() + u"Field.MACROBUTTON.docm");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
