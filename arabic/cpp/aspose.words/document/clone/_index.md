---
title: "Aspose::Words::Document::Clone method"
linktitle: "Clone"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::Clone method. يقوم بإنشاء نسخة عميقة من المستند في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/document/clone/
---
## Document::Clone method


يقوم بإنشاء نسخة عميقة من الـ[Document](../).

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::Document::Clone()
```


### ReturnValue

المستند المستنسخ.

## أمثلة



يوضح كيفية استنساخ مستند بعمق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

// سيؤدي الاستنساخ إلى إنتاج مستند جديد يحتوي على نفس المحتويات مثل الأصلي،
// ولكن بنسخة فريدة من كل عقدة في المستند الأصلي.
System::SharedPtr<Aspose::Words::Document> clone = doc->Clone();

ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->GetText(), clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Text());
ASSERT_NE(System::ObjectExt::GetHashCode(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)), System::ObjectExt::GetHashCode(clone->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)));
```

## انظر أيضًا

* Class [Document](../)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
