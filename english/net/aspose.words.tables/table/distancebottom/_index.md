---
title: Table.DistanceBottom
linktitle: DistanceBottom
second_title: Aspose.Words for .NET API Reference
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

Shows the minimum distance operations between table boundaries and text.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);
```

### See Also

* class [Table](../)
* namespace [Aspose.Words.Tables](../../table/)
* assembly [Aspose.Words](../../../)
