---
title: StructuredDocumentTagRangeStart Class
linktitle: StructuredDocumentTagRangeStart
articleTitle: StructuredDocumentTagRangeStart
second_title: Aspose.Words för .NET
description: Aspose.Words.Markup.StructuredDocumentTagRangeStart klass. Representerar en början påvarierade strukturerad dokumenttagg som accepterar innehåll i flera sektioner. Se ävenStructuredDocumentTagRangeEnd  i C#.
type: docs
weight: 4090
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class

Representerar en början på**varierade** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. Se även[`StructuredDocumentTagRangeEnd`](../structureddocumenttagrangeend/) .

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class StructuredDocumentTagRangeStart : Node, IEnumerable<Node>, IStructuredDocumentTag
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [StructuredDocumentTagRangeStart](structureddocumenttagrangestart/)(*[DocumentBase](../../aspose.words/documentbase/), [SdtType](../sdttype/)*) | Initierar en ny instans av**Structured document tag range start** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/childnodes/) { get; } | Hämtar alla noder mellan denna intervallstartnod och intervallslutnoden. |
| [Color](../../aspose.words.markup/structureddocumenttagrangestart/color/) { get; set; } | Hämtar eller ställer in färgen på den strukturerade dokumenttaggen. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [Id](../../aspose.words.markup/structureddocumenttagrangestart/id/) { get; } | Anger ett unikt skrivskyddat beständigt numeriskt ID för denna strukturerade dokumenttagg. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returnerar`Sann` om denna nod kan innehålla andra noder. |
| [IsShowingPlaceholderText](../../aspose.words.markup/structureddocumenttagrangestart/isshowingplaceholdertext/) { get; set; } | Anger om innehållet i denna strukturerade dokumenttagg ska tolkas till att innehålla platshållartext (i motsats till vanligt textinnehåll i den strukturerade dokumenttaggen). |
| [LastChild](../../aspose.words.markup/structureddocumenttagrangestart/lastchild/) { get; } | Får det sista barnet i stdContent-intervallet. |
| [Level](../../aspose.words.markup/structureddocumenttagrangestart/level/) { get; } | Hämtar nivån på vilken detta strukturerade dokumenttaggintervall startar i dokumentträdet. |
| [LockContentControl](../../aspose.words.markup/structureddocumenttagrangestart/lockcontentcontrol/) { get; set; } | När inställd på`Sann` , kommer den här egenskapen att förbjuda en användare från att ta bort den här strukturerade dokumenttaggen. |
| [LockContents](../../aspose.words.markup/structureddocumenttagrangestart/lockcontents/) { get; set; } | När inställd på`Sann` , kommer den här egenskapen att förbjuda en användare från att redigera innehållet i denna strukturerade dokumenttagg. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangestart/nodetype/) { get; } | ReturnerarStructuredDocumentTagRangeStart . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [Placeholder](../../aspose.words.markup/structureddocumenttagrangestart/placeholder/) { get; } | Får[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/)som innehåller platshållartext som ska visas när denna strukturerade dokumenttaggkörningsinnehåll är tomt, är det associerade mappade XML-elementet tomt som specificerat via[`XmlMapping`](./xmlmapping/) element eller[`IsShowingPlaceholderText`](./isshowingplaceholdertext/) element är`Sann` . |
| [PlaceholderName](../../aspose.words.markup/structureddocumenttagrangestart/placeholdername/) { get; set; } | Hämtar eller sätter Namn på[`BuildingBlock`](../../aspose.words.buildingblocks/buildingblock/) som innehåller platshållartext. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../../aspose.words/range/) objekt som representerar den del av ett dokument som finns i denna nod. |
| [RangeEnd](../../aspose.words.markup/structureddocumenttagrangestart/rangeend/) { get; } | Anger slutet av intervallet om[`StructuredDocumentTag`](../structureddocumenttag/) är en strukturerad dokumenttagg med intervall. Returnerar annars`null` . |
| [SdtType](../../aspose.words.markup/structureddocumenttagrangestart/sdttype/) { get; } | Får typ av denna strukturerade dokumenttagg. |
| [Tag](../../aspose.words.markup/structureddocumenttagrangestart/tag/) { get; set; } | Anger en tagg som är associerad med den nuvarande strukturerade dokumenttaggnoden. Kan inte vara`null` . |
| [Title](../../aspose.words.markup/structureddocumenttagrangestart/title/) { get; set; } | Anger det vänliga namnet som är kopplat till denna strukturerade dokumenttagg. Kan inte`null` . |
| [WordOpenXML](../../aspose.words.markup/structureddocumenttagrangestart/wordopenxml/) { get; } | Får en sträng som representerar XML som finns i noden iFlatOpc format. |
| [XmlMapping](../../aspose.words.markup/structureddocumenttagrangestart/xmlmapping/) { get; } | Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggintervall till XML data i en anpassad XML-del av det aktuella dokumentet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangestart/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accepterar en besökare. |
| [AppendChild](../../aspose.words.markup/structureddocumenttagrangestart/appendchild/)(*[Node](../../aspose.words/node/)*) | Lägger till den angivna noden i slutet av stdContent-intervallet. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| [GetChildNodes](../../aspose.words.markup/structureddocumenttagrangestart/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Returnerar en livesamling av underordnade noder som matchar de angivna typerna. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagrangestart/getenumerator/)() | Tillhandahåller stöd för varje stiliteration över undernoderna för denna nod. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Hämtar texten för denna nod och alla dess underordnade. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveAllChildren](../../aspose.words.markup/structureddocumenttagrangestart/removeallchildren/)() | Tar bort alla noder mellan denna intervallstartnod och intervallslutnoden. |
| [RemoveSelfOnly](../../aspose.words.markup/structureddocumenttagrangestart/removeselfonly/)() | Tar bort det här intervallets start- och lämpliga intervallslutnoder för den strukturerade dokumenttaggen, men behåller dess innehåll i dokumentträdet. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

## Anmärkningar

Kan vara omedelbart barn till[`Body`](../../aspose.words/body/) nod**endast** .

## Exempel

Visar hur du får egenskaperna för strukturerade dokumenttaggar med flera sektioner.

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
