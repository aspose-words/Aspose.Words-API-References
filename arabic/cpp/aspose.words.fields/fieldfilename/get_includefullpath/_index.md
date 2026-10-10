---
title: "طريقة Aspose::Words::Fields::FieldFileName::get_IncludeFullPath"
linktitle: "get_IncludeFullPath"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldFileName::get_IncludeFullPath. تحصل أو تعيين ما إذا كان يجب تضمين اسم مسار الملف الكامل في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldfilename/get_includefullpath/
---
## FieldFileName::get_IncludeFullPath method


يحصل أو يضبط ما إذا كان يجب تضمين اسم مسار الملف الكامل.

```cpp
bool Aspose::Words::Fields::FieldFileName::get_IncludeFullPath()
```


## أمثلة



يوضح كيفية استخدام [FieldOptions](../../fieldoptions/) لتجاوز القيمة الافتراضية لحقل FILENAME.
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

* Class [FieldFileName](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
