---
title: "Aspose::Words::Drawing::Fill::Patterned yöntemi"
linktitle: "Patterned"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Fill::Patterned yöntemi. Belirtilen doldurmayı C++'ta bir desene ayarlar."
type: docs
weight: 26000
url: /tr/cpp/aspose.words.drawing/fill/patterned/
---
## Fill::Patterned(Aspose::Words::Drawing::PatternType) method


Belirtilen dolguyu bir desene ayarlar.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |

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
## Fill::Patterned(Aspose::Words::Drawing::PatternType, System::Drawing::Color, System::Drawing::Color) method


Belirtilen dolguyu bir desene ayarlar.

```cpp
void Aspose::Words::Drawing::Fill::Patterned(Aspose::Words::Drawing::PatternType patternType, System::Drawing::Color foreColor, System::Drawing::Color backColor)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| patternType | Aspose::Words::Drawing::PatternType | [PatternType](../../patterntype/) |
| foreColor | System::Drawing::Color | Ön plan doldurmanın rengi. |
| backColor | System::Drawing::Color | Arka plan doldurmanın rengi. |

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
