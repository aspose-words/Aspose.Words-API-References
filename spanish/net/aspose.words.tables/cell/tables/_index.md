---
title: Cell.Tables
second_title: Referencia de API de Aspose.Words para .NET
description: Cell propiedad. Obtiene una colección de tablas que son hijas inmediatas de la celda.
type: docs
weight: 120
url: /es/net/aspose.words.tables/cell/tables/
---
## Cell.Tables property

Obtiene una colección de tablas que son hijas inmediatas de la celda.

```csharp
public TableCollection Tables { get; }
```

### Ejemplos

Muestra cómo saber si una tabla está anidada.

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
/// Un número entero que indica la profundidad de anidamiento de la tabla (número de nodos de la tabla principal).
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
/// No recorra recursivamente esas tablas para buscar más tablas.
/// </summary>
/// <returns>
/// Devuelve verdadero si al menos una celda secundaria contiene una tabla.
/// Devuelve falso si ninguna celda de la tabla contiene una tabla.
/// </returns>
private static int GetChildTableCount(Table table)
{
    int childTableCount = 0;

    foreach (Row row in table.Rows.OfType<Row>())
    {
        foreach (Cell Cell in row.Cells.OfType<Cell>())
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

* class [TableCollection](../../tablecollection/)
* class [Cell](../)
* espacio de nombres [Aspose.Words.Tables](../../cell/)
* asamblea [Aspose.Words](../../../)


