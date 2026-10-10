---
title: "Aspose::Words::Drawing::Fill::get_Pattern metod"
linktitle: "get_Pattern"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Fill::get_Pattern metod. Hämtar en PatternType för fyllningen i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Hämtar en [PatternType](../../patterntype/) för fyllningen.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


## Exempel



Visar hur man ställer in mönster för en form.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Det finns flera sätt att specificera fyllning till ett mönster.
// 1 -  Använd mönster på formens fyllning:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Använd mönster med förgrunds- och bakgrundsfärger på formens fyllning:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Se även

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
