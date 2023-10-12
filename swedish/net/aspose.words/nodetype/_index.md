---
title: Enum NodeType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.NodeType uppräkning. Anger typen av en Worddokumentnod.
type: docs
weight: 4230
url: /sv/net/aspose.words/nodetype/
---
## NodeType enumeration

Anger typen av en Word-dokumentnod.

```csharp
public enum NodeType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Any | `0` | Indikerar alla nodtyper. Tillåter att välja alla barn. |
| Document | `1` | A[`Document`](../document/) objekt som, som roten till dokumentträdet, ger åtkomst till hela Word-dokumentet. |
| Section | `2` | A[`Section`](../section/) objekt som motsvarar ett avsnitt i ett Word-dokument. |
| Body | `3` | A[`Body`](../body/) objekt som innehåller huvudtexten i ett avsnitt (huvudtextberättelse). |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter/) objekt som innehåller text från en viss sidhuvud eller sidfot i ett avsnitt. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table/) objekt som representerar en tabell i ett Word-dokument. |
| Row | `6` | En rad av ett bord. |
| Cell | `7` | En cell i en tabellrad. |
| Paragraph | `8` | Ett stycke text. |
| BookmarkStart | `9` | En början på en bokmärkesmarkör. |
| BookmarkEnd | `10` | Slutet på en bokmärkesmarkör. |
| EditableRangeStart | `11` | En början på ett redigerbart område. |
| EditableRangeEnd | `12` | Slutet på ett redigerbart intervall. |
| MoveFromRangeStart | `13` | En början på ett MoveFrom-intervall. |
| MoveFromRangeEnd | `14` | Slutet på ett MoveFrom-intervall. |
| MoveToRangeStart | `15` | En början på ett MoveTo-intervall. |
| MoveToRangeEnd | `16` | Slutet på ett MoveTo-intervall. |
| GroupShape | `17` | En grupp av former, bilder, OLE-objekt eller andra gruppformer. |
| Shape | `18` | Ett ritobjekt, till exempel en OfficeArt-form, bild eller ett OLE-objekt. |
| Comment | `19` | En kommentar i ett Word-dokument. |
| Footnote | `20` | En fotnot eller slutnot i ett Word-dokument. |
| Run | `21` | En rad text. |
| FieldStart | `22` | Ett specialtecken som anger början av ett Word-fält. |
| FieldSeparator | `23` | Ett specialtecken som skiljer fältkoden från fältresultatet. |
| FieldEnd | `24` | Ett specialtecken som anger slutet på ett Word-fält. |
| FormField | `25` | Ett formulärfält. |
| SpecialChar | `26` | Ett specialtecken som inte är en av de mer specifika specialteckentyperna. |
| SmartTag | `27` | En smart tagg runt en eller flera inline-strukturer (körningar, bilder, fält, etc.) i ett stycke |
| StructuredDocumentTag | `28` | Tillåter att definiera kundspecifik information och dess presentationssätt. |
| StructuredDocumentTagRangeStart | `29` | En början på **varierade** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. |
| StructuredDocumentTagRangeEnd | `30` | Ett slut på **varierade** strukturerad dokumenttagg som accepterar innehåll i flera sektioner. |
| GlossaryDocument | `31` | Ett ordlistadokument i huvuddokumentet. |
| BuildingBlock | `32` | En byggsten i ett ordlistadokument (t.ex. ordlistadokument). |
| CommentRangeStart | `33` | En markörnod som representerar början av ett kommenterat område. |
| CommentRangeEnd | `34` | En markörnod som representerar slutet av ett kommenterat område. |
| OfficeMath | `35` | Ett Office Math-objekt. Kan vara ekvation, funktion, matris eller något av andra matematiska objekt. Kan vara en samling matematiska objekt och kan även innehålla vissa icke-matematiska objekt som t.ex. |
| SubDocument | `36` | En underdokumentnod som är en länk till ett annat dokument. |
| System | `37` | Reserverad för internt bruk av Aspose.Words. |
| Null | `38` | Reserverad för internt bruk av Aspose.Words. |

### Exempel

Visar hur man går igenom en sammansatt nods samling av undernoder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast existerar under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av närmaste barn,
// och skriv ut alla körningar eller former som vi hittar inom.
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


