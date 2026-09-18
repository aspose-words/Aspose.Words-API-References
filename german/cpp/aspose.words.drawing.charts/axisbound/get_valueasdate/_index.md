---
title: "Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate-Methode"
linktitle: "get_ValueAsDate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate-Methode. Gibt den Wert der Achsenbegrenzung zurück, dargestellt als Datum/Zeit in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/axisbound/get_valueasdate/
---
## AxisBound::get_ValueAsDate method


Gibt den als Datum/Uhrzeit dargestellten Wert der Achsengrenze zurück.

```cpp
System::DateTime Aspose::Words::Drawing::Charts::AxisBound::get_ValueAsDate()
```


## Beispiele



Zeigt, wie benutzerdefinierte Achsenbegrenzungen festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine Serie mit zwei Dezimal-Arrays hinzu. Das erste Array enthält die X-Werte,
// und das zweite enthält die entsprechenden Y-Werte für Punkte im Streudiagramm.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// Standardmäßig wird eine Standardskalierung auf die X- und Y-Achsen des Diagramms angewendet,
// so dass beide Bereiche groß genug sind, um jeden X- und Y-Wert jeder Serie zu umfassen.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// Wir können eigene Achsenbegrenzungen definieren.
// In diesem Fall lassen wir beide, die X- und Y-Achsen, einen Bereich von 0 bis 10 anzeigen.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Erstellen Sie ein Liniendiagramm mit einer Serie, die einen Datumsbereich auf der X-Achse und Dezimalwerte für die Y-Achse erfordert.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// Wir können Achsenbegrenzungen auch in Form von Daten festlegen und das Diagramm auf einen Zeitraum beschränken.
// Das Festlegen des Bereichs auf 1980-1990 lässt die beiden Werte der Serie aus
// die außerhalb des Bereichs des Diagramms liegen.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## Siehe auch

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
