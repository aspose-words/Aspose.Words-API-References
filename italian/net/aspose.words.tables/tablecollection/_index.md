---
title: TableCollection Class
linktitle: TableCollection
articleTitle: TableCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Tables.TableCollection per un accesso semplice e tipizzato ai nodi Tabella, migliorando l'efficienza e la flessibilità nell'elaborazione dei documenti.
type: docs
weight: 7210
url: /it/net/aspose.words.tables/tablecollection/
---
## TableCollection class

Fornisce accesso tipizzato a una raccolta di[`Table`](../table/) nodi.

Per saperne di più, visita il[Lavorare con le tabelle](https://docs.aspose.com/words/net/working-with-tables/) articolo di documentazione.

```csharp
public class TableCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words.tables/tablecollection/item/) { get; } | Recupera un[`Table`](../table/) all'indice dato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Inserisce un nodo nella raccolta all'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words.tables/tablecollection/toarray/#toarray_1)() | Copia tutte le tabelle dalla raccolta in un nuovo array di tabelle. (2 methods) |

## Esempi

Mostra come rimuovere la prima e l'ultima riga di tutte le tabelle in un documento.

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

* class [NodeCollection](../../aspose.words/nodecollection/)
* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
