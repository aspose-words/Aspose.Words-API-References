---
title: Node.GetAncestor
second_title: Aspose.Words für .NET-API-Referenz
description: Node methode. Ruft den ersten Vorfahren des angegebenen Objekttyps ab.
type: docs
weight: 110
url: /de/net/aspose.words/node/getancestor/
---
## GetAncestor(Type) {#getancestor_1}

Ruft den ersten Vorfahren des angegebenen Objekttyps ab.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | Type | Der Objekttyp des abzurufenden Vorgängers. |

### Rückgabewert

Der Vorfahre des angegebenen Typs oder`Null` wenn kein Vorfahre dieses Typs gefunden wurde.

### Bemerkungen

Der Vorfahrentyp stimmt überein, wenn er gleich ist*ancestorType* oder abgeleitet von*ancestorType*.

### Beispiele

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Finden Sie heraus, ob Zellen in der Tabelle andere Tabellen als Kinder haben.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Finden Sie heraus, ob die Tabelle in einer anderen Tabelle verschachtelt ist und wenn ja, in welcher Tiefe.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Berechnet, auf welcher Ebene eine Tabelle in anderen Tabellen verschachtelt ist.
/// </summary>
/// <returns>
/// Eine Ganzzahl, die die Verschachtelungstiefe der Tabelle angibt (Anzahl der übergeordneten Tabellenknoten).
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
/// Bestimmt, ob eine Tabelle in ihren Zellen eine unmittelbar untergeordnete Tabelle enthält.
/// Diese Tabellen nicht rekursiv durchlaufen, um nach weiteren Tabellen zu suchen.
/// </summary>
/// <returns>
/// Gibt true zurück, wenn mindestens eine untergeordnete Zelle eine Tabelle enthält.
/// Gibt false zurück, wenn keine Zellen in der Tabelle eine Tabelle enthalten.
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

### Siehe auch

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namensraum [Aspose.Words](../../node/)
* Montage [Aspose.Words](../../../)

---

## GetAncestor(NodeType) {#getancestor}

Ruft den ersten Vorfahren des angegebenen ab[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | NodeType | Der Knotentyp des abzurufenden Vorfahren. |

### Rückgabewert

Der Vorfahre des angegebenen Typs oder`Null` wenn kein Vorfahre dieses Typs gefunden wurde.

### Beispiele

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Finden Sie heraus, ob Zellen in der Tabelle andere Tabellen als Kinder haben.
        int count = GetChildTableCount(table);
        Console.WriteLine("Table #{0} has {1} tables directly within its cells", i, count);

        // Finden Sie heraus, ob die Tabelle in einer anderen Tabelle verschachtelt ist und wenn ja, in welcher Tiefe.
        int tableDepth = GetNestedDepthOfTable(table);

        if (tableDepth > 0)
            Console.WriteLine("Table #{0} is nested inside another table at depth of {1}", i,
                tableDepth);
        else
            Console.WriteLine("Table #{0} is a non nested table (is not a child of another table)", i);
    }
}

/// <summary>
/// Berechnet, auf welcher Ebene eine Tabelle in anderen Tabellen verschachtelt ist.
/// </summary>
/// <returns>
/// Eine Ganzzahl, die die Verschachtelungstiefe der Tabelle angibt (Anzahl der übergeordneten Tabellenknoten).
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
/// Bestimmt, ob eine Tabelle in ihren Zellen eine unmittelbar untergeordnete Tabelle enthält.
/// Diese Tabellen nicht rekursiv durchlaufen, um nach weiteren Tabellen zu suchen.
/// </summary>
/// <returns>
/// Gibt true zurück, wenn mindestens eine untergeordnete Zelle eine Tabelle enthält.
/// Gibt false zurück, wenn keine Zellen in der Tabelle eine Tabelle enthalten.
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

### Siehe auch

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* namensraum [Aspose.Words](../../node/)
* Montage [Aspose.Words](../../../)


