---
title: Table.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words per .NET
description: Table DistanceTop proprietà. Ottiene o imposta la distanza tra il piano del tavolo e il testo circostante in punti in C#.
type: docs
weight: 150
url: /it/net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

Ottiene o imposta la distanza tra il piano del tavolo e il testo circostante, in punti.

```csharp
public double DistanceTop { get; set; }
```

## Esempi

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
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
