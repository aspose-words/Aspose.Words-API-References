---
title: "Aspose::Words::Drawing::ShapeLineStyle enum"
linktitle: "ShapeLineStyle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeLineStyle enum. Указывает составной стиль линии фигуры в C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enum


Указывает составной стиль линии для [Фигуры](../shape/).

```cpp
enum class ShapeLineStyle
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Single | 0 | Одна линия. |
| Double | 1 | Две линии одинаковой ширины. |
| ThickThin | 2 | Две линии, одна толстая, другая тонкая. |
| ThinThick | 3 | Две линии, одна тонкая, другая толстая. |
| Triple | 4 | Три линии: тонкая, толстая, тонкая. |
| Default | n/a | Значение по умолчанию — [Single](./). |


## Примеры



Показывает, как изменить свойства обводки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Базовые фигуры, такие как прямоугольник, имеют две видимые части.
// 1 —  Заливка, которая применяется к области внутри контура фигуры:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 —  Обводка, которая отмечает контур фигуры:
// Измените различные свойства обводки этой фигуры.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
