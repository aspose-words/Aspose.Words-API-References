---
title: Table.DistanceRight
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Får avståndet mellan tabell höger och omgivande text i punkter.
type: docs
weight: 140
url: /sv/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

Får avståndet mellan tabell höger och omgivande text, i punkter.

```csharp
public double DistanceRight { get; }
```

### Exempel

Visar det minsta avståndet mellan tabellgränser och text.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);
```

### Se även

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


