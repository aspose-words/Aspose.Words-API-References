---
title: PatternType Enum
linktitle: PatternType
articleTitle: PatternType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.PatternType 枚举，使用可自定义的填充图案增强您的形状。轻松提升您的文档设计！
type: docs
weight: 1550
url: /zh/net/aspose.words.drawing/patterntype/
---
## PatternType enumeration

指定用于填充形状的填充图案。

```csharp
public enum PatternType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `-1` | 没有图案。 |
| Percent10 | `1` | 10% 的前景色。 |
| Percent20 | `2` | 20% 的前景色。 |
| Percent25 | `3` | 25% 的前景色。 |
| Percent30 | `4` | 30% 的前景色。 |
| Percent40 | `5` | 40% 的前景色 |
| Percent50 | `6` | 50% 的前景色 |
| Percent5 | `7` | 5% 的前景色。 |
| Percent60 | `8` | 60% 的前景色。 |
| Percent70 | `9` | 70% 的前景色。 |
| Percent75 | `10` | 75% 的前景色。 |
| Percent80 | `11` | 80% 的前景色。 |
| Percent90 | `12` | 90% 的前景色。 |
| Cross | `13` | 十字架. |
| DarkDownwardDiagonal | `14` | 深色向下对角线。 |
| DarkHorizontal | `15` | 深色水平。 |
| DarkUpwardDiagonal | `16` | 深色向上对角线。 |
| DarkVertical | `17` | 深色垂直。 |
| DashedDownwardDiagonal | `18` | 向下对角线虚线。 |
| DashedHorizontal | `19` | 水平虚线。 |
| DashedUpwardDiagonal | `20` | 向上对角线虚线。 |
| DashedVertical | `21` | 垂直虚线。 |
| DiagonalBrick | `22` | 对角砖。 |
| DiagonalCross | `23` | 对角线交叉。 |
| Divot | `24` | 图案草皮。 |
| DottedDiamond | `25` | 点状菱形。 |
| DottedGrid | `26` | 虚线网格。 |
| DownwardDiagonal | `27` | 向下对角线。 |
| Horizontal | `28` | 水平. |
| HorizontalBrick | `29` | 水平砖。 |
| LargeCheckerBoard | `30` | 大型棋盘。 |
| LargeConfetti | `31` | 大五彩纸屑。 |
| LargeGrid | `32` | 大网格。 |
| LightDownwardDiagonal | `33` | 光线向下对角线。 |
| LightHorizontal | `34` | 浅水平。 |
| LightUpwardDiagonal | `36` | 向上对角线照射。 |
| LightVertical | `37` | 轻度垂直。 |
| NarrowHorizontal | `38` | 水平方向狭窄。 |
| NarrowVertical | `39` | 窄垂直。 |
| OutlinedDiamond | `40` | 轮廓钻石。 |
| Plaid | `41` | 格子. |
| Shingle | `42` | 木瓦. |
| SmallCheckerBoard | `43` | 小棋盘。 |
| SmallConfetti | `44` | 小五彩纸屑。 |
| SmallGrid | `45` | 小格子。 |
| SolidDiamond | `46` | 实心钻石。 |
| Sphere | `47` | 球体. |
| Trellis | `48` | 格子. |
| UpwardDiagonal | `49` | 向上对角线。 |
| Vertical | `50` | 垂直. |
| Wave | `51` | 挥手。 |
| Weave | `52` | 编织. |
| WideDownwardDiagonal | `53` | 宽向下对角线。 |
| WideUpwardDiagonal | `54` | 宽向上对角线。 |
| ZigZag | `55` | 之字形。 |

## 例子

展示如何设置形状的图案。

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Fill fill = shape.Fill;

Console.WriteLine("Pattern value is: {0}", fill.Pattern);

// 有几种方法可以指定填充图案。
// 1 - 将图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick);

// 2 - 将前景色和背景色的图案应用于形状填充：
fill.Patterned(PatternType.DiagonalBrick, Color.Aqua, Color.Bisque);

doc.Save(ArtifactsDir + "Shape.FillPattern.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
