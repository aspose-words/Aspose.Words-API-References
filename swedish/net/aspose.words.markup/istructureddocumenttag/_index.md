---
title: IStructuredDocumentTag Interface
linktitle: IStructuredDocumentTag
articleTitle: IStructuredDocumentTag
second_title: Aspose.Words för .NET
description: Aspose.Words.Markup.IStructuredDocumentTag gränssnitt. Gränssnitt för att definiera en gemensam data förStructuredDocumentTag ochStructuredDocumentTagRangeStart  i C#.
type: docs
weight: 3970
url: /sv/net/aspose.words.markup/istructureddocumenttag/
---
## IStructuredDocumentTag interface

Gränssnitt för att definiera en gemensam data för[`StructuredDocumentTag`](../structureddocumenttag/) och[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart/) .

```csharp
public interface IStructuredDocumentTag
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Color](../../aspose.words.markup/istructureddocumenttag/color/) { get; set; } | Hämtar eller ställer in färgen på den strukturerade dokumenttaggen. |
| [Id](../../aspose.words.markup/istructureddocumenttag/id/) { get; } | Anger ett unikt skrivskyddat beständigt numeriskt ID för detta**SDT**. |
| [IsShowingPlaceholderText](../../aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/) { get; set; } | Anger om innehållet i detta**SDT** ska tolkas att innehålla platshållare text (i motsats till vanligt textinnehåll inom SDT). |
| [Level](../../aspose.words.markup/istructureddocumenttag/level/) { get; } | Får nivån på vilken detta**SDT** förekommer i dokumentträdet. |
| [LockContentControl](../../aspose.words.markup/istructureddocumenttag/lockcontentcontrol/) { get; set; } | När den är satt till true kommer den här egenskapen att förbjuda en användare att ta bort detta**SDT** . |
| [LockContents](../../aspose.words.markup/istructureddocumenttag/lockcontents/) { get; set; } | När den är satt till true kommer den här egenskapen att förbjuda en användare att redigera innehållet i denna**SDT** . |
| [Placeholder](../../aspose.words.markup/istructureddocumenttag/placeholder/) { get; } | Får[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)som innehåller platshållartext som ska visas när innehållet i denna SDT-körning är tomt, det associerade mappade XML-elementet är tomt som specificerats via[`XmlMapping`](./xmlmapping/) element eller[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) element är sant. |
| [PlaceholderName](../../aspose.words.markup/istructureddocumenttag/placeholdername/) { get; set; } | Hämtar eller sätter Namn på[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext. |
| [SdtType](../../aspose.words.markup/istructureddocumenttag/sdttype/) { get; } | Får typ av detta**Strukturerad dokumenttagg** . |
| [Tag](../../aspose.words.markup/istructureddocumenttag/tag/) { get; set; } | Anger en tagg som är associerad med den aktuella SDT-noden. Kan inte vara null. |
| [Title](../../aspose.words.markup/istructureddocumenttag/title/) { get; set; } | Anger det vänliga namnet som är associerat med detta**SDT** . Kan inte vara null. |
| [WordOpenXML](../../aspose.words.markup/istructureddocumenttag/wordopenxml/) { get; } | Får en sträng som representerar XML som finns i noden iFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/istructureddocumenttag/xmlmapping/) { get; } | Hämtar ett objekt som representerar mappningen av denna strukturerade dokumenttagg till XML data i en anpassad XML-del av det aktuella dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [IsRanged](../../aspose.words.markup/istructureddocumenttag/isranged/)() | Returnerar sant om denna instans är en strukturerad dokumenttagg med intervall. |
| [StructuredDocumentTagNode](../../aspose.words.markup/istructureddocumenttag/structureddocumenttagnode/)() | Returnerar nodobjekt som implementerar detta gränssnitt. |

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
