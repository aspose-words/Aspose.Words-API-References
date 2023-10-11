---
title: CompositeNode.HasChildNodes
second_title: Aspose.Words per .NET API Reference
description: CompositeNode proprietà. RestituisceVERO se questo nodo ha nodi figli.
type: docs
weight: 30
url: /it/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Restituisce`VERO` se questo nodo ha nodi figli.

```csharp
public bool HasChildNodes { get; }
```

### Esempi

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tables" di un nodo Body:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzando il metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe della tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Guarda anche

* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../compositenode/)
* assemblea [Aspose.Words](../../../)


