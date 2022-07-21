---
title: GetAncestor
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene el primer ancestro del tipo de objeto especificado.
type: docs
weight: 110
url: /es/net/aspose.words/node/getancestor/
---
## GetAncestor(Type) {#getancestor_1}

Obtiene el primer ancestro del tipo de objeto especificado.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| ancestorType | Type | El tipo de objeto del ancestro a recuperar. |

### Valor_devuelto

El antepasado del tipo especificado o nulo si no se encontró ningún antepasado de este tipo.

### Observaciones

El tipo de antepasado coincide si es igual a ancestorType o se deriva de ancestorType.

### Ejemplos

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

* class [CompositeNode](../../compositenode)
* class [Node](../../node)
* espacio de nombres [Aspose.Words](../../node)
* asamblea [Aspose.Words](../../../)

---

## GetAncestor(NodeType) {#getancestor}

Obtiene el primer ancestro del especificado[`NodeType`](../../nodetype) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| ancestorType | NodeType | El tipo de nodo del ancestro a recuperar. |

### Valor_devuelto

El antepasado del tipo especificado o nulo si no se encontró ningún antepasado de este tipo.

### Ejemplos

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

* class [CompositeNode](../../compositenode)
* enum [NodeType](../../nodetype)
* class [Node](../../node)
* espacio de nombres [Aspose.Words](../../node)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
