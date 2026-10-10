---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove method"
linktitle: "Rimuovi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove method. Rimuove il tag di documento strutturato con l'identificatore specificato in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection::Remove method


Rimuove il tag di documento strutturato con l'identificatore specificato.

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::Remove(int32_t id)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | int32_t | L'identificatore del tag di documento strutturato. |

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

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
