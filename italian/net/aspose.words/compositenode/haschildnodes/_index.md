---
title: CompositeNode.HasChildNodes
second_title: Aspose.Words per .NET API Reference
description: CompositeNode proprietà. Restituisce true se questo nodo ha nodi figlio.
type: docs
weight: 40
url: /it/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Restituisce true se questo nodo ha nodi figlio.

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

// Aggiunge tutte le righe dalla tabella corrente alla successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuoto.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Guarda anche

* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../compositenode/)
* assemblea [Aspose.Words](../../../)


