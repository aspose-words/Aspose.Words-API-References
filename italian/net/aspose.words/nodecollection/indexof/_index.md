---
title: NodeCollection.IndexOf
second_title: Aspose.Words per .NET API Reference
description: NodeCollection metodo. Restituisce lindice in base zero del nodo specificato.
type: docs
weight: 70
url: /it/net/aspose.words/nodecollection/indexof/
---
## NodeCollection.IndexOf method

Restituisce l'indice in base zero del nodo specificato.

```csharp
public int IndexOf(Node node)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| node | Node | Il nodo da individuare. |

### Valore di ritorno

L'indice in base zero del nodo all'interno della raccolta, se trovato; altrimenti, -1.

### Osservazioni

Questo metodo esegue una ricerca lineare; pertanto, il tempo medio di esecuzione è proporzionale a[`Count`](../count/).

### Esempi

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
* spazio dei nomi [Aspose.Words](../../nodecollection/)
* assemblea [Aspose.Words](../../../)


