---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title Methode"
linktitle: "get_Title"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_Title-Methode. Gibt den freundlichen Namen an, der mit diesem SDT verknüpft ist. Darf in C++ nicht null sein."
type: docs
weight: 12000
url: /de/cpp/aspose.words.markup/istructureddocumenttag/get_title/
---
## IStructuredDocumentTag::get_Title method


Gibt den benutzerfreundlichen Namen an, der mit diesem **SDT** verknüpft ist. Darf nicht null sein.

```cpp
virtual System::String Aspose::Words::Markup::IStructuredDocumentTag::get_Title() const =0
```


## Beispiele



Zeigt, wie man ein strukturiertes Dokument-Tag erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Ruft das strukturierte Dokument-Tag anhand der Id ab.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Ruft das strukturierte Dokument-Tag oder das Bereichs-Tag anhand des Titels ab.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## Siehe auch

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
