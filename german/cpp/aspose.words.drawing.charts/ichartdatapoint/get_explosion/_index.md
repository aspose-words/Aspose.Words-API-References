---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion Methode"
linktitle: "get_Explosion"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion Methode. Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben wird. Kann negativ sein; ein negativer Wert bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosion angewendet wird. Gilt nur für Kuchendiagramme in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing.charts/ichartdatapoint/get_explosion/
---
## IChartDataPoint::get_Explosion method


Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; negativ bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosionsverschiebung angewendet wird. Gilt nur für Kuchendiagramme.

```cpp
virtual int32_t Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion()=0
```


## Beispiele



Zeigt, wie man die Segmente eines Kuchendiagramms vom Mittelpunkt entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Sales", chart->get_Series()->idx_get(0)->get_Name());

// \"Slices\" eines Kuchendiagramms können über das Explosion‑Attribut des jeweiligen Datenpunkts um einen Abstand vom Mittelpunkt entfernt werden.
// Fügen Sie dem ersten Abschnitt des Kuchendiagramms einen Datenpunkt hinzu und verschieben Sie ihn um 10 Punkte vom Mittelpunkt.
// Aspose.Words erstellt Datenpunkte automatisch, wenn sie nicht vorhanden sind.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataPoint> dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(0);
dataPoint->set_Explosion(10);

// Verschieben Sie den zweiten Abschnitt um einen größeren Abstand.
dataPoint = chart->get_Series()->idx_get(0)->get_DataPoints()->idx_get(1);
dataPoint->set_Explosion(40);

doc->Save(get_ArtifactsDir() + u"Charts.PieChartExplosion.docx");
```

## Siehe auch

* Interface [IChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
