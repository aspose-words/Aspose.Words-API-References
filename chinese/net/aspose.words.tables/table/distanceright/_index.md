---
title: Table.DistanceRight
second_title: Aspose.Words for .NET API 参考
description: Table 财产. 获取表格右侧和周围文本之间的距离以磅为单位
type: docs
weight: 140
url: /zh/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

获取表格右侧和周围文本之间的距离，以磅为单位。

```csharp
public double DistanceRight { get; }
```

### 例子

显示表格边界和文本之间的最小距离操作。

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);
```

### 也可以看看

* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../table/)
* 部件 [Aspose.Words](../../../)


