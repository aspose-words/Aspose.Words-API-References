---
title: Aspose::Words::Math::MathObjectType enum
linktitle: MathObjectType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Math::MathObjectType enum. Specifies type of an Office Math object in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.math/mathobjecttype/
---
## MathObjectType enum


Specifies type of an Office Math object.

```cpp
enum class MathObjectType : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Accent | 2 | Accent function, consisting of a base and a combining diacritical mark. |
| Argument | 8 | Argument object. Encloses Office Math entities when they are used as arguments to other Office Math entities. |
| Array | 9 | Array object, consisting of one or more equations, expressions, or other mathematical text runs that can be vertically justified as a unit with respect to surrounding text on the line. |
| Bar | 3 | Bar function, consisting of a base argument and an overbar or underbar. |
| BorderBox | 4 | Border Box object, consisting of a border drawn around an instance of mathematical text (such as a formula or equation) |
| Box | 5 | Box object, which is used to group components of an equation or other instance of mathematical text. |
| Degree | 7 | Degree in the mathematical radical. |
| Delimiter | 6 | Delimiter object, consisting of opening and closing delimiters (such as parentheses, braces, brackets, and vertical bars), and an element contained inside. |
| Denominator | 11 | Denominator of a fraction object. |
| Fraction | 10 | Fraction object, consisting of a numerator and denominator separated by a fraction bar. |
| Function | 13 | Function-Apply object, which consists of a function name and an argument element acted upon. |
| FunctionName | 14 | Name of the function. For example, function names are sin and cos. |
| GroupCharacter | 15 | Group-Character object, consisting of a character drawn above or below text, often with the purpose of visually grouping items |
| Limit | 16 | Lower limit of the [LowerLimit](./) object and the upper limit of the [UpperLimit](./) function. |
| LowerLimit | 17 | Lower-Limit object, consisting of text on the baseline and reduced-size text immediately below it. |
| Matrix | 19 | Matrix object, consisting of one or more elements laid out in one or more rows and one or more columns. |
| MatrixRow | 20 | Single row of the matrix. |
| NAry | 21 | N-ary object, consisting of an n-ary object, a base (or operand), and optional upper and lower limits. |
| None | 30 | Type of object is not specified. |
| Numerator | 12 | Numerator of the Fraction object. |
| OMath | 0 | Instance of mathematical text. |
| OMathPara | 1 | Math paragraph, or display math zone, that contains one or more [OMath](./) elements that are in display mode. |
| Phantom | 22 | Phantom object. |
| PreSubSuperscript | 26 | Pre-Sub-Superscript object, which consists of a base element and a subscript and superscript placed to the left of the base. |
| Radical | 23 | Radical object, consisting of a radical, a base element, and an optional degree . |
| SubSuperscript | 28 | Sub-superscript object, which consists of a base element, a reduced-size script placed below and to the right, and a reduced-size script placed above and to the right. |
| Subscript | 27 | Subscript object, which consists of a base element and a reduced-size script placed below and to the right. |
| SubscriptPart | 24 | Subscript of the object that can have subscript part. |
| Superscript | 29 | Superscript object, which consists of a base element and a reduced-size script placed above and to the right. |
| SuperscriptPart | 25 | Superscript of the superscript object. |
| UpperLimit | 18 | Upper-Limit object, consisting of text on the baseline and reduced-size text immediately above it. |

## See Also

* Namespace [Aspose::Words::Math](../)
* Library [Aspose.Words for C++](../../)
