---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_BubbleSizes Methode"
linktitle: "get_BubbleSizes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_BubbleSizes Methode. Gibt eine Sammlung von Blasengrößen für diese Diagrammserie in C++ zurück."
type: docs
weight: 2500
url: /de/cpp/aspose.words.drawing.charts/chartseries/get_bubblesizes/
---
## ChartSeries::get_BubbleSizes method


Ermittelt eine Sammlung von Blasengrößen für diese Diagrammserie.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::BubbleSizeCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_BubbleSizes()
```


## Beispiele



Zeigt, wie man mit dem Formatcode der Diagrammdaten arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Blasendiagramm ein.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Lösche standardmäßig generierte Serie.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Datenbeschriftungen anzeigen.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Setzen Sie Datenformatcodes.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Siehe auch

* Class [BubbleSizeCollection](../../bubblesizecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
