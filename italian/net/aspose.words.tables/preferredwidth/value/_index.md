---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words per .NET
description: Scopri la proprietà Valore LarghezzaPreferita per accedere e personalizzare facilmente la larghezza desiderata. Migliora il tuo design con misure precise oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Ottiene il valore di larghezza preferito. L'unità di misura è specificata in[`Type`](../type/) proprietà.

```csharp
public double Value { get; }
```

## Esempi

Mostra come verificare il tipo di larghezza preferito e il valore di una cella di una tabella.

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
