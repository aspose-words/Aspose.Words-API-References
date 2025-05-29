---
title: NodeCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words per .NET
description: Scopri il metodo IndexOf di NodeCollection per trovare in modo efficiente l'indice a partire da zero di qualsiasi nodo specificato nelle tue raccolte.
type: docs
weight: 70
url: /it/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Restituisce l'indice basato su zero del nodo specificato.

```csharp
public int IndexOf(Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | Node | Il nodo da localizzare. |

### Valore di ritorno

Indice a partire da zero del nodo all'interno della raccolta, se trovato; in caso contrario, -1.

## Osservazioni

Questo metodo esegue una ricerca lineare; pertanto, il tempo medio di esecuzione è proporzionale a[`Count`](../count/).

## Esempi

Mostra come ottenere l'indice di un nodo in una raccolta.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
NodeCollection allTables = doc.GetChildNodes(NodeType.Table, true);

Assert.AreEqual(0, allTables.IndexOf(table));

Row row = table.Rows[2];

Assert.AreEqual(2, table.IndexOf(row));

Cell cell = row.LastCell;

Assert.AreEqual(4, row.IndexOf(cell));
```

### Guarda anche

* class [Node](../../node/)
* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
