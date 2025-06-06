---
title: Cell.Tables
linktitle: Tables
articleTitle: Tables
second_title: Aspose.Words per .NET
description: Scopri le tabelle delle celle. Accedi facilmente a una raccolta di tabelle direttamente dalla tua cella per un'organizzazione semplificata e una gestione avanzata dei dati.
type: docs
weight: 120
url: /it/net/aspose.words.tables/cell/tables/
---
## Cell.Tables property

Ottiene una raccolta di tabelle che sono figlie immediate della cella.

```csharp
public TableCollection Tables { get; }
```

## Esempi

Mostra come scoprire se le tabelle sono annidate.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Scopri se ci sono celle nella tabella che hanno altre tabelle come figlie.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Scopri se la tabella è annidata all'interno di un'altra tabella e, in tal caso, a quale profondità.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Calcola a quale livello una tabella è annidata all'interno di altre tabelle.
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
/// Determina se una tabella contiene una tabella figlia immediata all'interno delle sue celle.
/// Non attraversare ricorsivamente queste tabelle per controllare altre tabelle.
/// </summary>
/// <returns>
/// Restituisce true se almeno una cella figlia contiene una tabella.
/// Restituisce false se nessuna cella nella tabella contiene una tabella.
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

### Guarda anche

* class [TableCollection](../../tablecollection/)
* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
