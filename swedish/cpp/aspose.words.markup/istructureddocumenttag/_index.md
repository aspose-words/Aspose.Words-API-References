---
title: "Aspose::Words::Markup::IStructuredDocumentTag gränssnitt"
linktitle: "IStructuredDocumentTag"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::IStructuredDocumentTag gränssnitt. Gränssnitt för att definiera gemensam data för StructuredDocumentTag och StructuredDocumentTagRangeStart i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface


Gränssnitt för att definiera gemensam data för [StructuredDocumentTag](../structureddocumenttag/) och [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).

```cpp
class IStructuredDocumentTag : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [get_Appearance](./get_appearance/)() | Hämtar eller anger utseendet på den strukturerade dokumenttaggen. |
| virtual [get_Color](./get_color/)() | Hämtar eller anger färgen på den strukturerade dokumenttaggen. |
| virtual [get_Id](./get_id/)() | Anger ett unikt skrivskyddat bestående numeriskt Id för denna **SDT**. |
| virtual [get_IsMultiSection](./get_ismultisection/)() | Returnerar true om detta objekt är en räckvidds‑ (flersektions) strukturerad dokumenttagg. |
| virtual [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() | Anger om innehållet i denna **SDT** ska tolkas som att det innehåller platshållartext (i motsats till vanlig textinnehåll inom SDT). Om den sätts till true återupptas detta tillstånd (visar platshållartext) när dokumentet öppnas. |
| virtual [get_Level](./get_level/)() const | Hämtar nivån där denna **SDT** förekommer i dokumentträdet. |
| virtual [get_LockContentControl](./get_lockcontentcontrol/)() | När den sätts till true kommer denna egenskap att förhindra en användare från att ta bort denna **SDT**. |
| virtual [get_LockContents](./get_lockcontents/)() | När den sätts till true kommer denna egenskap att förhindra en användare från att redigera innehållet i denna **SDT**. |
| virtual [get_Node](./get_node/)() | Returnerar [Node](../../aspose.words/node/)‑objekt som implementerar detta gränssnitt. |
| virtual [get_Placeholder](./get_placeholder/)() | Hämtar [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext som ska visas när innehållet i detta SDT‑kör är tomt, det associerade mappade XML‑elementet är tomt enligt vad som anges via [XmlMapping](./get_xmlmapping/)-elementet eller [IsShowingPlaceholderText](./get_isshowingplaceholdertext/)-elementet är true. |
| virtual [get_PlaceholderName](./get_placeholdername/)() | Hämtar eller anger namn på [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext. |
| virtual [get_SdtType](./get_sdttype/)() | Hämtar typ av denna **Structured document tag**. |
| virtual [get_Tag](./get_tag/)() const | Anger en tagg som är associerad med den aktuella SDT‑noden. Kan inte vara null. |
| virtual [get_Title](./get_title/)() const | Anger det vänliga namnet som är associerat med denna **SDT**. Kan inte vara null. |
| virtual [get_WordOpenXML](./get_wordopenxml/)() | Hämtar en sträng som representerar XML som finns i noden i [FlatOpc](../../aspose.words/saveformat/) formatet. |
| virtual [get_XmlMapping](./get_xmlmapping/)() | Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttagg till XML-data i en anpassad XML-del av det aktuella dokumentet. |
| virtual [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) | Returnerar en levande samling av undernoder som matchar de angivna typerna. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RemoveSelfOnly](./removeselfonly/)() | Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet. |
| virtual [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_Appearance](./get_appearance/). |
| virtual [set_Color](./set_color/)(System::Drawing::Color) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_Color](./get_color/). |
| virtual [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| virtual [set_LockContentControl](./set_lockcontentcontrol/)(bool) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl](./get_lockcontentcontrol/). |
| virtual [set_LockContents](./set_lockcontents/)(bool) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_LockContents](./get_lockcontents/). |
| virtual [set_PlaceholderName](./set_placeholdername/)(System::String) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_PlaceholderName](./get_placeholdername/). |
| virtual [set_Tag](./set_tag/)(System::String) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_Tag](./get_tag/). |
| virtual [set_Title](./set_title/)(System::String) | Sättare för [Aspose::Words::Markup::IStructuredDocumentTag::get_Title](./get_title/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man tar bort strukturerad dokumenttagg, men behåller innehållet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Denna samling tillhandahåller ett enhetligt gränssnitt för åtkomst till räckvidds- och icke‑räckviddsstrukturerade taggar.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Här kan vi hämta undernoder från det gemensamma gränssnittet för räckvidds- och icke‑räckviddsstrukturerade taggar.
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

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
