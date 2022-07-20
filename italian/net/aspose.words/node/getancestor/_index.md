---
title: GetAncestor
second_title: Aspose.Words per .NET API Reference
description: Ottiene il primo predecessore del tipo di oggetto specificato.
type: docs
weight: 110
url: /it/net/aspose.words/node/getancestor/
---
## GetAncestor(Type) {#getancestor_1}

Ottiene il primo predecessore del tipo di oggetto specificato.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| ancestorType | Type | Il tipo di oggetto dell'antenato da recuperare. |

### Valore di ritorno

L'antenato del tipo specificato o null se non è stato trovato nessun predecessore di questo tipo.

### Osservazioni

Il tipo di predecessore corrisponde se è uguale a ancestorType o derivato da ancestorType.

### Esempi

Mostra come scoprire se una tabella è nidificata.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Scopri se alcune celle nella tabella hanno altre tabelle come figli.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Scopri se la tabella è nidificata all'interno di un'altra tabella e, in tal caso, a quale profondità.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcola a quale livello è nidificata una tabella all'interno di altre tabelle.
/// </summary>
/// <returns>
/// Un numero intero che indica la profondità di annidamento della tabella (numero di nodi della tabella padre).
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
/// Determina se una tabella contiene una tabella figlio immediata all'interno delle sue celle.
/// Non attraversare in modo ricorsivo queste tabelle per cercare altre tabelle.
/// </summary>
/// <returns>
/// Restituisce true se almeno una cella figlio contiene una tabella.
/// Restituisce false se nessuna cella nella tabella contiene una tabella.
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

### Guarda anche

* class [CompositeNode](../../compositenode)
* class [Node](../../node)
* spazio dei nomi [Aspose.Words](../../node)
* assemblea [Aspose.Words](../../../)

---

## GetAncestor(NodeType) {#getancestor}

Ottiene il primo predecessore dell'oggetto specificato[`NodeType`](../../nodetype) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| ancestorType | NodeType | Il tipo di nodo dell'antenato da recuperare. |

### Valore di ritorno

L'antenato del tipo specificato o null se non è stato trovato nessun predecessore di questo tipo.

### Esempi

Mostra come scoprire se una tabella è nidificata.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);

    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Scopri se alcune celle nella tabella hanno altre tabelle come figli.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Scopri se la tabella è nidificata all'interno di un'altra tabella e, in tal caso, a quale profondità.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcola a quale livello è nidificata una tabella all'interno di altre tabelle.
/// </summary>
/// <returns>
/// Un numero intero che indica la profondità di annidamento della tabella (numero di nodi della tabella padre).
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
/// Determina se una tabella contiene una tabella figlio immediata all'interno delle sue celle.
/// Non attraversare in modo ricorsivo queste tabelle per cercare altre tabelle.
/// </summary>
/// <returns>
/// Restituisce true se almeno una cella figlio contiene una tabella.
/// Restituisce false se nessuna cella nella tabella contiene una tabella.
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

### Guarda anche

* class [CompositeNode](../../compositenode)
* enum [NodeType](../../nodetype)
* class [Node](../../node)
* spazio dei nomi [Aspose.Words](../../node)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->