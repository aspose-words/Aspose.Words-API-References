---
title: Aspose::Words::Drawing::Fill::get_Pattern method
linktitle: get_Pattern
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Fill::get_Pattern method. Gets a PatternType for the fill in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Gets a [PatternType](../../patterntype/) for the fill.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


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

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
