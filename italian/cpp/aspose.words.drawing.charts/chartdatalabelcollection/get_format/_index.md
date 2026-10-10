---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Format method"
linktitle: "get_Format"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Format method. Fornisce l'accesso alla formattazione di riempimento e linea delle etichette dei dati in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_format/
---
## ChartDataLabelCollection::get_Format method


Fornisce l'accesso alla formattazione di riempimento e linea delle etichette dati.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Format()
```


## Esempi



Mostra come impostare il riempimento, il tratto e la formattazione delle callout per le etichette dei dati del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Elimina la serie generata di default.
chart->get_Series()->Clear();

// Aggiungi nuova serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2", u"AW Category 3", u"AW Category 4"}), System::MakeArray<double>({100, 200, 300, 400}));

// Mostra le etichette dati.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowValue(true);

// Formatta le etichette dei dati come callout.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> format = series->get_DataLabels()->get_Format();
format->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::WedgeRectCallout);
format->get_Stroke()->set_Color(System::Drawing::Color::get_DarkGreen());
format->get_Fill()->Solid(System::Drawing::Color::get_Green());
series->get_DataLabels()->get_Font()->set_Color(System::Drawing::Color::get_Yellow());

// Modifica il riempimento e il tratto di un'etichetta dati individuale.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartFormat> labelFormat = series->get_DataLabels()->idx_get(0)->get_Format();
labelFormat->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());
labelFormat->get_Fill()->Solid(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.FormatDataLables.docx");
```

## Vedi anche

* Class [ChartFormat](../../chartformat/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
