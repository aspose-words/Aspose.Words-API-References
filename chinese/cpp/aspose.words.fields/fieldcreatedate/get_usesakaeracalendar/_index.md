---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar 方法"
linktitle: "get_UseSakaEraCalendar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar 方法。获取或设置在 C++ 中是否使用 Saka Era 日历。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldcreatedate/get_usesakaeracalendar/
---
## FieldCreateDate::get_UseSakaEraCalendar method


获取或设置是否使用 Saka 纪元历。

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseSakaEraCalendar() override
```


## 示例



展示如何使用 CREATEDATE 字段显示文档的创建日期/时间。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// 我们可以使用 CREATEDATE 字段显示文档创建的日期和时间。
// 以下是三种不同的日历类型，CREATEDATE 字段可根据其显示日期/时间。
// 1 - 伊斯兰阴历：
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  Umm al-Qura 日历：
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  印度国家日历：
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## 另见

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
