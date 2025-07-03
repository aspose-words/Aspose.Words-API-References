---
title: Aspose::Words::Drawing::PatternType enum
linktitle: PatternType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::PatternType enum. Specifies the fill pattern to be used to fill a shape in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Specifies the fill pattern to be used to fill a shape.

```cpp
enum class PatternType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | -1 | No pattern. |
| Percent10 | 1 | 10% of the foreground color. |
| Percent20 | 2 | 20% of the foreground color. |
| Percent25 | 3 | 25% of the foreground color. |
| Percent30 | 4 | 30% of the foreground color. |
| Percent40 | 5 | 40% of the foreground color |
| Percent50 | 6 | 50% of the foreground color |
| Percent5 | 7 | 5% of the foreground color. |
| Percent60 | 8 | 60% of the foreground color. |
| Percent70 | 9 | 70% of the foreground color. |
| Percent75 | 10 | 75% of the foreground color. |
| Percent80 | 11 | 80% of the foreground color. |
| Percent90 | 12 | 90% of the foreground color. |
| Cross | 13 | Cross. |
| DarkDownwardDiagonal | 14 | Dark downward diagonal. |
| DarkHorizontal | 15 | Dark horizontal. |
| DarkUpwardDiagonal | 16 | Dark upward diagonal. |
| DarkVertical | 17 | Dark vertical. |
| DashedDownwardDiagonal | 18 | Dashed downward diagonal. |
| DashedHorizontal | 19 | Dashed horizontal. |
| DashedUpwardDiagonal | 20 | Dashed upward diagonal. |
| DashedVertical | 21 | Dashed vertical. |
| DiagonalBrick | 22 | Diagonal brick. |
| DiagonalCross | 23 | Diagonal cross. |
| Divot | 24 | Pattern divot. |
| DottedDiamond | 25 | Dotted diamond. |
| DottedGrid | 26 | Dotted grid. |
| DownwardDiagonal | 27 | Downward diagonal. |
| Horizontal | 28 | Horizontal. |
| HorizontalBrick | 29 | Horizontal brick. |
| LargeCheckerBoard | 30 | Large checker board. |
| LargeConfetti | 31 | Large confetti. |
| LargeGrid | 32 | Large grid. |
| LightDownwardDiagonal | 33 | Light downward diagonal. |
| LightHorizontal | 34 | Light horizontal. |
| LightUpwardDiagonal | 36 | Light upward diagonal. |
| LightVertical | 37 | Light vertical. |
| NarrowHorizontal | 38 | Narrow horizontal. |
| NarrowVertical | 39 | Narrow vertical. |
| OutlinedDiamond | 40 | Outlined diamond. |
| Plaid | 41 | Plaid. |
| Shingle | 42 | Shingle. |
| SmallCheckerBoard | 43 | Small checker board. |
| SmallConfetti | 44 | Small confetti. |
| SmallGrid | 45 | Small grid. |
| SolidDiamond | 46 | Solid diamond. |
| Sphere | 47 | Sphere. |
| Trellis | 48 | Trellis. |
| UpwardDiagonal | 49 | Upward diagonal. |
| Vertical | 50 | Vertical. |
| Wave | 51 | Wave. |
| Weave | 52 | Weave. |
| WideDownwardDiagonal | 53 | Wide downward diagonal. |
| WideUpwardDiagonal | 54 | Wide upward diagonal. |
| ZigZag | 55 | Zig zag. |


## Examples



Shows how to set pattern for a shape. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// There are several ways specified fill to a pattern.
// 1 -  Apply pattern to the shape fill:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Apply pattern with foreground and background colors to the shape fill:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
