---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words for .NET
description: 探索 iTextShaper 的 ShapeText 方法，它可以有效地从文本片段生成 Cluster 对象，确保精确的文本格式和对齐。
type: docs
weight: 10
url: /zh/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

返回[`Cluster`](../../cluster/)从文本片段序列生成的对象。 返回数组的长度等于*runs*. 如果在索引处运行有相应的集群，则在同一索引处的结果将会记录它们。

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| runs | String[] | 一系列文本片段 |
| direction | Direction | 文本的方向 |
| script | UnicodeScript | 脚本 |
| enabledFontFeatures | FontFeature[] | 需要考虑的一组明确启用的 OpenType 功能 |
| variations | VariationAxisCoordinate[] | 字体的变化轴值 |

### 也可以看看

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* 命名空间 [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* 部件 [Aspose.Words](../../../)
