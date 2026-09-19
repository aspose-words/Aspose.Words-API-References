---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle"
linktitle: "GetByTitle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle. Restituisce il primo tag di documento strutturato trovato nella collezione con il titolo specificato in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Restituisce il primo tag di documento strutturato trovato nella raccolta con il titolo specificato.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| titolo | const System::String\& | Il titolo del tag di documento strutturato. |
## Note


Restituisce null se il tag di documento strutturato con il titolo specificato non può essere trovato.

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
