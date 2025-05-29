---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Markup.StructuredDocumentTagRangeStart, som möjliggör sömlös innehållshantering med flera sektioner i strukturerade dokument.
type: docs
weight: 4780
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Representerar början på**avståndsbestämd** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. Se även[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Initierar en ny instans av**Startintervall för tagg för strukturerat dokument** klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Appearance](../../aspose.words.markup/structureddocumenttagrangestart/appearance/) { get; set; } | Hämtar eller ställer in utseendet på den strukturerade dokumenttaggen. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Hämtar eller ställer in färgen på den strukturerade dokumenttaggen. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Anger ett unikt skrivskyddat, beständigt numeriskt ID för den här strukturerade dokumenttaggen. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returer`sann` om denna nod kan innehålla andra noder. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Anger om innehållet i den här taggen för strukturerat dokument ska tolkas som att innehålla platshållartext för (i motsats till vanligt textinnehåll i taggen för strukturerat dokument). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Hämtar det sista barnet i stdContent-intervallet. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Hämtar nivån där detta strukturerade dokumenttaggintervall börjar i dokumentträdet. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | När den är inställd på`sann` , den här egenskapen kommer att förhindra att en användare tar bort den här strukturerade dokumenttaggen. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | När den är inställd på`sann` , kommer den här egenskapen att förhindra att en användare redigerar innehållet i den här strukturerade dokumenttaggen. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | ReturerStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Hämtar[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)innehåller platshållartext som ska visas när innehållet i den här strukturerade dokumenttaggen är tomt, det associerade mappade XML-elementet är tomt enligt anvisningarna via[`XmlMapping`](./xmlmapping/) elementet eller[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) elementet är`sann` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Hämtar eller anger namnet på[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) innehåller platshållartext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/)objekt som representerar den del av ett dokument som finns i denna nod. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Anger slutet av intervallet om[`StructuredDocumentTag`](../structureddocumenttag/) är en tagg för strukturerat dokument med intervall. Annars returnerar`null` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Hämtar typen av denna strukturerade dokumenttagg. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Anger en tagg som är associerad med den aktuella noden för strukturerat dokumenttagg. Kan inte`null` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Anger det användarvänliga namnet som är associerat med den här taggen för strukturerat dokument. Kan inte vara`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. |
| [WordOpenXMLMinimal](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxmlminimal/) { get; } | Hämtar en sträng som representerar XML-koden som finns i noden iFlatOpc format. Till skillnad från[`WordOpenXML`](./wordopenxml/) egenskapen genererar den här metoden ett avskalat dokument som exkluderar alla delar som inte är innehållsrelaterade. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggintervall till XML-data i en anpassad XML-del av det aktuella dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tar emot en besökare. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Lägger till den angivna noden i slutet av stdContent-intervallet. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en live-samling av underordnade noder som matchar de angivna typerna. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Ger stöd för iterationen för varje stil över de underordnade noderna till denna nod. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Tar bort alla noder mellan denna startnod för intervallet och slutnoden för intervallet. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Tar bort denna startnod och lämpliga slutnoder för intervallet från den strukturerade dokumenttaggen, men behåller dess innehåll inuti dokumentträdet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |

## Anmärkningar

Kan vara direkt underordnat[`Body`](../../aspose.words/body/) nod**endast** .

## Exempel

Visar hur man hämtar egenskaperna för taggar för strukturerade dokument med flera sektioner.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

StructuredDocumentTagRangeStart rangeStartTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeStart, true)[0] as StructuredDocumentTagRangeStart;
StructuredDocumentTagRangeEnd rangeEndTag =
    doc.GetChildNodes(NodeType.StructuredDocumentTagRangeEnd, true)[0] as StructuredDocumentTagRangeEnd;

Console.WriteLine("StructuredDocumentTagRangeStart values:");
Console.WriteLine($"\t|Id: {rangeStartTag.Id}");
Console.WriteLine($"\t|Title: {rangeStartTag.Title}");
Console.WriteLine($"\t|PlaceholderName: {rangeStartTag.PlaceholderName}");
Console.WriteLine($"\t|IsShowingPlaceholderText: {rangeStartTag.IsShowingPlaceholderText}");
Console.WriteLine($"\t|LockContentControl: {rangeStartTag.LockContentControl}");
Console.WriteLine($"\t|LockContents: {rangeStartTag.LockContents}");
Console.WriteLine($"\t|Level: {rangeStartTag.Level}");
Console.WriteLine($"\t|NodeType: {rangeStartTag.NodeType}");
Console.WriteLine($"\t|RangeEnd: {rangeStartTag.RangeEnd}");
Console.WriteLine($"\t|Color: {rangeStartTag.Color.ToArgb()}");
Console.WriteLine($"\t|SdtType: {rangeStartTag.SdtType}");
Console.WriteLine($"\t|FlatOpcContent: {rangeStartTag.WordOpenXML}");
Console.WriteLine($"\t|Tag: {rangeStartTag.Tag}\n");

Console.WriteLine("StructuredDocumentTagRangeEnd values:");
Console.WriteLine($"\t|Id: {rangeEndTag.Id}");
Console.WriteLine($"\t|NodeType: {rangeEndTag.NodeType}");
```

### Se även

* class [Node](../../aspose.words/node/)
* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
