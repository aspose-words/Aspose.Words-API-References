---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation метод"
linktitle: "get_Orientation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation метод. Получает или задает ориентацию текста заголовка оси в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words.drawing.charts/chartaxistitle/get_orientation/
---
## ChartAxisTitle::get_Orientation method


Получает или задает ориентацию текста заголовка оси.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation()
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

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
