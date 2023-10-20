---
title: Cell.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words per .NET
description: Cell EnsureMinimum metodo. Se lultimo figlio non è un paragrafo crea e aggiunge un paragrafo vuoto in C#.
type: docs
weight: 140
url: /it/net/aspose.words.tables/cell/ensureminimum/
---
## Cell.EnsureMinimum method

Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto.

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

// Le celle possono contenere paragrafi con elementi tipici come sequenze, forme e persino altre tabelle.
// La nostra nuova cella non ha paragrafi e non possiamo aggiungere contenuti come nodi di esecuzione e forma finché non lo fa.
Assert.AreEqual(0, cell.GetChildNodes(NodeType.Any, true).Count);

// La chiamata al metodo "EnsureMinimum" su una cella lo garantirà
// la cella ha almeno un paragrafo vuoto, al quale possiamo poi aggiungere contenuti.
cell.EnsureMinimum();
cell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
