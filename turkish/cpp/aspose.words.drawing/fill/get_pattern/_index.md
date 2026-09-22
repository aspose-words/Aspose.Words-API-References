---
title: "Aspose::Words::Drawing::Fill::get_Pattern metodu"
linktitle: "get_Pattern"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::get_Pattern metodu. C++'ta dolgu için bir PatternType alır."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.drawing/fill/get_pattern/
---
## Fill::get_Pattern method


Dolgu için bir [PatternType](../../patterntype/) alır.

```cpp
Aspose::Words::Drawing::PatternType Aspose::Words::Drawing::Fill::get_Pattern()
```


## Örnekler



Bir şekil için deseni nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Desene doldurmayı belirtmenin birkaç yolu vardır.
// 1 -  Deseni şekil doldurmasına uygula:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Ön plan ve arka plan renkleriyle deseni şekil doldurmasına uygula:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Ayrıca Bakınız

* Enum [PatternType](../../patterntype/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
