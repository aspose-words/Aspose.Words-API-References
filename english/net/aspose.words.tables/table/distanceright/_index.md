---
title: Table.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: Aspose.Words for .NET
description: Adjust the Table DistanceRight property to control spacing between your table and surrounding text in points, enhancing layout and readability.
type: docs
weight: 140
url: /net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

Gets or sets distance between table right and the surrounding text, in points.

```csharp
public double DistanceRight { get; set; }
```

## Examples

Shows how to set distance between table boundaries and text.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.That(table.DistanceTop, Is.EqualTo(25.9d));
Assert.That(table.DistanceBottom, Is.EqualTo(25.9d));
Assert.That(table.DistanceLeft, Is.EqualTo(17.3d));
Assert.That(table.DistanceRight, Is.EqualTo(17.3d));

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
