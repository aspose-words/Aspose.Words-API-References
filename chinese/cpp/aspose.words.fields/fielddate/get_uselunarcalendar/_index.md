---
title: "Aspose::Words::Fields::FieldDate::get_UseLunarCalendar 方法"
linktitle: "get_UseLunarCalendar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldDate::get_UseLunarCalendar 方法。获取或设置是否在 C++ 中使用伊斯兰阴历或希伯来阴历。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fielddate/get_uselunarcalendar/
---
## FieldDate::get_UseLunarCalendar method


获取或设置是否使用伊斯兰阴历或希伯来阴历。

```cpp
bool Aspose::Words::Fields::FieldDate::get_UseLunarCalendar() override
```


## 示例



展示如何使用 DATE 字段根据不同类型的日历显示日期。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 如果我们希望文档中的文本始终显示正确的日期，可以使用 DATE 字段。
// 以下是 DATE 字段可以用来显示日期的三种文化日历类型。
// 1 - 伊斯兰阴历：
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al-Qura 日历：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  印度国家日历：
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// 插入一个 DATE 字段并将其日历类型设置为主机应用程序上次使用的类型。
// 在 Microsoft Word 中，该类型将是最近在 Insert -> Text -> Date and Time 对话框中使用的类型。
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## 另见

* Class [FieldDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
