---
title: "Aspose::Words::Drawing::PatternType 枚举"
linktitle: "PatternType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::PatternType 枚举。指定在 C++ 中用于填充形状的填充模式。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


指定用于填充形状的填充图案。

```cpp
enum class PatternType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | -1 | 无图案。 |
| Percent10 | 1 | 前景色的 10%。 |
| Percent20 | 2 | 前景色的 20%。 |
| Percent25 | 3 | 前景色的 25%。 |
| Percent30 | 4 | 前景色的 30%。 |
| Percent40 | 5 | 前景色的 40% |
| Percent50 | 6 | 前景色的 50% |
| Percent5 | 7 | 前景颜色的 5%。 |
| Percent60 | 8 | 前景颜色的 60%。 |
| Percent70 | 9 | 前景颜色的 70%。 |
| Percent75 | 10 | 前景颜色的 75%。 |
| Percent80 | 11 | 前景颜色的 80%。 |
| Percent90 | 12 | 前景颜色的 90%。 |
| Cross | 13 | 十字形。 |
| DarkDownwardDiagonal | 14 | 深向下对角线。 |
| DarkHorizontal | 15 | 深水平线。 |
| DarkUpwardDiagonal | 16 | 深向上对角线。 |
| DarkVertical | 17 | 深垂直线。 |
| DashedDownwardDiagonal | 18 | 虚线向下对角线。 |
| DashedHorizontal | 19 | 虚线水平。 |
| 虚线向上对角线 | 20 | 虚线向上对角线。 |
| 虚线垂直 | 21 | 虚线垂直。 |
| 对角砖 | 22 | 对角砖。 |
| 对角十字 | 23 | 对角十字。 |
| 凹痕 | 24 | 图案凹痕。 |
| 点状菱形 | 25 | 点状菱形。 |
| 点状网格 | 26 | 点状网格。 |
| 向下对角线 | 27 | 向下对角线。 |
| Horizontal | 28 | 水平。 |
| 水平砖 | 29 | 水平砖。 |
| 大棋盘 | 30 | 大棋盘。 |
| 大彩屑 | 31 | 大彩屑。 |
| 大网格 | 32 | 大型网格。 |
| LightDownwardDiagonal | 33 | 浅向下对角线。 |
| LightHorizontal | 34 | 浅水平。 |
| LightUpwardDiagonal | 36 | 浅向上对角线。 |
| LightVertical | 37 | 浅垂直。 |
| NarrowHorizontal | 38 | 窄水平。 |
| NarrowVertical | 39 | 窄垂直。 |
| OutlinedDiamond | 40 | 轮廓菱形。 |
| Plaid | 41 | 格子。 |
| Shingle | 42 | 瓦片。 |
| SmallCheckerBoard | 43 | 小棋盘。 |
| SmallConfetti | 44 | 小彩屑。 |
| SmallGrid | 45 | 小网格。 |
| 实心菱形 | 46 | 实心菱形。 |
| 球体 | 47 | 球体。 |
| 格子 | 48 | 格子。 |
| 向上对角线 | 49 | 向上对角线。 |
| Vertical | 50 | 垂直。 |
| Wave | 51 | 波形。 |
| 编织 | 52 | 编织。 |
| 宽向下对角线 | 53 | 宽向下对角线。 |
| 宽向上对角线 | 54 | 宽向上对角线。 |
| 锯齿形 | 55 | 锯齿形。 |


## 示例



展示如何为形状设置图案。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// 有几种方法可以将填充指定为图案。
// 1 -  将图案应用于形状填充：
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  将图案与前景色和背景色一起应用于形状填充：
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
