---
title: "Classe Aspose::Words::Markup::StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Markup::StructuredDocumentTagCollection. Une collection d'instances IStructuredDocumentTag qui représentent les balises de document structuré dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


Une collection d'instances [IStructuredDocumentTag](../istructureddocumenttag/) qui représentent les balises de document structuré dans la plage spécifiée. Pour en savoir plus, consultez l'article de documentation [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Count](./get_count/)() | Renvoie le nombre de balises de document structuré dans la collection. |
| [GetById](./getbyid/)(int32_t) | Renvoie la balise de document structuré par identifiant. |
| [GetByTag](./getbytag/)(const System::String\&) | Renvoie la première balise de document structuré rencontrée dans la collection avec le tag spécifié. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Renvoie la première balise de document structuré rencontrée dans la collection avec le titre spécifié. |
| [GetEnumerator](./getenumerator/)() override | Renvoie un objet énumérateur. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Renvoie la balise de document structuré à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Supprime la balise de document structuré avec l'identifiant spécifié. |
| [RemoveAt](./removeat/)(int32_t) | Supprime une balise de document structuré à l'index spécifié. |
| static [Type](./type/)() |  |

## Exemples



Montre comment obtenir une balise de document structuré.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Obtenez la balise de document structuré par Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Obtenez la balise de document structuré ou la balise de plage par Titre.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Voir aussi

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
