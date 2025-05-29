---
title: Table.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words for .NET
description: 调整表格底部距离属性来控制表格底部和周围文本之间的间距，增强布局和可读性。
type: docs
weight: 120
url: /zh/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

获取或设置表格底部与周围文本之间的距离（以磅为单位）。

```csharp
public double DistanceBottom { get; set; }
```

## 例子

显示如何设置表格边界和文本之间的距离。

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
