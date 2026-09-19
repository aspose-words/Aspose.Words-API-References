---
title: "Metodo Aspose::Words::Range::get_StructuredDocumentTags"
linktitle: "get_StructuredDocumentTags"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Range::get_StructuredDocumentTags. Restituisce una raccolta StructuredDocumentTags che rappresenta tutti i tag di documento strutturati nell'intervallo in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/range/get_structureddocumenttags/
---
## Range::get_StructuredDocumentTags method


Restituisce una raccolta [StructuredDocumentTags](./) che rappresenta tutti i tag di documento strutturati nell'intervallo.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> Aspose::Words::Range::get_StructuredDocumentTags()
```


## Esempi



Mostra come rimuovere un tag di documento strutturato.
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
// Rimuovi il tag di documento strutturato per Id.
structuredDocumentTags->Remove(1691867797);
// Rimuovi il tag di documento strutturato alla posizione 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## Vedi anche

* Class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
