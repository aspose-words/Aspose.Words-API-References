---
title: "طريقة Aspose::Words::PlainTextDocument::get_Text"
linktitle: "get_Text"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PlainTextDocument::get_Text. يحصل على المحتوى النصي للمستند مجمعًا كسلسلة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


يحصل على المحتوى النصي للمستند مدموجًا كسلسلة.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## أمثلة



يظهر كيفية تحميل محتويات مستند Microsoft Word كنص عادي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## انظر أيضًا

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
