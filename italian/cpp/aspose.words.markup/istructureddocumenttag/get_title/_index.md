---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title metodo"
linktitle: "get_Title"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title metodo. Specifica il nome amichevole associato a questo SDT. Non può essere nullo in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


Specifica il nome descrittivo associato a questo **SDT**. Non può essere null.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
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
