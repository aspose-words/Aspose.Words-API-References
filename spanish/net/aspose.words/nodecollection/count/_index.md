---
title: NodeCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad NodeCollection Count para acceder fácilmente al número total de nodos en su colección, mejorando la gestión y la eficiencia de los datos.
type: docs
weight: 10
url: /es/net/aspose.words/nodecollection/count/
---
## NodeCollection.Count property

Obtiene el número de nodos en la colección.

```csharp
public int Count { get; }
```

## Ejemplos

Muestra cómo recorrer la colección de nodos secundarios de un nodo compuesto.

```csharp
Document doc = new Document();

// Agregue dos ejecuciones y una forma como nodos secundarios al primer párrafo de este documento.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Tenga en cuenta que 'CustomNodeId' no se guarda en un archivo de salida y solo existe durante la vida útil del nodo.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterar a través de la colección de hijos inmediatos del párrafo,
// e imprimir cualquier recorrido o forma que encontremos dentro.
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

Muestra cómo averiguar si las tablas están anidadas.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Descubra si alguna celda de la tabla tiene otras tablas como hijas.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Descubra si la tabla está anidada dentro de otra tabla y, de ser así, a qué profundidad.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcula en qué nivel está anidada una tabla dentro de otras tablas.
/// </summary>
/// <returns>
/// Un entero que indica la profundidad de anidación de la tabla (número de nodos de la tabla principal).
/// </returns>
private static int GetNestedDepthOfTable(Table table)
{
    int depth = 0;
    Node parent = table.GetAncestor(table.NodeType);

    while (parent != null)
    {
        depth++;
        parent = parent.GetAncestor(typeof(Table));
    }

    return depth;
}

/// <summary>
/// Determina si una tabla contiene alguna tabla secundaria inmediata dentro de sus celdas.
/// No recorra recursivamente esas tablas para buscar otras tablas.
/// </summary>
/// <returns>
/// Devuelve verdadero si al menos una celda secundaria contiene una tabla.
/// Devuelve falso si ninguna celda en la tabla contiene una tabla.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows)
    {
        foreach (Cell Cell in row.Cells)
        {
            TableCollection childTables = Cell.Tables;

            if (childTables.Count > 0)
                childTableCount++;
        }
    }

    return childTableCount;
}
```

### Ver también

* class [NodeCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
