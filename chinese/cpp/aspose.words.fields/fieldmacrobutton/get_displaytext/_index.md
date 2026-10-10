---
title: "Aspose::Words::Fields::FieldMacroButton::get_DisplayText 方法"
linktitle: "get_DisplayText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldMacroButton::get_DisplayText 方法。获取或设置在 C++ 中作为选中以运行宏或命令的 \"按钮\" 显示的文本。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.fields/fieldmacrobutton/get_displaytext/
---
## FieldMacroButton::get_DisplayText method


获取或设置显示为\"按钮\"的文本，该按钮用于运行宏或命令。

```cpp
System::String Aspose::Words::Fields::FieldMacroButton::get_DisplayText()
```


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

* Class [FieldMacroButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
