---
title: StructuredDocumentTagRangeEnd
second_title: Aspose.Words för .NET API Referens
description: Representerar ett slut på varierade strukturerad dokumenttagg som accepterar innehåll i flera sektioner. Se ävenStructuredDocumentTagRangeStart./structureddocumenttagrangestart nod.
type: docs
weight: 3840
url: /sv/net/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class

Representerar ett slut på **varierade** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. Se även[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart) nod.

```csharp
public class StructuredDocumentTagRangeEnd : Node
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [StructuredDocumentTagRangeEnd](structureddocumenttagrangeend)(DocumentBase, int) | Initierar en ny instans av **Slut på intervall för strukturerade dokumenttaggar** class. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document) { get; } | Hämtar dokumentet som denna nod tillhör. |
| [Id](../../aspose.words.markup/structureddocumenttagrangeend/id) { get; } | Anger ett unikt skrivskyddat beständigt numeriskt ID för detta **StructuredDocumentTagRange** node. Motsvarande[`StructuredDocumentTagRangeStart`](../structureddocumenttagrangestart) noden har samma[`Id`](../structureddocumenttagrangestart/id) . |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Returnerar sant om denna nod kan innehålla andra noder. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Hämtar noden omedelbart efter denna nod. |
| override [NodeType](../../aspose.words.markup/structureddocumenttagrangeend/nodetype) { get; } |  |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Accept](../../aspose.words.markup/structureddocumenttagrangeend/accept)(DocumentVisitor) |  |
| [Clone](../../aspose.words/node/clone)(bool) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| virtual [GetText](../../aspose.words/node/gettext)() | Hämtar texten för denna nod och alla dess underordnade. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |

### Anmärkningar

Kan vara omedelbart barn till[`Body`](../../aspose.words/body) nod **endast** .

### Exempel

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

* class [Node](../../aspose.words/node)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
