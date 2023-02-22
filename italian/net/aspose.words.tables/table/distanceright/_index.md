---
title: Table.DistanceRight
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene la distanza tra la tabella a destra e il testo circostante in punti.
type: docs
weight: 140
url: /it/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

Ottiene la distanza tra la tabella a destra e il testo circostante, in punti.

```csharp
public double DistanceRight { get; }
```

### Esempi

Mostra le operazioni di distanza minima tra i limiti della tabella e il testo.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


