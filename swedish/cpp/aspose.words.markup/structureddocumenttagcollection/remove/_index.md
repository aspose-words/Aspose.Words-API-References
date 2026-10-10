---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove metod"
linktitle: "Ta bort"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove metod. Tar bort det strukturerade dokumenttagget med den angivna identifieraren i C++."
type: docs
weight: 10000
url: /sv/cpp/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection::Remove method


Tar bort den strukturerade dokumenttaggen med den angivna identifieraren.

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::Remove(int32_t id)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| id | int32_t | Den strukturerade dokumenttaggens identifierare. |

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

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
