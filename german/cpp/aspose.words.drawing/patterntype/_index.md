---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::PatternType enum. Gibt das Füllmuster an, das zum Füllen einer Form in C++ verwendet wird."
type: docs
weight: 31000
url: /de/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Gibt das Füllmuster an, das zum Füllen einer Form verwendet wird.

```cpp
enum class PatternType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | -1 | Kein Muster. |
| Percent10 | 1 | 10 % der Vordergrundfarbe. |
| Percent20 | 2 | 20 % der Vordergrundfarbe. |
| Percent25 | 3 | 25 % der Vordergrundfarbe. |
| Percent30 | 4 | 30 % der Vordergrundfarbe. |
| Percent40 | 5 | 40 % der Vordergrundfarbe |
| Percent50 | 6 | 50 % der Vordergrundfarbe |
| Percent5 | 7 | 5 % der Vordergrundfarbe. |
| Percent60 | 8 | 60 % der Vordergrundfarbe. |
| Percent70 | 9 | 70 % der Vordergrundfarbe. |
| Percent75 | 10 | 75 % der Vordergrundfarbe. |
| Percent80 | 11 | 80 % der Vordergrundfarbe. |
| Percent90 | 12 | 90 % der Vordergrundfarbe. |
| Cross | 13 | Kreuz. |
| DarkDownwardDiagonal | 14 | Dunkel nach unten diagonal. |
| DarkHorizontal | 15 | Dunkel horizontal. |
| DarkUpwardDiagonal | 16 | Dunkel nach oben diagonal. |
| DarkVertical | 17 | Dunkel vertikal. |
| DashedDownwardDiagonal | 18 | Gestrichelt nach unten diagonal. |
| DashedHorizontal | 19 | Gestrichelt horizontal. |
| DashedUpwardDiagonal | 20 | Gestrichelt nach oben diagonal. |
| DashedVertical | 21 | Gestrichelt vertikal. |
| DiagonalBrick | 22 | Diagonale Ziegel. |
| DiagonalCross | 23 | Diagonales Kreuz. |
| Divot | 24 | Muster Vertiefung. |
| DottedDiamond | 25 | Gepunkteter Diamant. |
| DottedGrid | 26 | Gepunktetes Raster. |
| DownwardDiagonal | 27 | Abwärts diagonal. |
| Horizontal | 28 | Horizontal. |
| HorizontalBrick | 29 | Horizontaler Ziegel. |
| LargeCheckerBoard | 30 | Großes Schachbrett. |
| LargeConfetti | 31 | Großes Konfetti. |
| LargeGrid | 32 | Großes Raster. |
| LightDownwardDiagonal | 33 | Leicht abwärts diagonal. |
| LightHorizontal | 34 | Leicht horizontal. |
| LightUpwardDiagonal | 36 | Leicht aufwärts diagonal. |
| LightVertical | 37 | Leicht vertikal. |
| NarrowHorizontal | 38 | Schmal horizontal. |
| NarrowVertical | 39 | Schmal vertikal. |
| OutlinedDiamond | 40 | Umrandeter Diamant. |
| Karo | 41 | Karo. |
| Schindel | 42 | Schindel. |
| SmallCheckerBoard | 43 | Kleines Schachbrett. |
| SmallConfetti | 44 | Kleines Konfetti. |
| SmallGrid | 45 | Kleines Raster. |
| SolidDiamond | 46 | Solider Diamant. |
| Sphere | 47 | Kugel. |
| Trellis | 48 | Spalier. |
| UpwardDiagonal | 49 | Aufsteigende Diagonale. |
| Vertikal | 50 | Vertikal. |
| Welle | 51 | Welle. |
| Weave | 52 | Weben. |
| WideDownwardDiagonal | 53 | Breite absteigende Diagonale. |
| WideUpwardDiagonal | 54 | Breite aufsteigende Diagonale. |
| ZigZag | 55 | Zigzag. |


## Beispiele



Zeigt, wie man ein Muster für eine Form festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Es gibt mehrere Möglichkeiten, eine Füllung mit einem Muster anzugeben.
// 1 -  Muster auf die Formfüllung anwenden:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Muster mit Vorder- und Hintergrundfarben auf die Formfüllung anwenden:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
