---
title: "Aspose::Words::Fields::FieldComments::get_Text طريقة"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldComments::get_Text طريقة. يحصل على نص التعليقات أو يضبطه في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


يحصل أو يعيّن نص التعليقات.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## أمثلة



يظهر كيفية استخدام حقل COMMENTS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// عيّن قيمة لخاصية "Comments" المدمجة في المستند.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// أنشئ حقل COMMENTS لعرض قيمة تلك الخاصية المدمجة.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// إذا أعطينا حقل COMMENTS قيمة خاصية Text وقمنا بتحديثه، سيقوم الحقل بـ
// ستستبدل القيمة الحالية لخاصية "Comments" المدمجة بقيمة خاصية Text الخاصة به،
// ثم تعرض القيمة الجديدة.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## انظر أيضًا

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
