---
title: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture 方法"
linktitle: "get_PreProcessCulture"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions::get_PreProcessCulture 方法。获取或设置在 C++ 中预处理字段值的文化。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


获取或设置用于预处理字段值的区域性。

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## 备注


当前此属性仅影响 [FieldDocProperty](../../fielddocproperty/) 字段的值。

默认值为 **null**。当此属性设置为 **null** 时，[FieldDocProperty](../../fielddocproperty/) 字段的值将使用由 [FieldUpdateCultureSource](../get_fieldupdateculturesource/) 属性控制的文化进行预处理。

## 示例



展示如何设置预处理文化。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 设置文化，以便某些字段按照该文化格式化其显示的值。
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// DOCPROPERTY 字段将显示按照预处理文化格式化的结果。
// 我们已将其设置为德语。字段将使用 "dd.mm.yyyy hh:mm" 格式显示日期/时间。
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// 切换到不变文化后，DOCPROPERTY 字段将使用 "mm/dd/yyyy hh:mm" 格式。
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## 另见

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
