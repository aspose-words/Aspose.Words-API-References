---
title: TableCollection Class
linktitle: TableCollection
articleTitle: TableCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Tables.TableCollection für einen einfachen, typisierten Zugriff auf Tabellenknoten und verbessern Sie so die Effizienz und Flexibilität der Dokumentverarbeitung.
type: docs
weight: 7210
url: /de/net/aspose.words.tables/tablecollection/
---
## TableCollection class

Bietet typisierten Zugriff auf eine Sammlung von[`Table`](../table/) Knoten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Tabellen](https://docs.aspose.com/words/net/working-with-tables/) Dokumentationsartikel.

```csharp
public class TableCollection : NodeCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ruft die Anzahl der Knoten in der Sammlung ab. |
| [Item](../../aspose.words.tables/tablecollection/item/) { get; } | Ruft eine[`Table`](../table/) am angegebenen Index. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Fügt am Ende der Sammlung einen Knoten hinzu. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Bestimmt, ob ein Knoten in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Bietet eine einfache Iteration im „foreach“-Stil über die Knotensammlung. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Fügt einen Knoten am angegebenen Index in die Sammlung ein. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../../aspose.words.tables/tablecollection/toarray/#toarray_1)() | Kopiert alle Tabellen aus der Sammlung in ein neues Tabellen-Array. (2 methods) |

## Beispiele

Zeigt, wie die erste und die letzte Zeile aller Tabellen in einem Dokument entfernt werden.

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)
