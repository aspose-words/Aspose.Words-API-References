---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime طريقة"
linktitle: "get_LastSavedTime"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime. يحصل على أو يحدد وقت آخر حفظ بتوقيت UTC في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_lastsavedtime/
---
## BuiltInDocumentProperties::get_LastSavedTime method


يحصل أو يضبط وقت آخر حفظ بتوقيت UTC.

```cpp
System::DateTime Aspose::Words::Properties::BuiltInDocumentProperties::get_LastSavedTime()
```

## ملاحظات


بالنسبة للمستندات التي تم إنشاؤها من تنسيق RTF، تُعيد هذه الخاصية الوقت المحلي لعملية الحفظ الأخيرة.

Aspose.Words لا يقوم بتحديث هذه الخاصية.

## أمثلة



يظهر كيفية العمل مع خصائص المستند في فئة "Origin".
```cpp
// افتح مستندًا قمنا بإنشائه وتحريره باستخدام Microsoft Word.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

// الخصائص المدمجة التالية تحتوي على معلومات حول إنشاء وتحرير هذا المستند.
// يمكننا النقر بزر الماوس الأيمن على هذا المستند في Windows Explorer والعثور على
// هذه الخصائص عبر "Properties" -> "Details" -> فئة "Origin".
// يمكن للحقول مثل PRINTDATE و EDITTIME عرض هذه القيم في جسم المستند.
std::cout << System::String::Format(u"Created using {0}, on {1}", properties->get_NameOfApplication(), properties->get_CreatedTime()) << std::endl;
std::cout << System::String::Format(u"Minutes spent editing: {0}", properties->get_TotalEditingTime()) << std::endl;
std::cout << System::String::Format(u"Date/time last printed: {0}", properties->get_LastPrinted()) << std::endl;
std::cout << System::String::Format(u"Template document: {0}", properties->get_Template()) << std::endl;

// يمكننا أيضًا تغيير قيم الخصائص المدمجة.
properties->set_Company(u"Doe Ltd.");
properties->set_Manager(u"Jane Doe");
properties->set_Version(5);
System::WithLambda::setter_post_increment_wrap(GETTER_SETTER_LAMBDA_ARGS(properties, RevisionNumber));

// Microsoft Word يقوم بتحديث الخصائص التالية تلقائيًا عند حفظ المستند.
// لاستخدام هذه الخصائص مع Aspose.Words، سنحتاج إلى ضبط القيم لها يدويًا.
properties->set_LastSavedBy(u"John Doe");
properties->set_LastSavedTime(System::DateTime::get_Now());

// يمكننا النقر بزر الماوس الأيمن على هذا المستند في Windows Explorer والعثور على هذه الخصائص في "Properties" -> "Details" -> "Origin".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.Origin.docx");
```


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

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
