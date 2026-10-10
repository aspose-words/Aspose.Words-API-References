---
title: "طريقة get_IgnoreStoreItemId"
linktitle: "get_IgnoreStoreItemId"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة get_IgnoreStoreItemId. يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين StructuredDocumentTag في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.comparing/advancedcompareoptions/get_ignorestoreitemid/
---
## AdvancedCompareOptions::get_IgnoreStoreItemId method


يحدد ما إذا كان يجب تجاهل الاختلاف في معرف عنصر التخزين لـ StructuredDocumentTag.

```cpp
bool Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId() const
```


## أمثلة



يوضح كيفية مقارنة SDT بنفس المحتوى ولكن بمعرف عنصر تخزين مختلف.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// قم بتكوين الخيارات لمقارنة SDT بنفس المحتوى ولكن بمعرف عنصر تخزين مختلف.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## انظر أيضًا

* Class [AdvancedCompareOptions](../)
* Namespace [Aspose::Words::Comparing](../../)
* Library [Aspose.Words for C++](../../../)
