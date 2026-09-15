---
title: "طريقة Aspose::Words::Document::get_PunctuationKerning"
linktitle: "get_PunctuationKerning"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_PunctuationKerning. يحدد ما إذا كان التباعد بين الحروف (kerning) يُطبق على كل من النص اللاتيني وعلامات الترقيم في C++."
type: docs
weight: 44500
url: /ar/cpp/aspose.words/document/get_punctuationkerning/
---
## Document::get_PunctuationKerning method


يحدد ما إذا كان التباعد بين الحروف (kerning) يطبق على النص اللاتيني وعلامات الترقيم.

```cpp
bool Aspose::Words::Document::get_PunctuationKerning()
```


## أمثلة



يوضح كيفية العمل مع تطبيق التباعد بين الحروف على كل من النص اللاتيني وعلامات الترقيم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
ASSERT_TRUE(doc->get_PunctuationKerning());
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
