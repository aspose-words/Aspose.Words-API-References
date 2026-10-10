---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle Methode"
linktitle: "GetByTitle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle Methode. Gibt das erste strukturierte Dokument‑Tag in der Sammlung mit dem angegebenen Titel in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wird.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Titel | const System::String\& | Der Titel des strukturierten Dokument‑Tags. |
## Hinweise


Gibt null zurück, wenn das strukturierte Dokument‑Tag mit dem angegebenen Titel nicht gefunden werden kann.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
