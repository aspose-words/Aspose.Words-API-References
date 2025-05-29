---
title: Node.GetAncestor
linktitle: GetAncestor
articleTitle: GetAncestor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Node GetAncestor-Methode, um einfach den ersten Vorfahren eines angegebenen Objekttyps abzurufen und so Ihre Codierungseffizienz und -genauigkeit zu verbessern.
type: docs
weight: 110
url: /de/net/aspose.words/node/getancestor/
---
## GetAncestor(*Type*) {#getancestor_1}

Ruft den ersten Vorgänger des angegebenen Objekttyps ab.

```csharp
public CompositeNode GetAncestor(Type ancestorType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | Type | Der abzurufende Objekttyp des Vorgängers. |

### Rückgabewert

Der Vorgänger des angegebenen Typs oder`null` wenn kein Vorgänger dieses Typs gefunden wurde.

## Bemerkungen

Der Vorgängertyp stimmt überein, wenn er gleich ist mit*ancestorType* oder abgeleitet von*ancestorType*.

## Beispiele

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Herausfinden, ob Zellen in der Tabelle andere Tabellen als untergeordnete Tabellen haben.
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
/// Bestimmt, ob eine Tabelle innerhalb ihrer Zellen eine unmittelbar untergeordnete Tabelle enthält.
/// Durchlaufen Sie diese Tabellen nicht rekursiv, um nach weiteren Tabellen zu suchen.
/// </summary>
/// <returns>
/// Gibt „true“ zurück, wenn mindestens eine untergeordnete Zelle eine Tabelle enthält.
/// Gibt „false“ zurück, wenn keine Zelle in der Tabelle eine Tabelle enthält.
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

### Siehe auch

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## GetAncestor(*[NodeType](../../nodetype/)*) {#getancestor}

Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../nodetype/) .

```csharp
public CompositeNode GetAncestor(NodeType ancestorType)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ancestorType | NodeType | Der Knotentyp des abzurufenden Vorgängers. |

### Rückgabewert

Der Vorgänger des angegebenen Typs oder`null` wenn kein Vorgänger dieses Typs gefunden wurde.

## Beispiele

Zeigt, wie man herausfindet, ob Tabellen verschachtelt sind.

```csharp
public void CalculateDepthOfNestedTables()
{
    Document doc = new Document(MyDir + "Nested tables.docx");
    NodeCollection tables = doc.GetChildNodes(NodeType.Table, true);
    for (int i = 0; i < tables.Count; i++)
    {
        Table table = (Table)tables[i];

        // Herausfinden, ob Zellen in der Tabelle andere Tabellen als untergeordnete Tabellen haben.
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
/// Bestimmt, ob eine Tabelle innerhalb ihrer Zellen eine unmittelbar untergeordnete Tabelle enthält.
/// Durchlaufen Sie diese Tabellen nicht rekursiv, um nach weiteren Tabellen zu suchen.
/// </summary>
/// <returns>
/// Gibt „true“ zurück, wenn mindestens eine untergeordnete Zelle eine Tabelle enthält.
/// Gibt „false“ zurück, wenn keine Zelle in der Tabelle eine Tabelle enthält.
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

### Siehe auch

* class [CompositeNode](../../compositenode/)
* enum [NodeType](../../nodetype/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
