---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation metodo"
linktitle: "get_Orientation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation metodo. Ottiene o imposta l'orientamento del testo del titolo del grafico in C++."
type: docs
weight: 1875
url: /it/cpp/aspose.words.drawing.charts/charttitle/get_orientation/
---
## ChartTitle::get_Orientation method


Restituisce o imposta l'orientamento del testo del titolo del grafico.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation()
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

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
