---
title: "classe Aspose::Words::Markup::StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Markup::StructuredDocumentTagCollection. Una raccolta di istanze IStructuredDocumentTag che rappresentano i tag di documento strutturato nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


Una raccolta di [IStructuredDocumentTag](../istructureddocumenttag/) istanze che rappresentano i tag di documento strutturato nell'intervallo specificato. Per saperne di più, visita l'articolo di documentazione [Tag di documento strutturato o controllo contenuto](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Restituisce il numero di tag di documento strutturato nella raccolta. |
| [GetById](./getbyid/)(int32_t) | Restituisce il tag di documento strutturato per identificatore. |
| [GetByTag](./getbytag/)(const System::String\&) | Restituisce il primo tag di documento strutturato trovato nella raccolta con il tag specificato. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Restituisce il primo tag di documento strutturato trovato nella raccolta con il titolo specificato. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce il tag di documento strutturato all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Rimuove il tag di documento strutturato con l'identificatore specificato. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un tag di documento strutturato all'indice specificato. |
| static [Type](./type/)() |  |

## Esempi



Mostra come ottenere il tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Ottieni il tag di documento strutturato per Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Ottieni il tag di documento strutturato o il tag di intervallo per Titolo.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
