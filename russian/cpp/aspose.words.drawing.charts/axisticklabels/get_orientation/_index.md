---
title: "Метод Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation"
linktitle: "get_Orientation"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation. Получает или задает ориентацию текста меток делений в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


Получает или задает ориентацию текста меток делений.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Примечания


Значение по умолчанию — [Horizontal](../../../aspose.words.drawing/shapetextorientation/).

Обратите внимание, что некоторые значения [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) не влияют на ориентацию текста меток делений на оси значений.

## Примеры



Показывает, как изменить ориентацию и вращение меток делений оси.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте столбчатую диаграмму.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Установите ориентацию и вращение меток делений оси.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## См. также

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
