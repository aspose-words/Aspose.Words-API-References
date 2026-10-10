---
title: "Metodo Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D"
linktitle: "get_Bubble3D"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D. Specifica se le bolle nel grafico a bolle devono avere un effetto 3-D applicato in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/chartseries/get_bubble3d/
---
## ChartSeries::get_Bubble3D method


Specifica se le bolle nel grafico a bolle devono avere un effetto 3-D applicato.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D() override
```


## Esempi



Mostra come utilizzare gli effetti 3D con i grafici a bolle.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble3D, 500, 350);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_TRUE(chart->get_Series()->idx_get(0)->get_Bubble3D());

// Applica un'etichetta dati a ogni bolla che visualizza il suo diametro.
for (int32_t i = 0; i < 3; i++)
{
    chart->get_Series()->idx_get(0)->set_HasDataLabels(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->set_ShowBubbleSize(true);
    chart->get_Series()->idx_get(0)->get_DataLabels()->idx_get(i)->get_Font()->set_Size(12);
}

doc->Save(get_ArtifactsDir() + u"Charts.Bubble3D.docx");
```

## Vedi anche

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
