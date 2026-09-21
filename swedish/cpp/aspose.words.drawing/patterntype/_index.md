---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::PatternType enum. Anger fyllningsmönstret som ska användas för att fylla en form i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Anger fyllningsmönstret som ska användas för att fylla en form.

```cpp
enum class PatternType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | -1 | Inget mönster. |
| Percent10 | 1 | 10 % av förgrundsfärgen. |
| Percent20 | 2 | 20% av förgrundsfärgen. |
| Procent25 | 3 | 25% av förgrundsfärgen. |
| Procent30 | 4 | 30% av förgrundsfärgen. |
| Procent40 | 5 | 40% av förgrundsfärgen |
| Procent50 | 6 | 50% av förgrundsfärgen |
| Procent5 | 7 | 5% av förgrundsfärgen. |
| Procent60 | 8 | 60% av förgrundsfärgen. |
| Procent70 | 9 | 70% av förgrundsfärgen. |
| Procent75 | 10 | 75% av förgrundsfärgen. |
| Procent80 | 11 | 80% av förgrundsfärgen. |
| Procent90 | 12 | 90% av förgrundsfärgen. |
| Kors | 13 | Kors. |
| MörkNedåtriktadDiagonal | 14 | Mörk nedåtriktad diagonal. |
| MörkHorisontell | 15 | Mörk horisontell. |
| MörkUppåDiagonal | 16 | Mörk uppåtlutande diagonal. |
| MörkVertikal | 17 | Mörk vertikal. |
| StreckadNedåtlutandeDiagonal | 18 | Streckad nedåtlutande diagonal. |
| StreckadHorisontell | 19 | Streckad horisontell. |
| StreckadUppåtlutandeDiagonal | 20 | Streckad uppåtlutande diagonal. |
| StreckadVertikal | 21 | Streckad vertikal. |
| DiagonalTegel | 22 | Diagonal tegel. |
| DiagonalKors | 23 | Diagonal kors. |
| Grop | 24 | Mönster grop. |
| PrickadDiamant | 25 | Prickad diamant. |
| PrickatRutnät | 26 | Prickat rutnät. |
| NedåtlutandeDiagonal | 27 | Nedåtlutande diagonal. |
| Horisontell | 28 | Horisontell. |
| HorizontalBrick | 29 | Horisontell tegel. |
| LargeCheckerBoard | 30 | Stort schackbräde. |
| LargeConfetti | 31 | Stort konfetti. |
| LargeGrid | 32 | Stort rutnät. |
| LightDownwardDiagonal | 33 | Ljus nedåtlutande diagonal. |
| LightHorizontal | 34 | Ljus horisontell. |
| LightUpwardDiagonal | 36 | Ljus uppåtlutande diagonal. |
| LightVertical | 37 | Ljus vertikal. |
| NarrowHorizontal | 38 | Smal horisontell. |
| NarrowVertical | 39 | Smal vertikal. |
| OutlinedDiamond | 40 | Konturerad diamant. |
| Rutig | 41 | Rutig. |
| Takpanna | 42 | Takpanna. |
| LitenSchackbräda | 43 | Litet schackbräde. |
| LitenKonfetti | 44 | Liten konfetti. |
| LitenRutnät | 45 | Liten rutnät. |
| SolidDiamant | 46 | Solid diamant. |
| Sfär | 47 | Sfär. |
| Galler | 48 | Galler. |
| UppåtlutandeDiagonal | 49 | Uppåtlutande diagonal. |
| Vertikal | 50 | Vertikal. |
| Våg | 51 | Våg. |
| Väv | 52 | Väv. |
| BredNedåtlutandeDiagonal | 53 | Bred nedåtlutande diagonal. |
| BredUppåtlutandeDiagonal | 54 | Bred uppåtlutande diagonal. |
| Sicksack | 55 | Zick-zack. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
