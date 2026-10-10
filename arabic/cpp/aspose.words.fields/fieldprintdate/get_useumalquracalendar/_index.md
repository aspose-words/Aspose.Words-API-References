---
title: "طريقة Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar"
linktitle: "get_UseUmAlQuraCalendar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar. تحصل أو تعين ما إذا كان سيتم استخدام تقويم أم القرى في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.fields/fieldprintdate/get_useumalquracalendar/
---
## FieldPrintDate::get_UseUmAlQuraCalendar method


يحصل أو يضبط ما إذا كان سيتم استخدام تقويم أم القرى.

```cpp
bool Aspose::Words::Fields::FieldPrintDate::get_UseUmAlQuraCalendar() override
```


## أمثلة



يعرض حقول PRINTDATE المقروءة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Field sample - PRINTDATE.docx");

// عند طباعة مستند بواسطة طابعة أو طباعته كملف PDF (ولكن ليس تصديره إلى PDF),
// ستعرض حقول PRINTDATE تاريخ/وقت عملية الطباعة.
// إذا لم يحدث أي طباعة، ستعرض هذه الحقول "0/0/0000".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(0));

ASSERT_EQ(u"3/25/2020 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE ", field->GetFieldCode());

// فيما يلي ثلاثة أنواع مختلفة من التقويمات التي يعتمد عليها حقل PRINTDATE
// يمكنه عرض تاريخ ووقت آخر عملية طباعة.
// 1 -  التقويم القمري الإسلامي:
field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(1));

ASSERT_TRUE(field->get_UseLunarCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\h", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(2));

// 2 -  تقويم أم القرى:
ASSERT_TRUE(field->get_UseUmAlQuraCalendar());
ASSERT_EQ(u"8/1/1441 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\u", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldPrintDate>(doc->get_Range()->get_Fields()->idx_get(3));

// 3 -  التقويم الوطني الهندي:
ASSERT_TRUE(field->get_UseSakaEraCalendar());
ASSERT_EQ(u"1/5/1942 12:00:00 AM", field->get_Result());
ASSERT_EQ(u" PRINTDATE  \\s", field->GetFieldCode());
```

## انظر أيضًا

* Class [FieldPrintDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
