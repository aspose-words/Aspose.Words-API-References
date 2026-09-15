---
title: "طريقة Aspose::Words::PlainTextDocument::get_CustomDocumentProperties"
linktitle: "get_CustomDocumentProperties"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PlainTextDocument::get_CustomDocumentProperties. يحصل على CustomDocumentProperties للوثيقة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/plaintextdocument/get_customdocumentproperties/
---
## PlainTextDocument::get_CustomDocumentProperties method


يحصل على [CustomDocumentProperties](./) للوثيقة.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::PlainTextDocument::get_CustomDocumentProperties() const
```


## أمثلة



يوضح كيفية تحميل محتويات مستند Microsoft Word كنص عادي ثم الوصول إلى الخصائص المخصصة للمستند الأصلي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_CustomDocumentProperties()->Add(u"Location of writing", System::String(u"123 Main St, London, UK"));

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASPOSE_ASSERT_EQ(u"123 Main St, London, UK", plaintext->get_CustomDocumentProperties()->idx_get(u"Location of writing")->get_Value());
```

## انظر أيضًا

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
