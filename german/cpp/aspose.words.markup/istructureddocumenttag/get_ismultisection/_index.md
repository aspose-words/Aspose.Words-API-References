---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection Methode"
linktitle: "get_IsMultiSection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection Methode. Gibt true zurück, wenn diese Instanz ein bereichsbezogenes (mehrabschnittiges) strukturiertes Dokument-Tag in C++ ist."
type: docs
weight: 3500
url: /de/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Gibt true zurück, wenn diese Instanz ein Bereichs‑(Mehrabschnitt‑) strukturierter Dokument-Tag ist.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
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
