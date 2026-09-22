---
title: "Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar طريقة"
linktitle: "get_UseLunarCalendar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar طريقة. يحصل أو يضبط ما إذا كان سيتم استخدام التقويم القمري الهجري أو التقويم القمري العبري في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldsavedate/get_uselunarcalendar/
---
## FieldSaveDate::get_UseLunarCalendar method


يحصل أو يضبط ما إذا كان سيتم استخدام التقويم القمري الهجري أو التقويم القمري العبري.

```cpp
bool Aspose::Words::Fields::FieldSaveDate::get_UseLunarCalendar() override
```


## أمثلة



يُظهر كيفية استخدام حقل SAVEDATE لعرض التاريخ/الوقت لآخر عملية حفظ للوثيقة تم تنفيذها باستخدام Microsoft Word.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->Writeln(u" Date this document was last saved:");

// يمكننا استخدام حقل SAVEDATE لعرض تاريخ ووقت آخر عملية حفظ على الوثيقة.
// عملية الحفظ التي تشير إليها هذه الحقول هي الحفظ اليدوي في تطبيق مثل Microsoft Word،
// ليس طريقة Save الخاصة بالوثيقة.
// فيما يلي ثلاثة أنواع مختلفة من التقويمات التي يمكن لحقل SAVEDATE من خلالها عرض التاريخ/الوقت.
// 1 -  التقويم القمري الإسلامي:
builder->Write(u"According to the Lunar Calendar - ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseLunarCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\h", field->GetFieldCode());

// 2 -  تقويم أم القرى:
builder->Write(u"\nAccording to the Umm al-Qura calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseUmAlQuraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\u", field->GetFieldCode());

// 3 - التقويم الوطني الهندي:
builder->Write(u"\nAccording to the Indian National calendar - ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldSaveDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSaveDate, true));
field->set_UseSakaEraCalendar(true);

ASSERT_EQ(u" SAVEDATE  \\s", field->GetFieldCode());

// تستمد حقول SAVEDATE قيم التاريخ/الوقت من الخاصية المدمجة LastSavedTime.
// طريقة Save الخاصة بالوثيقة لن تقوم بتحديث هذه القيمة، لكن لا يزال بإمكاننا تحديثها يدويًا.
doc->get_BuiltInDocumentProperties()->set_LastSavedTime(System::DateTime::get_Now());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SAVEDATE.docx");
```

## انظر أيضًا

* Class [FieldSaveDate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
