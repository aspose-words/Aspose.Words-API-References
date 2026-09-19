---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation metodo"
linktitle: "get_Rotation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation metodo. Ottiene o imposta la rotazione del titolo del grafico in gradi in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.drawing.charts/charttitle/get_rotation/
---
## ChartTitle::get_Rotation method


Restituisce o imposta la rotazione del titolo del grafico in gradi.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation()
```


## Esempi



Mostra come impostare l'orientamento e la rotazione dei titoli del grafico e degli assi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Prima di impostare le proprietà del titolo, assicurati che questo titolo venga visualizzato.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## Vedi anche

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
