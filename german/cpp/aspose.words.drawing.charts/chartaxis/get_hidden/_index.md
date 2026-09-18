---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden Methode"
linktitle: "get_Hidden"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden Methode. Gibt ein Flag zurück oder legt es fest, das angibt, ob diese Achse verborgen ist oder nicht in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.drawing.charts/chartaxis/get_hidden/
---
## ChartAxis::get_Hidden method


Ermittelt oder legt ein Flag fest, das angibt, ob diese Achse ausgeblendet ist oder nicht.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_Hidden()
```


## Beispiele



Zeigt, wie Diagrammachsen ausgeblendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine benutzerdefinierte Serie mit Kategorien für die X‑Achse und entsprechenden Dezimalwerten für die Y‑Achse hinzu.
chart->get_Series()->Add(u"AW Series 1", System::MakeArray<System::String>({u"Item 1", u"Item 2", u"Item 3", u"Item 4", u"Item 5"}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2}));

// Blenden Sie die Diagrammachsen aus, um das Erscheinungsbild des Diagramms zu vereinfachen.
chart->get_AxisX()->set_Hidden(true);
chart->get_AxisY()->set_Hidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.HideChartAxis.docx");
```

## Siehe auch

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
