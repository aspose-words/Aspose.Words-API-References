---
title: Table.DistanceBottom
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Får avståndet mellan tabellbotten och den omgivande texten i punkter.
type: docs
weight: 120
url: /sv/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Får avståndet mellan tabellbotten och den omgivande texten, i punkter.

```csharp
public double DistanceBottom { get; }
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


