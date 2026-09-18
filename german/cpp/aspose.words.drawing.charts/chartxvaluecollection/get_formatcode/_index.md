---
title: "Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode Methode"
linktitle: "get_FormatCode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode Methode. Ruft den für die X‑Werte in C++ angewendeten Formatcode ab oder legt ihn fest."
type: docs
weight: 2500
url: /de/cpp/aspose.words.drawing.charts/chartxvaluecollection/get_formatcode/
---
## ChartXValueCollection::get_FormatCode method


Liest oder legt den Formatcode fest, der auf die X-Werte angewendet wird.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode()
```

## Hinweise


Die Zahlenformatierung wird verwendet, um die Darstellung von Werten im Diagramm zu ändern. Beispiele für Zahlenformate:

Zahl - "#,##0.00"

Währung - "\"\$\\"#,##0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Prozent - "0.00%"

Bruch - "# ?/?"

Wissenschaftlich - "0.00E+00"

Buchhaltung - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Benutzerdefiniert mit Farbe - "[Red]-#,##0.0"

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

* Class [ChartXValueCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
