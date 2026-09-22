---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::RemoveAt method. يزيل علامة مستند مُنظمة عند الفهرس المحدد في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection::RemoveAt method


يزيل علامة مستند مهيكلة عند الفهرس المحدد.

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::RemoveAt(int32_t index)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| index | int32_t | فهرس داخل المجموعة. |

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

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
