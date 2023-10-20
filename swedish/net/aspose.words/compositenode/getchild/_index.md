---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words för .NET
description: CompositeNode GetChild metod. Returnerar en Nte underordnad nod som matchar den angivna typen i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Returnerar en N:te underordnad nod som matchar den angivna typen.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nodeType | NodeType | Anger typen av underordnad nod. |
| index | Int32 | Nollbaserat index för den underordnade noden att välja. Negativa index är också tillåtna och indikerar åtkomst från slutet, det vill säga -1 betyder den sista noden. |
| isDeep | Boolean | `Sann` för att välja från alla underordnade noder rekursivt; `falsk`att endast välja bland närmaste barn. Se anmärkningar för mer info. |

### Returvärde

Den underordnade noden som matchar kriterierna eller`null` om ingen matchande nod hittas.

## Anmärkningar

Om index ligger utanför intervallet, a`null` returneras.

Observera att uppmärkningsnoder (StructuredDocumentTag ochSmartTag ) korsas även när*isDeep* =`falsk` och`GetChild` anropas för non-markup nodtyp. Till exempel om den första körningen i en para är inslagen i en[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , kommer den fortfarande att returneras av`GetChild`(Run , 0,`falsk`).

## Exempel

Visar hur man tillämpar egenskaperna för en tabells stil direkt på tabellens element.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Den här metoden gäller tabellstilsegenskaper som de vi ställt in ovan.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

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

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
