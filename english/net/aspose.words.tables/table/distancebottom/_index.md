---
title: Table.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words for .NET
description: Table DistanceBottom property. Gets or sets distance between table bottom and the surrounding text in points in C#.
type: docs
weight: 120
url: /net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

Gets or sets distance between table bottom and the surrounding text, in points.

```csharp
public double DistanceBottom { get; set; }
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
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
