---
title: "Metodo get_Axes di Aspose::Words::Drawing::Charts::Chart"
linktitle: "get_Axes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Axes di Aspose::Words::Drawing::Charts::Chart. Restituisce una raccolta di tutti gli assi di questo grafico in C++."
type: docs
weight: 1500
url: /it/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


Ottiene una collezione di tutti gli assi di questo grafico.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## Esempi



Mostra come lavorare con la raccolta degli assi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Nascondi le linee della griglia principale sugli assi Y primario e secondario.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## Vedi anche

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
