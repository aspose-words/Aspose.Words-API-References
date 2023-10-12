---
title: Table.DistanceBottom
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Ruft den Abstand zwischen der Tabellenunterseite und dem umgebenden Text in Punkten ab oder legt diesen fest.
type: docs
weight: 120
url: /de/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Ruft den Abstand zwischen der Tabellenunterseite und dem umgebenden Text in Punkten ab oder legt diesen fest.

```csharp
public double DistanceBottom { get; set; }
```

### Beispiele

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
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


