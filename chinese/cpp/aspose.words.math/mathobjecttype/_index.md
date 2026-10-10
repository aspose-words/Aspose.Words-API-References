---
title: "Aspose::Words::Math::MathObjectType 枚举"
linktitle: "MathObjectType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Math::MathObjectType 枚举. 指定在 C++ 中 Office Math 对象的类型."
type: docs
weight: 2000
url: /zh/cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


指定 Office [Math](../) 对象的类型.

```cpp
enum class MathObjectType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| OMath | 0 | 数学文本的实例. |
| OMathPara | 1 | [Math](../) 段落或显示数学区域，包含一个或多个处于显示模式的 [OMath](./) 元素. |
| Accent | 2 | Accent 函数，由基字符和组合变音符号组成. |
| Bar | 3 | Bar 函数，由基参数和上划线或下划线组成. |
| BorderBox | 4 | [Border](../../aspose.words/border/) Box 对象，由围绕数学文本实例（如公式或方程）的边框组成. |
| Box | 5 | Box 对象，用于对方程或其他数学文本实例的组件进行分组. |
| Delimiter | 6 | Delimiter 对象，由开闭定界符（如圆括号、花括号、方括号和竖线）以及其中包含的元素组成. |
| Degree | 7 | 数学根号中的 Degree. |
| Argument | 8 | Argument 对象。当它们作为其他 Office [Math](../) 实体的参数时，用于封装 Office [Math](../) 实体. |
| Array | 9 | Array 对象，由一个或多个方程、表达式或其他数学文本串组成，可相对于行内周围文本作为一个整体垂直对齐. |
| Fraction | 10 | Fraction 对象，由分子和分母通过分数线分隔组成. |
| Denominator | 11 | Fraction 对象的 Denominator. |
| Numerator | 12 | Fraction 对象的分子。 |
| 函数 | 13 | Function-Apply 对象，由函数名和被作用的参数元素组成。 |
| FunctionName | 14 | 函数的名称。例如，函数名称有 sin 和 cos。 |
| GroupCharacter | 15 | Group-Character 对象，由绘制在文本上方或下方的字符组成，通常用于视觉上对项目进行分组。 |
| Limit | 16 | [LowerLimit](./) 对象的下限和 [UpperLimit](./) 函数的上限。 |
| LowerLimit | 17 | Lower-Limit 对象，由基线上的文本和紧接其下的缩小文本组成。 |
| UpperLimit | 18 | Upper-Limit 对象，由基线上的文本和紧接其上的缩小文本组成。 |
| Matrix | 19 | Matrix 对象，由一个或多个元素排列成一个或多个行和一个或多个列组成。 |
| MatrixRow | 20 | Matrix 的单行。 |
| NAry | 21 | N-ary 对象，由 n-ary 对象、基数（或操作数）以及可选的上限和下限组成。 |
| Phantom | 22 | Phantom 对象。 |
| Radical | 23 | Radical 对象，由根号、基元素和可选的指数组成。 |
| SubscriptPart | 24 | 对象的下标，可包含下标部分。 |
| SuperscriptPart | 25 | 上标对象的上标。 |
| PreSubSuperscript | 26 | Pre-Sub-Superscript 对象，由一个基元素以及放置在基元素左侧的下标和上标组成。 |
| 下标 | 27 | 下标对象，由一个基元素以及放置在右下方的缩小脚本组成。 |
| 下上标 | 28 | 下上标对象，由一个基元素、放置在右下方的缩小脚本以及放置在右上方的缩小脚本组成。 |
| 上标 | 29 | 上标对象，由一个基元素以及放置在右上方的缩小脚本组成。 |
| None | 30 | 未指定对象类型。 |

## 另见

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
