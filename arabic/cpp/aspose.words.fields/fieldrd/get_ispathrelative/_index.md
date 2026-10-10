---
title: "طريقة Aspose::Words::Fields::FieldRD::get_IsPathRelative"
linktitle: "get_IsPathRelative"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::FieldRD::get_IsPathRelative. يحصل أو يحدد ما إذا كان المسار نسبياً إلى المستند الحالي في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldrd/get_ispathrelative/
---
## FieldRD::get_IsPathRelative method


يحصل أو يضبط ما إذا كان المسار نسبيًا للمستند الحالي.

```cpp
bool Aspose::Words::Fields::FieldRD::get_IsPathRelative()
```


## أمثلة



يعرض كيفية استخدام حقل RD لإنشاء إدخالات جدول المحتويات من العناوين في مستندات أخرى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// استخدم مُنشئ المستند لإدراج جدول المحتويات،
// ثم أضف مدخلاً واحدًا لفهرس المحتويات في الصفحة التالية.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
builder->Writeln(u"TOC entry from within this document");

// أدرج حقل RD، الذي يشير إلى مستند آخر في نظام الملفات المحلي في خاصية FileName الخاصة به.
// سيتقبل فهرس المحتويات الآن جميع العناوين من المستند المشار إليه كمدخلات لجدوله.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldRD>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRefDoc, true));
field->set_FileName(get_ArtifactsDir() + u"ReferencedDocument.docx");

ASSERT_EQ(System::String::Format(u" RD  {0}ReferencedDocument.docx", get_ArtifactsDir().Replace(u"\\", u"\\\\")), field->GetFieldCode());

// أنشئ المستند الذي يشير إليه حقل RD وأدرج عنوانًا.
// سيظهر هذا العنوان كمدخل في حقل فهرس المحتويات في مستندنا الأول.
auto referencedDoc = System::MakeObject<Aspose::Words::Document>();
auto refDocBuilder = System::MakeObject<Aspose::Words::DocumentBuilder>(referencedDoc);
refDocBuilder->get_CurrentParagraph()->get_ParagraphFormat()->set_StyleName(u"Heading 1");
refDocBuilder->Writeln(u"TOC entry from referenced document");
referencedDoc->Save(get_ArtifactsDir() + u"ReferencedDocument.docx");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.RD.docx");
```

## انظر أيضًا

* Class [FieldRD](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
