---
title: "Aspose::Words::Drawing::PatternType enum"
linktitle: "PatternType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::PatternType enum. Указывает шаблон заливки, который будет использоваться для заполнения формы в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words.drawing/patterntype/
---
## PatternType enum


Указывает шаблон заливки, который будет использоваться для заполнения фигуры.

```cpp
enum class PatternType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | -1 | Нет шаблона. |
| Percent10 | 1 | 10% от цвета переднего плана. |
| Percent20 | 2 | 20% от цвета переднего плана. |
| Percent25 | 3 | 25% от цвета переднего плана. |
| Percent30 | 4 | 30% от цвета переднего плана. |
| Percent40 | 5 | 40% от цвета переднего плана |
| Percent50 | 6 | 50% от цвета переднего плана |
| Percent5 | 7 | 5% от цвета переднего плана. |
| Percent60 | 8 | 60% от цвета переднего плана. |
| Percent70 | 9 | 70% от цвета переднего плана. |
| Percent75 | 10 | 75% от цвета переднего плана. |
| Percent80 | 11 | 80% от цвета переднего плана. |
| Percent90 | 12 | 90% от цвета переднего плана. |
| Крест | 13 | Крест. |
| DarkDownwardDiagonal | 14 | Темная нисходящая диагональ. |
| DarkHorizontal | 15 | Темный горизонтальный. |
| DarkUpwardDiagonal | 16 | Темная восходящая диагональ. |
| DarkVertical | 17 | Темный вертикальный. |
| DashedDownwardDiagonal | 18 | Пунктирная нисходящая диагональ. |
| DashedHorizontal | 19 | Пунктирный горизонтальный. |
| DashedUpwardDiagonal | 20 | Пунктирная восходящая диагональ. |
| DashedVertical | 21 | Пунктирный вертикальный. |
| DiagonalBrick | 22 | Диагональная кирпичная. |
| DiagonalCross | 23 | Диагональный крест. |
| Divot | 24 | Узор ямка. |
| DottedDiamond | 25 | Точечный ромб. |
| ТочечнаяСетка | 26 | Точечная сетка. |
| НисходящаяДиагональ | 27 | Нисходящая диагональ. |
| Горизонтальная | 28 | Горизонтальная. |
| ГоризонтальнаяКирпич | 29 | Горизонтальная кирпичная. |
| БольшаяШахматнаяДоска | 30 | Большая шахматная доска. |
| БольшойКонфетти | 31 | Большой конфетти. |
| БольшаяСетка | 32 | Большая сетка. |
| СветлаяНисходящаяДиагональ | 33 | Светлая нисходящая диагональ. |
| СветлаяГоризонталь | 34 | Светлая горизонталь. |
| СветлаяВосходящаяДиагональ | 36 | Светлая восходящая диагональ. |
| СветлаяВертикаль | 37 | Светлая вертикаль. |
| УзкаяГоризонталь | 38 | Узкая горизонталь. |
| УзкаяВертикаль | 39 | Узкая вертикаль. |
| OutlinedDiamond | 40 | Контурный ромб. |
| Plaid | 41 | Клетка. |
| Shingle | 42 | Гонт. |
| SmallCheckerBoard | 43 | Маленькая шахматная доска. |
| SmallConfetti | 44 | Мелкие конфетти. |
| SmallGrid | 45 | Маленькая сетка. |
| SolidDiamond | 46 | Сплошной ромб. |
| Sphere | 47 | Сфера. |
| Trellis | 48 | Трельяж. |
| UpwardDiagonal | 49 | Восходящая диагональ. |
| Вертикальная | 50 | Vertical. |
| Волна | 51 | Волна. |
| Weave | 52 | Плетение. |
| WideDownwardDiagonal | 53 | Широкая нисходящая диагональ. |
| WideUpwardDiagonal | 54 | Широкая восходящая диагональ. |
| ZigZag | 55 | Зигзаг. |


## Примеры



Показывает, как установить узор для фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();

std::cout << System::String::Format(u"Pattern value is: {0}", fill->get_Pattern()) << std::endl;

// Существует несколько способов заполнения узором.
// 1 -  Применить узор к заливке фигуры:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick);

// 2 -  Применить узор с цветами переднего плана и фона к заливке фигуры:
fill->Patterned(Aspose::Words::Drawing::PatternType::DiagonalBrick, System::Drawing::Color::get_Aqua(), System::Drawing::Color::get_Bisque());

doc->Save(get_ArtifactsDir() + u"Shape.FillPattern.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
