---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.NodeType för att enkelt identifiera och hantera olika nodtyper i Word-dokument för sömlös dokumentbehandling.
type: docs
weight: 4920
url: /sv/net/aspose.words/nodetype/
---
## NodeType enumeration

Anger typen av nod i ett Word-dokument.

```csharp
public enum NodeType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Any | `0` | Indikerar alla nodtyper. Tillåter att välja alla underordnade nodtyper. |
| Document | `1` | En[`Document`](../document/) objekt som, som roten till dokumentträdet, ger åtkomst till hela Word-dokumentet. |
| Section | `2` | En[`Section`](../section/) objekt som motsvarar ett avsnitt i ett Word-dokument. |
| Body | `3` | En[`Body`](../body/) objekt som innehåller huvudtexten i ett avsnitt (huvudtextberättelse). |
| HeaderFooter | `4` | En[`HeaderFooter`](../headerfooter/) objekt som innehåller texten från ett visst sidhuvud eller en sidfot inuti ett avsnitt. |
| Table | `5` | En[`Table`](../../aspose.words.tables/table/) objekt som representerar en tabell i ett Word-dokument. |
| Row | `6` | En rad av ett bord. |
| Cell | `7` | En cell i en tabellrad. |
| Paragraph | `8` | Ett textstycke. |
| BookmarkStart | `9` | En början på en bokmärkesmarkör. |
| BookmarkEnd | `10` | Änden av en bokmärkesmarkör. |
| EditableRangeStart | `11` | En början på ett redigerbart område. |
| EditableRangeEnd | `12` | Slutet på ett redigerbart intervall. |
| MoveFromRangeStart | `13` | En början på ett MoveFrom-intervall. |
| MoveFromRangeEnd | `14` | Slutet på ett MoveFrom-intervall. |
| MoveToRangeStart | `15` | En början på ett Flytta till-intervall. |
| MoveToRangeEnd | `16` | Slutet på ett Flytta till-intervall. |
| GroupShape | `17` | En grupp av former, bilder, OLE-objekt eller andra gruppformer. |
| Shape | `18` | Ett ritobjekt, till exempel en OfficeArt-form, bild eller ett OLE-objekt. |
| Comment | `19` | En kommentar i ett Word-dokument. |
| Footnote | `20` | En fotnot eller slutnot i ett Word-dokument. |
| Run | `21` | En rad texter. |
| FieldStart | `22` | Ett specialtecken som anger början av ett Word-fält. |
| FieldSeparator | `23` | Ett specialtecken som separerar fältkoden från fältresultatet. |
| FieldEnd | `24` | Ett specialtecken som anger slutet på ett Word-fält. |
| FormField | `25` | Ett formulärfält. |
| SpecialChar | `26` | Ett specialtecken som inte är en av de mer specifika specialteckentyperna. |
| SmartTag | `27` | En smart tagg runt en eller flera inline-strukturer (sekvenser, bilder, fält etc.) i ett stycke |
| StructuredDocumentTag | `28` | Gör det möjligt att definiera kundspecifik information och hur den ska presenteras. |
| StructuredDocumentTagRangeStart | `29` | En början på**avståndsbestämd** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. |
| StructuredDocumentTagRangeEnd | `30` | Ett slut på**avståndsbestämd** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. |
| GlossaryDocument | `31` | Ett ordlistadokument inom huvuddokumentet. |
| BuildingBlock | `32` | En byggsten i ett ordlistedokument (t.ex. en post i ett ordlistedokument). |
| CommentRangeStart | `33` | En markörnod som representerar början på ett kommenterat intervall. |
| CommentRangeEnd | `34` | En markörnod som representerar slutet på ett kommenterat intervall. |
| OfficeMath | `35` | Ett Office Math-objekt. Kan vara en ekvation, funktion, matris eller ett annat matematiskt objekt. Kan vara en samling matematiska objekt och kan även innehålla vissa icke-matematiska objekt, såsom textsekvenser. |
| SubDocument | `36` | En deldokumentnod som är en länk till ett annat dokument. |
| System | `37` | Reserverad för internt bruk av Aspose.Words. |
| Null | `38` | Reserverad för internt bruk av Aspose.Words. |

## Exempel

Visar hur man navigerar genom en sammansatt nods samling av underordnade noder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast finns under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av omedelbara underordnade,
// och skriv ut alla körningar eller former som vi hittar inuti.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
