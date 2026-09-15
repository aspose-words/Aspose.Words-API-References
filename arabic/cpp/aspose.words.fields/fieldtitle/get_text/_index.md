---
title: "Aspose::Words::Fields::FieldTitle::get_Text الطريقة"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldTitle::get_Text طريقة. يحصل أو يضبط نص العنوان في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


يحصل أو يضبط نص العنوان.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## أمثلة



يظهر كيفية استخدام حقل TITLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// عيّن قيمة لخاصية المستند المدمجة "Title".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// يمكننا استخدام حقل TITLE لعرض قيمة هذه الخاصية في المستند.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// تعيين قيمة لخاصية Text الخاصة بالحقل،
// ثم سيؤدي تحديث الحقل إلى استبدال الخاصية المدمجة المقابلة بالقيمة الجديدة.
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## انظر أيضًا

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
