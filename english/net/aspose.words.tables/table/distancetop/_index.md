---
title: Table.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words for .NET
description: Adjust the distance between your table top and surrounding text effortlessly. Enhance your layout for a polished, professional look with DistanceTop!
type: docs
weight: 150
url: /net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

Gets or sets distance between table top and the surrounding text, in points.

```csharp
public double DistanceTop { get; set; }
```

## Examples

Shows how to set distance between table boundaries and text.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

// Set distance between table and surrounding text.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../../aspose.words.tables/)
* assembly [Aspose.Words](../../../)
