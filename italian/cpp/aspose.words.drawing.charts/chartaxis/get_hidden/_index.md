---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden metodo"
linktitle: "get_Hidden"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden metodo. Ottiene o imposta un flag che indica se questo asse è nascosto o meno in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


Ottiene o imposta un flag che indica se questo asse è nascosto o meno.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## Esempi



Mostra come nascondere gli assi del grafico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Aggiungi una serie personalizzata con categorie per l'asse X e i relativi valori decimali per l'asse Y.
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// Nascondi gli assi del grafico per semplificare l'aspetto del grafico.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## Vedi anche

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
