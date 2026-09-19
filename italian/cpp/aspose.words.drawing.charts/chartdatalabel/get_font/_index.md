---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Font metodo"
linktitle: "get_Font"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_Font metodo. Fornisce l'accesso alla formattazione del carattere di questa etichetta dati in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.drawing.charts/chartdatalabel/get_font/
---
## ChartDataLabel::get_Font method


Fornisce l'accesso alla formattazione del carattere di questa etichetta dati.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartDataLabel::get_Font()
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

* Class [Font](../../../aspose.words/font/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
