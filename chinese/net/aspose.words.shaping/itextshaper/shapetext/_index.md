---
title: ITextShaper.ShapeText
second_title: Aspose.Words for .NET API 参考
description: ITextShaper 方法. 返回Cluster从一系列文本片段生成的对象 返回数组的长度等于runs. 如果在索引处运行具有相应的簇则同一索引处的结果将记录它们
type: docs
weight: 10
url: /zh/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

返回[`Cluster`](../../cluster/)从一系列文本片段生成的对象。 返回数组的长度等于*runs*. 如果在索引处运行具有相应的簇，则同一索引处的结果将记录它们。

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| runs | String[] | 一系列文本片段 |
| direction | Direction | 文字方向 |
| script | UnicodeScript | 一个脚本 |
| fontFeatures | FontFeature[] | 需要考虑的一组功能 |

### 也可以看看

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* 命名空间 [Aspose.Words.Shaping](../../itextshaper/)
* 部件 [Aspose.Words](../../../)


