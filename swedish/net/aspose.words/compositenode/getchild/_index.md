---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words för .NET
description: Upptäck CompositeNode GetChild-metoden för att enkelt hämta den N:te undernoden av en specifik typ, vilket förbättrar effektiviteten i din datahantering.
type: docs
weight: 100
url: /sv/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Returnerar en N:te underordnad nod som matchar den angivna typen.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| nodeType | NodeType | Anger typen av undernoden. |
| index | Int32 | Nollbaserat index för den underordnade noden att välja. Negativa index är också tillåtna och indikerar åtkomst från slutet, det vill säga -1 betyder den sista noden. |
| isDeep | Boolean | `sann` att välja rekursivt från alla underordnade noder; `falsk` att endast välja bland direkta underordnade objekt. Se kommentarer för mer information. |

### Returvärde

Den underordnade noden som matchar kriterierna eller`null` om ingen matchande nod hittas.

## Anmärkningar

Om indexet är utanför intervallet, a`null` returneras.

Observera att markupnoder (StructuredDocumentTag ochSmartTag ) passeras även när*isDeep* =`falsk` och`GetChild` anropas för nodtyper utan markup. Till exempel om den första körningen i en para är inkapslad i en[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , den kommer fortfarande att returneras av`GetChild`(Run , 0,`falsk`).

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

// Den här metoden avser tabellstilsegenskaper som de vi angav ovan.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

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

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
