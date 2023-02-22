---
title: Table.DistanceBottom
second_title: Aspose.Words für .NET-API-Referenz
description: Table eigendom. Ermittelt den Abstand zwischen Tabellenunterkante und umgebendem Text in Punkten.
type: docs
weight: 120
url: /de/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Ermittelt den Abstand zwischen Tabellenunterkante und umgebendem Text in Punkten.

```csharp
public double DistanceBottom { get; }
```

### Beispiele

Zeigt die Mindestabstandsoperationen zwischen Tabellengrenzen und Text an.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);
```

### Siehe auch

* class [Table](../)
* namensraum [Aspose.Words.Tables](../../table/)
* Montage [Aspose.Words](../../../)


