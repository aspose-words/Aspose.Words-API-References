---
title: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar 方法"
linktitle: "get_UseSakaEraCalendar"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar 方法。获取或设置在 C++ 中是否使用 Saka Era 日历。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fields/fieldprintdate/get_usesakaeracalendar/
---
## FieldPrintDate::get_UseSakaEraCalendar method


获取或设置是否使用 Saka 纪元历。

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseSakaEraCalendar() override
```


## 示例



显示已读取的 PRINTDATE 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// 当文档通过打印机打印或打印为 PDF（但未导出为 PDF）时，
// PRINTDATE 字段将显示打印操作的日期/时间。
// 如果未进行打印，这些字段将显示 "0/0/0000"。
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// 以下是根据 PRINTDATE 字段的三种不同日历类型
// 可以显示上一次打印操作的日期和时间。
// 1 - 伊斯兰阴历：
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  Umm al-Qura 日历：
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  印度国家日历：
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## 另见

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
