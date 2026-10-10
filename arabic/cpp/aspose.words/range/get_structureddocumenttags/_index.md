---
title: "Aspose::Words::Range::get_StructuredDocumentTags طريقة"
linktitle: "get_StructuredDocumentTags"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Range::get_StructuredDocumentTags طريقة. تُرجع مجموعة StructuredDocumentTags التي تمثل جميع علامات المستند المهيكلة في النطاق في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


تُرجع مجموعة [StructuredDocumentTags](./) التي تمثل جميع علامات المستند المهيكلة في النطاق.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## أمثلة



يظهر كيفية إزالة علامة المستند المهيكلة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> structuredDocumentTags = doc->get_Range()->get_StructuredDocumentTags();
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt;
for (int32_t i = 0; i < structuredDocumentTags->get_Count(); i++)
{
    sdt = structuredDocumentTags->idx_get(i);
    std::cout << sdt->get_Title() << std::endl;
}

sdt = structuredDocumentTags->GetById(1691867797);
ASSERT_EQ(1691867797, sdt->get_Id());

ASSERT_EQ(5, structuredDocumentTags->get_Count());
// أزل علامة المستند المهيكلة بواسطة المعرف.
structuredDocumentTags->Remove(1691867797);
// أزل علامة المستند المهيكلة في الموضع 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## انظر أيضًا

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
