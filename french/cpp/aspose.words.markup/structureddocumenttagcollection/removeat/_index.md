---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::RemoveAt méthode"
linktitle: "RemoveAt"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::RemoveAt méthode. Supprime une balise de document structuré à l'index spécifié en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.markup/structureddocumenttagcollection/removeat/
---
## StructuredDocumentTagCollection::RemoveAt method


Supprime une balise de document structuré à l'index spécifié.

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::RemoveAt(int32_t index)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| index | int32_t | Un index dans la collection. |

## Exemples



Montre comment supprimer une balise de document structurée.
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
// Supprime la balise de document structurée par identifiant.
structuredDocumentTags->Remove(1691867797);
// Supprime la balise de document structurée à la position 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## Voir aussi

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
