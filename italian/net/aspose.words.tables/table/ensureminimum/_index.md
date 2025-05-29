---
title: Table.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words per .NET
description: Scopri il metodo Table EnsureMinimum, crea e aggiungi senza sforzo una riga quando la tua tabella è vuota per una gestione dei dati ottimale.
type: docs
weight: 420
url: /it/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Se la tabella non ha righe, ne crea e ne aggiunge una[`Row`](../../row/) .

```csharp
public void EnsureMinimum()
```

## Esempi

Mostra come garantire che un nodo di tabella contenga i nodi a cui dobbiamo aggiungere contenuto.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Le tabelle contengono righe, che contengono celle, che possono contenere paragrafi
// con elementi tipici quali sequenze, forme e persino altre tabelle.
// La nostra nuova tabella non ha nessuno di questi nodi e non possiamo aggiungervi contenuti finché non ne avrà uno.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// La chiamata al metodo "EnsureMinimum" su una tabella garantirà che
// la tabella ha almeno una riga e una cella con un paragrafo vuoto.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
