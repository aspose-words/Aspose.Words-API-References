---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation metod"
linktitle: "get_Rotation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation metod. Hämtar eller anger rotationen för axelrubriken i grader i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words.drawing.charts/chartaxistitle/get_rotation/
---
## ChartAxisTitle::get_Rotation method


Hämtar eller anger rotationen för axelrubriken i grader.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation()
```


## Exempel



Visar hur man ställer in orientering och rotation för diagram- och axeltitlar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Innan du ställer in titelns egenskaper, se till att denna titel kommer att visas.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## Se även

* Class [ChartAxisTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
