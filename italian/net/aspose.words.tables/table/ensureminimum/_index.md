---
title: Table.EnsureMinimum
second_title: Aspose.Words per .NET API Reference
description: Table metodo. Se la tabella non ha righe ne crea e ne aggiunge una Riga .
type: docs
weight: 400
url: /it/net/aspose.words.tables/table/ensureminimum/
---
## Table.EnsureMinimum method

Se la tabella non ha righe, ne crea e ne aggiunge una **Riga** .

```csharp
public void EnsureMinimum()
```

### Esempi

Mostra come garantire che un nodo tabella contenga i nodi necessari per aggiungere contenuto.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Le tabelle contengono righe, che contengono celle, che possono contenere paragrafi
// con elementi tipici come piste, forme e persino altre tabelle.
// La nostra nuova tabella non ha nessuno di questi nodi e non possiamo aggiungervi contenuti finché non lo fa.
Assert.AreEqual(0, table.GetChildNodes(NodeType.Any, true).Count);

// Chiamare il metodo "EnsureMinimum" su una tabella lo garantirà
// la tabella ha almeno una riga e una cella con un paragrafo vuoto.
table.EnsureMinimum();
table.FirstRow.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


