---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation метод"
linktitle: "get_Rotation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation метод. Получает или задает вращение заголовка оси в градусах в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.drawing.charts/chartaxistitle/get_rotation/
---
## ChartAxisTitle::get_Rotation method


Получает или задает поворот заголовка оси в градусах.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation()
```


## Примеры



Показывает, как задать ориентацию и вращение заголовков диаграмм и осей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Перед установкой свойств заголовка убедитесь, что этот заголовок будет отображаться.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## См. также

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
