---
title: Table.DistanceRight
linktitle: DistanceRight
articleTitle: DistanceRight
second_title: 用于 .NET 的 Aspose.Words
description: Table DistanceRight 财产. 获取或设置表格右侧与周围文本之间的距离以磅为单位 在 C#.
type: docs
weight: 140
url: /zh/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

获取或设置表格右侧与周围文本之间的距离（以磅为单位）。

```csharp
public double DistanceRight { get; set; }
```

## 例子

演示如何设置表格边界和文本之间的距离。

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

 // 设置表格和周围文本之间的距离。
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
