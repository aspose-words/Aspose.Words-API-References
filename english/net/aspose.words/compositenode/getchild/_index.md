---
title: CompositeNode.GetChild
linktitle: GetChild
second_title: Aspose.Words for .NET API Reference
description: CompositeNode GetChild method. Returns an Nth child node that matches the specified type in C#.
type: docs
weight: 90
url: /net/aspose.words/compositenode/getchild/
---
## GetChild method

Returns an Nth child node that matches the specified type.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | NodeType | Specifies the type of the child node. |
| index | Int32 | Zero based index of the child node to select. Negative indexes are also allowed and indicate access from the end, that is -1 means the last node. |
| isDeep | Boolean | `true` to select from all child nodes recursively; `false` to select only among immediate children. See remarks for more info. |

### Return Value

The child node that matches the criteria or `null` if no matching node is found.

## Remarks

If index is out of range, a `null` is returned.

Note that markup nodes (StructuredDocumentTag and SmartTag) are traversed even when *isDeep* = `false` and `GetChild` is invoked for non-markup node type. For example if the first run in a para is wrapped in a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), it will still be returned by `GetChild`(Run, 0, `false`).

## Examples

Shows how to apply the properties of a table's style directly to the table's elements.

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

// This method concerns table style properties such as the ones we set above.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Shows how to traverse through a composite node's collection of child nodes.

```csharp
Document doc = new Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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

### See Also

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
