---
title: "Aspose::Words::FieldOptions::get_FileName طريقة"
linktitle: "get_FileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldOptions::get_FileName. يحصل على أو يضبط اسم ملف المستند في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


الحصول على أو تعيين اسم ملف المستند.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## ملاحظات


يتم استخدام هذه الخاصية بواسطة حقل [FieldFileName](../../fieldfilename/) بأولوية أعلى من خاصية [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## أمثلة



يوضح كيفية استخدام [FieldOptions](../) لتجاوز القيمة الافتراضية لحقل FILENAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// سيعرض حقل FILENAME هذا اسم ملف النظام المحلي للمستند الذي حمّلناه.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// بشكل افتراضي، يُظهر حقل FILENAME اسم الملف، لكن ليس مسار نظام الملفات المحلي الكامل.
// يمكننا ضبط علامة لجعله يعرض مسار الملف الكامل.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// يمكننا أيضًا ضبط قيمة لهذه الخاصية لت
// نتجاوز القيمة التي يعرضها حقل FILENAME.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## انظر أيضًا

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
