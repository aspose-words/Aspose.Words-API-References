---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion metod"
linktitle: "get_Explosion"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion metod. Anger hur mycket datapunkten ska flyttas från mitten av pajen. Kan vara negativt; ett negativt värde betyder att egenskapen inte är satt och ingen explosion ska tillämpas. Gäller endast pajdiagram i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.drawing.charts/chartdatapoint/get_explosion/
---
## ChartDataPoint::get_Explosion method


Anger hur mycket datapunkten ska flyttas från mitten av pajen. Kan vara negativt, negativt betyder att egenskapen inte är satt och ingen explosion ska tillämpas. Gäller endast pajdiagram.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion() override
```


## Exempel



Visar hur man flyttar skivorna i ett pajdiagram bort från mitten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// "Slices" i ett pajdiagram kan flyttas bort från mitten med ett avstånd via respektive datapunkts Explosion‑attribut.
// Lägg till en datapunkt till den första delen av pajdiagrammet och flytta den bort från mitten med 10 enheter.
// Aspose.Words skapar datapunkter automatiskt om de inte finns.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Flytta den andra delen längre bort.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## Se även

* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
