---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words för .NET
description: Utforska gränssnittet Aspose.Words.Markup.IStructuredDocumentTag för effektiv hantering av strukturerade dokumenttaggar och förbättra din dokumenthantering idag!
type: docs
weight: 4660
url: /sv/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Gränssnitt för att definiera gemensamma data för[`StructuredDocumentTag`](../structureddocumenttag/) och[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Appearance](../../aspose.words.markup/istructureddocumenttag/appearance/) { get; set; } | Hämtar eller ställer in utseendet på den strukturerade dokumenttaggen. |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Hämtar eller ställer in färgen på den strukturerade dokumenttaggen. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Anger ett unikt skrivskyddat, beständigt numeriskt ID för detta**SDT**. |
| [IsMultiSection](../../aspose.words.markup/istructureddocumenttag/ismultisection/) { get; } | Returnerar sant om den här instansen är en strukturerad dokumenttagg med varierande intervall (flera sektioner). |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Anger om innehållet i detta**SDT** ska tolkas som att innehålla platshållaren text (i motsats till vanligt textinnehåll inom SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Hämtar nivån vid vilken detta**SDT** förekommer i dokumentträdet. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | När den här egenskapen är satt till sant förhindrar den en användare från att ta bort detta**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | När den här egenskapen är satt till sant förhindrar den en användare att redigera innehållet i detta**SDT** . |
| [Node](../../aspose.words.markup/istructureddocumenttag/node/) { get; } | Returnerar nodobjektet som implementerar detta gränssnitt. |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Hämtar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext som ska visas när innehållet i denna SDT-körning är tomt, det associerade mappade XML-elementet är tomt enligt anvisningarna via[`XmlMapping`](./xmlmapping/) element eller[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) elementet är sant. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Hämtar eller anger namnet på[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Hämtar typ av detta**Tagg för strukturerat dokument** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Anger en tagg som är associerad med den aktuella SDT-noden. Kan inte vara null. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Anger det användarvänliga namnet som är associerat med detta**SDT** . Kan inte vara null. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Hämtar ett objekt som representerar mappningen av denna strukturerade dokumenttagg till XML-data i en anpassad XML-del av det aktuella dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetChildNodes](../../aspose.words.markup/istructureddocumenttag/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar de angivna typerna. |
| [RemoveSelfOnly](../../aspose.words.markup/istructureddocumenttag/removeselfonly/)() | Tar bort endast denna SDT-nod, men behåller dess innehåll i dokumentträdet. |

## Exempel

Visar hur man tar bort taggen för strukturerat dokument, men behåller innehållet inuti.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Denna samling tillhandahåller ett enhetligt gränssnitt för åtkomst till strukturerade taggar med och utan intervall.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Här kan vi hämta underordnade noder från det gemensamma gränssnittet för strukturerade taggar med och utan intervall.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
