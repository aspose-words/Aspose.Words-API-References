---
title: CompositeNode.GetChild
second_title: Referencia de API de Aspose.Words para .NET
description: CompositeNode método. Devuelve un enésimo nodo secundario que coincide con el tipo especificado.
type: docs
weight: 100
url: /es/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Devuelve un enésimo nodo secundario que coincide con el tipo especificado.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| nodeType | NodeType | Especifica el tipo de nodo secundario. |
| index | Int32 | Índice de base cero del nodo secundario a seleccionar. También se permiten índices negativos e indican acceso desde el final, es decir -1 significa el último nodo. |
| isDeep | Boolean | `verdadero` para seleccionar de todos los nodos secundarios de forma recursiva; `FALSO`para seleccionar sólo entre los hijos inmediatos. Ver comentarios para más información. |

### Valor_devuelto

El nodo hijo que coincide con los criterios o`nulo` si no se encuentra ningún nodo coincidente.

### Observaciones

Si el índice está fuera de rango, un`nulo` es regresado.

Tenga en cuenta que los nodos de marcado (StructuredDocumentTag ySmartTag ) se recorren incluso cuando*isDeep* =`FALSO` y`GetChild` se invoca para el tipo de nodo sin marcado. Por ejemplo, si la primera ejecución en para está envuelta en un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , todavía será devuelto por`GetChild`(Run , 0,`FALSO`).

### Ejemplos

Muestra cómo aplicar las propiedades del estilo de una tabla directamente a los elementos de la tabla.

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

// Este método se refiere a propiedades de estilo de tabla como las que configuramos anteriormente.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Muestra cómo recorrer la colección de nodos secundarios de un nodo compuesto.

```csharp
Document doc = new Document();

// Agregue dos ejecuciones y una forma como nodos secundarios al primer párrafo de este documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Tenga en cuenta que 'CustomNodeId' no se guarda en un archivo de salida y existe solo durante la vida útil del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterar a través de la colección de hijos inmediatos del párrafo,
// e imprimir cualquier corrida o forma que encontremos dentro.
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

### Ver también

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* espacio de nombres [Aspose.Words](../../compositenode/)
* asamblea [Aspose.Words](../../../)


