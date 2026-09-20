---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::ShapeTextOrientation. Указывает ориентацию текста в фигурах в C++."
type: docs
weight: 37500
url: /ru/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Указывает ориентацию текста в фигурах.

```cpp
enum class ShapeTextOrientation
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Горизонтальная | 0 | Текст располагается горизонтально (lr-tb). |
| Вниз | 1 | Текст повернут на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl). |
| Вверх | 2 | Текст повернут на 90 градусов влево, чтобы отображаться снизу вверх (bt-lr). |
| VerticalFarEast | 3 | Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз (tb-rl-v). |
| VerticalRotatedFarEast | 4 | Символы Дальнего Востока отображаются вертикально, остальной текст вращается на 90 градусов вправо, чтобы отображаться сверху вниз вертикально, затем слева направо горизонтально (tb-lr-v). |
| WordArtVertical | 5 | Текст расположен вертикально, по одной букве сверху другой. |
| WordArtVerticalRightToLeft | 6 | Текст расположен вертикально, по одной букве сверху другой, затем горизонтально справа налево. |


## Примеры



Показывает, как изменить ориентацию и вращение меток данных.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Показать метки данных.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Определить форму метки данных.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Установить ориентацию и вращение метки данных для всей серии.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Изменить ориентацию и вращение первой метки данных.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
