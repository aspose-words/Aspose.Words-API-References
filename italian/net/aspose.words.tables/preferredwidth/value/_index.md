---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words per .NET
description: PreferredWidth Value proprietà. Ottiene il valore di larghezza preferito. Lunità di misura è specificata nelType proprietà in C#.
type: docs
weight: 50
url: /it/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Ottiene il valore di larghezza preferito. L'unità di misura è specificata nel[`Type`](../type/) proprietà.

```csharp
public double Value { get; }
```

## Esempi

Mostra come verificare il tipo di larghezza e il valore preferiti di una cella di tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Guarda anche

* class [PreferredWidth](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
