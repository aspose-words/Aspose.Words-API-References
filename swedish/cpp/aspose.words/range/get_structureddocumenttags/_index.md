---
title: "Aspose::Words::Range::get_StructuredDocumentTags metod"
linktitle: "get_StructuredDocumentTags"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Range::get_StructuredDocumentTags metod. Returnerar en StructuredDocumentTags-samling som representerar alla strukturerade dokumenttaggar i intervallet i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


Returnerar en [StructuredDocumentTags](./)-samling som representerar alla strukturerade dokumenttaggar i intervallet.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## Exempel



Visar hur man tar bort en strukturerad dokumenttagg.
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
// Ta bort den strukturerade dokumenttaggen med Id.
structuredDocumentTags->Remove(1691867797);
// Ta bort den strukturerade dokumenttaggen på position 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## Se även

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
