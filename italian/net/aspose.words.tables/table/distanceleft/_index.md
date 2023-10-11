---
title: Table.DistanceLeft
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Ottiene o imposta la distanza tra la tabella a sinistra e il testo circostante in punti.
type: docs
weight: 130
url: /it/net/aspose.words.tables/table/distanceleft/
---
## Table.DistanceLeft property

Ottiene o imposta la distanza tra la tabella a sinistra e il testo circostante, in punti.

```csharp
public double DistanceLeft { get; set; }
```

### Esempi

Mostra come impostare la distanza tra i bordi della tabella e il testo.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

 // Imposta la distanza tra la tabella e il testo circostante.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


