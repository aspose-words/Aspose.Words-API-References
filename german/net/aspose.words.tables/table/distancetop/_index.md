---
title: Table.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words für .NET
description: Passen Sie den Abstand zwischen Ihrer Tabellenoberfläche und dem umgebenden Text mühelos an. Optimieren Sie Ihr Layout mit DistanceTop für ein elegantes, professionelles Erscheinungsbild!
type: docs
weight: 150
url: /de/net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

Ruft den Abstand zwischen der Tabellenoberfläche und dem umgebenden Text in Punkten ab oder legt ihn fest.

```csharp
public double DistanceTop { get; set; }
```

## Beispiele

Zeigt, wie der Abstand zwischen Tabellengrenzen und Text festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

// Abstand zwischen Tabelle und umgebendem Text festlegen.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../../aspose.words.tables/)
* Montage [Aspose.Words](../../../)
