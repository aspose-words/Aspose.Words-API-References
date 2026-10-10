---
title: "طريقة Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes"
linktitle: "get_IsInKilobytes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes. يحصل أو يضبط ما إذا كان سيتم عرض حجم الملف بالكيلوبايت في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldfilesize/get_isinkilobytes/
---
## FieldFileSize::get_IsInKilobytes method


يحصل أو يضبط ما إذا كان يجب عرض حجم الملف بالكيلوبايت.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInKilobytes()
```


## أمثلة



يوضح كيفية عرض حجم ملف المستند باستخدام حقل FILESIZE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// فيما يلي ثلاث وحدات قياس مختلفة
// يمكن لحقول FILESIZE من خلالها عرض حجم ملف المستند.
// 1 -  بايت:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  كيلوبايت:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  ميغابايت:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// لتحديث قيم هذه الحقول أثناء التحرير في Microsoft Word،
// يجب أولاً حفظ التغييرات، ثم تحديث هذه الحقول يدويًا.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## انظر أيضًا

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
