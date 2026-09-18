---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection Klasse"
linktitle: "StructuredDocumentTagCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection Klasse. Eine Sammlung von IStructuredDocumentTag‑Instanzen, die die strukturierten Dokument‑Tags im angegebenen Bereich repräsentieren. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


Eine Sammlung von [IStructuredDocumentTag](../istructureddocumenttag/) Instanzen, die die strukturierten Dokument‑Tags im angegebenen Bereich repräsentieren. Weitere Informationen finden Sie im Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Count](./get_count/)() | Gibt die Anzahl der strukturierten Dokument‑Tags in der Sammlung zurück. |
| [GetById](./getbyid/)(int32_t) | Gibt das strukturierte Dokument‑Tag anhand der Kennung zurück. |
| [GetByTag](./getbytag/)(const System::String\&) | Gibt das erste in der Sammlung gefundene strukturierte Dokument‑Tag mit dem angegebenen Tag zurück. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Gibt das erste strukturierte Dokument-Tag zurück, das in der Sammlung mit dem angegebenen Titel gefunden wird. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt das strukturierte Dokument-Tag am angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Entfernt das strukturierte Dokument-Tag mit der angegebenen Kennung. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein strukturiertes Dokument-Tag am angegebenen Index. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
