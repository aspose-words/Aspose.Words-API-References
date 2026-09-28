---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation метод"
linktitle: "get_Rotation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation метод. Получает или задает вращение подписей данных всей серии в градусах в C++."
type: docs
weight: 5667
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_rotation/
---
## ChartDataLabelCollection::get_Rotation method


Получает или задает вращение подписей данных всей серии в градусах.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation()
```

## Примечания


Диапазон допустимых значений от -180 до 180 включительно. Значение по умолчанию — 0.

Если значение [Orientation](../get_orientation/) равно [Horizontal](../../../aspose.words.drawing/shapetextorientation/), формы подписей, если они существуют, вращаются вместе с текстом подписи. В противном случае вращается только текст подписи.

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

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
