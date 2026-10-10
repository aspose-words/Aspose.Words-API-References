---
title: "Aspose::Words::Fields::FieldKeywords::get_Text method"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldKeywords::get_Text method. يحصل على نص الكلمات المفتاحية أو يضبطه في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


يحصل أو يضبط نص الكلمات المفتاحية.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## أمثلة



يظهر كيفية إدراج حقل KEYWORDS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف بعض الكلمات المفتاحية، والتي تُعرف أيضًا باسم "العلامات" في مستكشف الملفات.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// يعرض حقل KEYWORDS قيمة هذه الخاصية.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// تعيين قيمة لخاصية Text الخاصة بالحقل،
// ثم سيؤدي تحديث الحقل إلى استبدال الخاصية المدمجة المقابلة بالقيمة الجديدة.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## انظر أيضًا

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
