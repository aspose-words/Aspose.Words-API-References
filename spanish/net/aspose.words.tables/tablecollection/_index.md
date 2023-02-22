---
title: Class TableCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Tables.TableCollection clase. Proporciona acceso escrito a una colección deTable nodos.
type: docs
weight: 6060
url: /es/net/aspose.words.tables/tablecollection/
---
## TableCollection class

Proporciona acceso escrito a una colección de[`Table`](../table/) nodos.

```csharp
public class TableCollection : NodeCollection
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Obtiene el número de nodos de la colección. |
| [Item](../../aspose.words.tables/tablecollection/item/) { get; } | Recupera un **Mesa** en el índice dado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Agrega un nodo al final de la colección. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Elimina todos los nodos de esta colección y del documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Determina si un nodo está en la colección. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Proporciona una iteración de estilo "foreach" simple sobre la colección de nodos. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Devuelve el índice de base cero del nodo especificado. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Inserta un nodo en la colección en el índice especificado. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Elimina el nodo de la colección y del documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Elimina el nodo en el índice especificado de la colección y del documento. |
| [ToArray](../../aspose.words.tables/tablecollection/toarray/#toarray_1)() | Copia todas las tablas de la colección a una nueva matriz de tablas. (2 methods) |

### Ejemplos

Muestra cómo eliminar la primera y la última fila de todas las tablas de un documento.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(5, tables[0].Rows.Count);
Assert.AreEqual(4, tables[1].Rows.Count);

foreach (Table table in tables.OfType<Table>())
{
    table.FirstRow?.Remove();
    table.LastRow?.Remove();
}

Assert.AreEqual(3, tables[0].Rows.Count);
Assert.AreEqual(2, tables[1].Rows.Count);
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

        // Averigüe si alguna celda de la tabla tiene otras tablas como hijos.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Averigüe si la tabla está anidada dentro de otra tabla y, de ser así, a qué profundidad.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcula a qué nivel está anidada una tabla dentro de otras tablas.
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

* class [NodeCollection](../../aspose.words/nodecollection/)
* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)


