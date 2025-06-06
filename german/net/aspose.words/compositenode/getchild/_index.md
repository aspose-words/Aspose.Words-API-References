---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompositeNode GetChild-Methode, um einfach den N-ten untergeordneten Knoten eines bestimmten Typs abzurufen und so die Effizienz Ihrer Datenverwaltung zu steigern.
type: docs
weight: 100
url: /de/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| nodeType | NodeType | Gibt den Typ des untergeordneten Knotens an. |
| index | Int32 | Nullbasierter Index des auszuwählenden untergeordneten Knotens. Negative Indizes sind ebenfalls zulässig und zeigen den Zugriff vom Ende an, d. h. -1 bedeutet den letzten Knoten. |
| isDeep | Boolean | `WAHR` um rekursiv aus allen untergeordneten Knoten auszuwählen; `FALSCH` um nur unter unmittelbaren Kindern auszuwählen. Weitere Informationen finden Sie in den Anmerkungen. |

### Rückgabewert

Der untergeordnete Knoten, der den Kriterien entspricht oder`null` wenn kein passender Knoten gefunden wird.

## Bemerkungen

Wenn der Index außerhalb des Bereichs liegt,`null` wird zurückgegeben.

Beachten Sie, dass Markup-Knoten (StructuredDocumentTag UndSmartTag ) werden durchlaufen, auch wenn*isDeep* =`FALSCH` Und`GetChild` wird für Nicht-Markup-Knotentypen aufgerufen. Wenn beispielsweise der erste Lauf in einem para in einen[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , es wird immer noch zurückgegeben durch`GetChild`(Run , 0,`FALSCH`).

## Beispiele

Zeigt, wie die Eigenschaften des Stils einer Tabelle direkt auf die Elemente der Tabelle angewendet werden.

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

// Diese Methode betrifft Tabellenstileigenschaften wie die, die wir oben festgelegt haben.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die „CustomNodeId“ nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durchlaufen Sie die Sammlung der unmittelbar untergeordneten Elemente des Absatzes.
// und drucke alle Läufe oder Formen aus, die wir darin finden.
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

### Siehe auch

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
