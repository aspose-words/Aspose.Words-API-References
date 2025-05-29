---
title: CompositeNode.HasChildNodes
linktitle: HasChildNodes
articleTitle: HasChildNodes
second_title: Aspose.Words per .NET
description: Scopri se un CompositeNode ha nodi figlio con la proprietà HasChildNodes. Semplifica la tua programmazione con questa funzionalità essenziale per una gestione efficiente dei nodi.
type: docs
weight: 30
url: /it/net/aspose.words/compositenode/haschildnodes/
---
## CompositeNode.HasChildNodes property

Restituisce`VERO` se questo nodo ha nodi figlio.

```csharp
public bool HasChildNodes { get; }
```

## Esempi

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tabelle" di un nodo Corpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzo del metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe dalla tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Guarda anche

* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
