---
title: Patterned
second_title: Aspose.Words for C++ API Reference
description: Sets the specified fill to a pattern.
type: docs
weight: 326
url: /cpp/aspose.words.drawing/fill/patterned/
---
## Fill::Patterned(Aspose::Words::Drawing::PatternType) method


Sets the specified fill to a pattern.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |

## Examples



Shows how to set pattern for a shape. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Shape stroke pattern border.docx");

auto shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
SharedPtr<Fill> fill = shape->get_Fill();

std::cout << String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// There are several ways specified fill to a pattern.
// 1 -  Apply pattern to the shape fill:
fill->Patterned(PatternType::DiagonalBrick);

// 2 -  Apply pattern with foreground and background colors to the shape fill:
fill->Patterned(PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(ArtifactsDir + u"Shape.FillPattern.docx");
```

## See Also

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
## Fill::Patterned(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) method


Sets the specified fill to a pattern.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType, System::Drawing::Color foreColor, System::Drawing::Color backColor)
```


| Parameter | Type | Description |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |
| foreColor | System::Drawing::Color | The color of the foreground fill. |
| backColor | System::Drawing::Color | The color of the background fill. |

## Examples



Shows how to set pattern for a shape. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Shape stroke pattern border.docx");

auto shape = System::DynamicCast<Shape>(doc->GetChild(NodeType::Shape, 0, true));
SharedPtr<Fill> fill = shape->get_Fill();

std::cout << String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// There are several ways specified fill to a pattern.
// 1 -  Apply pattern to the shape fill:
fill->Patterned(PatternType::DiagonalBrick);

// 2 -  Apply pattern with foreground and background colors to the shape fill:
fill->Patterned(PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(ArtifactsDir + u"Shape.FillPattern.docx");
```

## See Also

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words](../../../)
