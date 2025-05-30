---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words per .NET
description: Ottimizza la struttura delle tue celle con il metodo EnsureMinimum aggiungi senza sforzo un paragrafo se l'ultimo figlio non lo è. Migliora la chiarezza del tuo documento!
type: docs
weight: 160
url: /it/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Se l'ultimo elemento figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto.

```csharp
public void EnsureMinimum()
```

## Esempi

Mostra come garantire che un nodo cella contenga i nodi necessari per iniziare ad aggiungervi contenuto.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);
Cell cell = new Cell(doc);
row.AppendChild(cell);

// Le celle possono contenere paragrafi con elementi tipici quali sequenze, forme e persino altre tabelle.
// La nostra nuova cella non ha paragrafi e non possiamo aggiungervi contenuti come nodi run e shape finché non li avrà.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// La chiamata al metodo "EnsureMinimum" su una cella garantirà che
// la cella ha almeno un paragrafo vuoto, a cui possiamo quindi aggiungere contenuti.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
