---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format metodo"
linktitle: "get_Format"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Format metodo. Fornisce l'accesso alla formattazione di riempimento e linea della serie in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.drawing.charts/chartseries/get_format/
---
## ChartSeries::get_Format method


Fornisce l'accesso alla formattazione di riempimento e linea della serie.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartSeries::get_Format()
```


## Esempi



Mostra come impostare il colore della serie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Elimina la serie generata di default.
seriesColl->Clear();

// Crea un array di nomi di categoria.
auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});

// Aggiunta di nuove serie. Gli array di valori e di categorie devono avere la stessa dimensione.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = seriesColl->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = seriesColl->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = seriesColl->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));

// Imposta il colore della serie.
series1->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Red());
series2->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Yellow());
series3->get_Format()->get_Fill()->set_ForeColor(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.SeriesColor.docx");
```

## Vedi anche

* Class [ChartFormat](../../chartformat/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
