---
title: Row.EnsureMinimum
second_title: Aspose.Words per .NET API Reference
description: Row metodo. Se ilRow non ha celle ne crea e ne aggiunge unaCell .
type: docs
weight: 150
url: /it/net/aspose.words.tables/row/ensureminimum/
---
## Row.EnsureMinimum method

Se il[`Row`](../) non ha celle, ne crea e ne aggiunge una[`Cell`](../../cell/) .

```csharp
public void EnsureMinimum()
```

### Esempi

Mostra come garantire che un nodo di riga contenga i nodi necessari per iniziare ad aggiungervi contenuto.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);
Row row = new Row(doc);
table.AppendChild(row);

// Le righe contengono celle, contenenti paragrafi con elementi tipici come sequenze, forme e persino altre tabelle.
// La nostra nuova riga non ha nessuno di questi nodi e non possiamo aggiungervi contenuti finché non lo farà.
Assert.AreEqual(0, row.GetChildNodes(NodeType.Any, true).Count);

// La chiamata al metodo "EnsureMinimum" su una tabella lo garantirà
// la tabella ha almeno una cella con un paragrafo vuoto.
row.EnsureMinimum();
row.FirstCell.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));
```

### Guarda anche

* class [Row](../)
* spazio dei nomi [Aspose.Words.Tables](../../row/)
* assemblea [Aspose.Words](../../../)


