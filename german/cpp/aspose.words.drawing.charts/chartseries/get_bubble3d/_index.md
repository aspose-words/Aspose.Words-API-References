---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D Methode"
linktitle: "get_Bubble3D"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D Methode. Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing.charts/chartseries/get_bubble3d/
---
## ChartSeries::get_Bubble3D method


Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D() override
```


## Beispiele



Zeigt, wie man 3D‑Effekte mit Blasendiagrammen verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Wenden Sie ein Datenetikett auf jede Blase an, das ihren Durchmesser anzeigt.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## Siehe auch

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
