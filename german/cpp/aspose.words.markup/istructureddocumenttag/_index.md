---
title: "Aspose::Words::Markup::IStructuredDocumentTag Schnittstelle"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::IStructuredDocumentTag Schnittstelle. Schnittstelle zur Definition gemeinsamer Daten für StructuredDocumentTag und StructuredDocumentTagRangeStart in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Schnittstelle zur Definition gemeinsamer Daten für [StructuredDocumentTag](../structureddocumenttag/) und [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Liest oder setzt das Erscheinungsbild des strukturierten Dokument-Tags. |
| virtual [get_Color](./get_color/)() | Liest oder setzt die Farbe des strukturierten Dokument-Tags. |
| virtual [get_Id](./get_id/)() | Gibt eine eindeutige schreibgeschützte persistente numerische Id für dieses **SDT** an. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Gibt true zurück, wenn diese Instanz ein Bereichs‑(Mehrabschnitt‑) strukturierter Dokument-Tag ist. |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Gibt an, ob der Inhalt dieses **SDT** als Platzhaltertext interpretiert werden soll (im Gegensatz zu regulärem Textinhalt innerhalb des SDT). Wenn auf true gesetzt, wird dieser Zustand beim Öffnen des Dokuments wiederhergestellt (Platzhaltertext wird angezeigt). |
| virtual [get_Level](./get_level/)() const | Liest die Ebene, auf der dieses **SDT** im Dokumentbaum vorkommt. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | Wenn auf true gesetzt, verhindert diese Eigenschaft, dass ein Benutzer dieses **SDT** löscht. |
| virtual [get_LockContents](./get_lockcontents/)() | Wenn auf true gesetzt, verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieses **SDT** bearbeitet. |
| virtual [get_Node](./get_node/)() | Gibt ein [Node](../../aspose.words/node/)‑Objekt zurück, das diese Schnittstelle implementiert. |
| virtual [get_Placeholder](./get_placeholder/)() | Liest das [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), das Platzhaltertext enthält und angezeigt werden soll, wenn der Inhalt dieses SDT‑Laufs leer ist, das zugehörige zugeordnete XML‑Element leer ist, wie über das [XmlMapping](./get_xmlmapping/)‑Element angegeben, oder das [IsShowingPlaceholderText](./get_isshowingplaceholdertext/)‑Element true ist. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Liest oder setzt den Namen des [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/), das Platzhaltertext enthält. |
| virtual [get_SdtType](./get_sdttype/)() | Liest den Typ dieses **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Gibt ein Tag an, das dem aktuellen SDT‑Knoten zugeordnet ist. Darf nicht null sein. |
| virtual [get_Title](./get_title/)() const | Gibt den benutzerfreundlichen Namen an, der mit diesem **SDT** verknüpft ist. Darf nicht null sein. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Liest einen String, der das XML darstellt, das im Knoten im [FlatOpc](../../aspose.words/saveformat/)‑Format enthalten ist. |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Liest ein Objekt, das die Zuordnung dieses strukturierten Dokument-Tags zu XML‑Daten in einem benutzerdefinierten XML‑Teil des aktuellen Dokuments darstellt. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Gibt eine Live‑Sammlung von Kindknoten zurück, die den angegebenen Typen entsprechen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Entfernt nur diesen SDT‑Knoten selbst, lässt jedoch den Inhalt im Dokumentbaum erhalten. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Setter für [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein strukturiertes Dokument‑Tag entfernt, lässt jedoch den Inhalt erhalten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Diese Sammlung bietet eine einheitliche Schnittstelle zum Zugriff auf bereichsbezogene und nicht bereichsbezogene strukturierte Tags.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Hier können wir Kindknoten über die gemeinsame Schnittstelle von bereichsbezogenen und nicht bereichsbezogenen strukturierten Tags abrufen.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
