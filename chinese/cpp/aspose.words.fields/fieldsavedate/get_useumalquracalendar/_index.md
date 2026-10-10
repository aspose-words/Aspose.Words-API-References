---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseUmAlQuraCalendar 方法"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseUmAlQuraCalendar 方法。获取或设置是否在 C++ 中使用 Um-al-Qura 日历。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fields/fieldsavedate/get_useumalquracalendar/
---
## FieldSaveDate::get_UseUmAlQuraCalendar method


获取或设置是否使用 Um-al-Qura 日历。

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseUmAlQuraCalendar() override
```


## 示例



展示如何使用 SAVEDATE 字段显示使用 Microsoft Word 执行的文档最近一次保存操作的日期/时间。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// 我们可以使用 SAVEDATE 字段在文档上显示上一次保存操作的日期和时间。
// 这些字段所指的保存操作是类似 Microsoft Word 的应用程序中的手动保存，
// 而不是文档的 Save 方法。
// 以下是三种不同的日历类型，SAVEDATE 字段可以根据这些类型显示日期/时间。
// 1 - 伊斯兰阴历：
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura 日历：
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - 印度国家日历：
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// SAVEDATE 字段从内置属性 LastSavedTime 获取其日期/时间值。
// 文档的 Save 方法不会更新此值，但我们仍然可以手动更新它。
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## 另见

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
