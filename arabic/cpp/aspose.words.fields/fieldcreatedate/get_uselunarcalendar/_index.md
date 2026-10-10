---
title: "Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar طريقة"
linktitle: "get_UseLunarCalendar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar طريقة. يحصل أو يضبط ما إذا كان سيتم استخدام التقويم القمري الهجري أو التقويم القمري العبري في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldcreatedate/get_uselunarcalendar/
---
## FieldCreateDate::get_UseLunarCalendar method


يحصل أو يضبط ما إذا كان سيتم استخدام التقويم القمري الهجري أو التقويم القمري العبري.

```cpp
bool Aspose::Words::Fields::FieldCreateDate::get_UseLunarCalendar() override
```


## أمثلة



يوضح كيفية استخدام حقل CREATEDATE لعرض تاريخ/وقت إنشاء المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was created:");

// يمكننا استخدام حقل CREATEDATE لعرض تاريخ ووقت إنشاء المستند.
// فيما يلي ثلاثة أنواع مختلفة من التقويمات التي يمكن لحقل CREATEDATE من خلالها عرض التاريخ/الوقت.
// 1 -  التقويم القمري الإسلامي:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\h", field->GetFieldCode());

// 2 -  تقويم أم القرى:
builder->Write(u"\nAccording to the Umm al-Qura Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\u", field->GetFieldCode());

// 3 -  التقويم الوطني الهندي:
builder->Write(u"\nAccording to the Indian National Calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldCreateDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCreateDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" CREATEDATE  \\s", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CREATEDATE.docx");
```

## انظر أيضًا

* Class [FieldCreateDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
