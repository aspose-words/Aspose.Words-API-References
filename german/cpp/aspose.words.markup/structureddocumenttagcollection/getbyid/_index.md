---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById Methode"
linktitle: "GetById"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById Methode. Gibt das strukturierte Dokument‑Tag anhand der Kennung in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Gibt das strukturierte Dokument‑Tag anhand der Kennung zurück.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| id | int32_t | Der Kennung des strukturierten Dokument‑Tags. |
## Hinweise


Gibt null zurück, wenn das strukturierte Dokument‑Tag mit der angegebenen Kennung nicht gefunden werden kann.

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
