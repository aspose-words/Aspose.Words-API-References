---
title: "Aspose::Words::Fields::FieldAuthor::get_AuthorName طريقة"
linktitle: "get_AuthorName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldAuthor::get_AuthorName. يحصل على أو يضبط اسم مؤلف المستند في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldauthor/get_authorname/
---
## FieldAuthor::get_AuthorName method


يحصل أو يعيّن اسم مؤلف المستند.

```cpp
System::String Aspose::Words::Fields::FieldAuthor::get_AuthorName()
```


## أمثلة



يوضح كيفية استخدام حقل AUTHOR لعرض اسم منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تستمد حقول AUTHOR نتائجها من خاصية المستند المدمجة المسماة \"Author\".
// إذا أنشأنا وحفظنا مستندًا في Microsoft Word،
// سيحتوي على اسم المستخدم الخاص بنا في تلك الخاصية.
// ومع ذلك، إذا أنشأنا مستندًا برمجيًا باستخدام Aspose.Words،
// ستكون خاصية \"Author\"، بشكل افتراضي، سلسلة فارغة.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// حدد اسم مؤلف احتياطي لاستخدامه في حقول AUTHOR
// إذا كانت خاصية \"Author\" تحتوي على سلسلة فارغة.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// تحديث حقل AUTHOR الذي يحتوي على قيمة
// سيطبق تلك القيمة على خاصية \"Author\" المدمجة.
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// تغيير هذه الخاصية، ثم تحديث حقل AUTHOR سيطبق هذه القيمة على الحقل.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// إذا قمنا بتحديث حقل AUTHOR بعد تغيير خاصية \"Name\" الخاصة به،
// ثم سيعرض الحقل الاسم الجديد ويطبق الاسم الجديد على الخاصية المدمجة.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// حقول AUTHOR لا تؤثر على الخاصية DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## انظر أيضًا

* Class [FieldAuthor](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
