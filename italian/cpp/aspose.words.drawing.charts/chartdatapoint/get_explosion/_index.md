---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion metodo"
linktitle: "get_Explosion"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion metodo. Specifica la quantità con cui il punto dati deve essere spostato dal centro della torta. Può essere negativo, negativo significa che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.drawing.charts/chartdatapoint/get_explosion/
---
## ChartDataPoint::get_Explosion method


Specifica la quantità di spostamento del punto dati dal centro della torta. Può essere negativo; un valore negativo indica che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion() override
```


## Esempi



Mostra come spostare le fette di un grafico a torta lontano dal centro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" di un grafico a torta può essere spostata lontano dal centro di una certa distanza tramite l'attributo Explosion del relativo punto dati.
// Aggiungi un punto dati alla prima porzione del grafico a torta e spostalo lontano dal centro di 10 punti.
// Aspose.Words crea punti dati automaticamente se non esistono.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Sposta la seconda porzione a una distanza maggiore.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## Vedi anche

* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
