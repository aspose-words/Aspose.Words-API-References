---
title: Table.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words for .NET
description: Adjust the Table DistanceBottom property to control spacing between your table's bottom and surrounding text, enhancing layout and readability.
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
