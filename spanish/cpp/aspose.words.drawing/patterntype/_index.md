---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::PatternType enum. Especifica el patrón de relleno que se usará para rellenar una forma en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Especifica el patrón de relleno que se usará para rellenar una forma.

```cpp
enum class PatternType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | -1 | Sin patrón. |
| Percent10 | 1 | 10% del color de primer plano. |
| Percent20 | 2 | 20% del color de primer plano. |
| Percent25 | 3 | 25% del color de primer plano. |
| Percent30 | 4 | 30% del color de primer plano. |
| Percent40 | 5 | 40% del color de primer plano |
| Percent50 | 6 | 50% del color de primer plano |
| Percent5 | 7 | 5% del color de primer plano. |
| Percent60 | 8 | 60% del color de primer plano. |
| Percent70 | 9 | 70% del color de primer plano. |
| Percent75 | 10 | 75% del color de primer plano. |
| Percent80 | 11 | 80% del color de primer plano. |
| Percent90 | 12 | 90% del color de primer plano. |
| Cross | 13 | Cruz. |
| DarkDownwardDiagonal | 14 | Diagonal descendente oscura. |
| DarkHorizontal | 15 | Horizontal oscuro. |
| DarkUpwardDiagonal | 16 | Diagonal ascendente oscura. |
| DarkVertical | 17 | Vertical oscuro. |
| DashedDownwardDiagonal | 18 | Diagonal descendente punteada. |
| DashedHorizontal | 19 | Horizontal punteada. |
| DashedUpwardDiagonal | 20 | Diagonal ascendente punteada. |
| DashedVertical | 21 | Vertical punteada. |
| DiagonalBrick | 22 | Ladrillo diagonal. |
| DiagonalCross | 23 | Cruz diagonal. |
| Divot | 24 | Divot de patrón. |
| DottedDiamond | 25 | Diamante punteado. |
| DottedGrid | 26 | Cuadrícula punteada. |
| DownwardDiagonal | 27 | Diagonal descendente. |
| Horizontal | 28 | Horizontal. |
| HorizontalBrick | 29 | Ladrillo horizontal. |
| LargeCheckerBoard | 30 | Tablero de damas grande. |
| LargeConfetti | 31 | Confeti grande. |
| LargeGrid | 32 | Cuadrícula grande. |
| LightDownwardDiagonal | 33 | Diagonal descendente ligera. |
| LightHorizontal | 34 | Horizontal ligera. |
| LightUpwardDiagonal | 36 | Diagonal ascendente ligera. |
| LightVertical | 37 | Vertical ligera. |
| NarrowHorizontal | 38 | Horizontal estrecha. |
| NarrowVertical | 39 | Vertical estrecha. |
| OutlinedDiamond | 40 | Diamante contorneado. |
| Plaid | 41 | A cuadros. |
| Shingle | 42 | Teja. |
| SmallCheckerBoard | 43 | Tablero de ajedrez pequeño. |
| SmallConfetti | 44 | Confeti pequeño. |
| SmallGrid | 45 | Cuadrícula pequeña. |
| SolidDiamond | 46 | Diamante sólido. |
| Sphere | 47 | Esfera. |
| Trellis | 48 | Enrejado. |
| UpwardDiagonal | 49 | Diagonal ascendente. |
| Vertical | 50 | Vertical. |
| Wave | 51 | Onda. |
| Weave | 52 | Tejido. |
| WideDownwardDiagonal | 53 | Diagonal descendente ancha. |
| WideUpwardDiagonal | 54 | Diagonal amplia ascendente. |
| ZigZag | 55 | Zig zag. |


## Ejemplos



Muestra cómo establecer un patrón para una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Hay varias formas de especificar el relleno con un patrón.
// 1 -  Aplicar patrón al relleno de la forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Aplicar patrón con colores de primer plano y de fondo al relleno de la forma:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
