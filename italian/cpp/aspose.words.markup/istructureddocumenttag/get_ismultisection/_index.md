---
title: "Metodo Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection"
linktitle: "get_IsMultiSection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection. Restituisce true se questa istanza è un tag di documento strutturato a intervallo (multi-sezione) in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Restituisce true se questa istanza è un tag di documento strutturato a intervallo (multi-sezione).

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


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

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
