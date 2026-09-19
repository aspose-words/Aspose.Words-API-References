---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_Format metodo"
linktitle: "get_Format"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_Format metodo. Fornisce l'accesso alla formattazione di riempimento e linea della legenda in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words.drawing.charts/chartlegend/get_format/
---
## ChartLegend::get_Format method


Fornisce l'accesso alla formattazione di riempimento e linea della legenda.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartLegend::get_Format()
```


## Esempi



Mostra come utilizzare la formattazione del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Elimina le serie generate per impostazione predefinita.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Formatta lo sfondo del grafico.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Nascondi le etichette dei tick dell'asse.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Formatta il titolo del grafico.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatta il titolo dell'asse.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatta la legenda.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Vedi anche

* Class [ChartFormat](../../chartformat/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
