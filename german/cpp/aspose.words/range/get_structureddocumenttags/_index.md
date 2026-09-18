---
title: "Aspose::Words::Range::get_StructuredDocumentTags Methode"
linktitle: "get_StructuredDocumentTags"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Range::get_StructuredDocumentTags Methode. Gibt eine StructuredDocumentTags Sammlung zurück, die alle strukturierten Dokument-Tags im Bereich repräsentiert, in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


Gibt eine [StructuredDocumentTags](./) Sammlung zurück, die alle strukturierten Dokument-Tags im Bereich darstellt.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## Beispiele



Zeigt, wie man ein strukturiertes Dokument-Tag entfernt.
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
// Entferne das strukturierte Dokument-Tag nach Id.
structuredDocumentTags->Remove(1691867797);
// Entferne das strukturierte Dokument-Tag an Position 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## Siehe auch

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
