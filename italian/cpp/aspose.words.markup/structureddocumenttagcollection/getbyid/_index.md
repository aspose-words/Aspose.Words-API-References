---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById method"
linktitle: "GetById"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById method. Restituisce il tag di documento strutturato per identificatore in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Restituisce il tag di documento strutturato per identificatore.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| id | int32_t | L'identificatore del tag di documento strutturato. |
## Note


Restituisce null se il tag di documento strutturato con l'identificatore specificato non può essere trovato.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
