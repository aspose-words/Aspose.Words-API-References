---
title: "Aspose::Words::Drawing::Charts::AxisBound Klasse"
linktitle: "AxisBound"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::AxisBound Klasse. Stellt die minimale oder maximale Grenze von Achsenwerten dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Stellt die minimale oder maximale Grenze von Achsenwerten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [AxisBound](./axisbound/)() | Erstellt eine neue Instanz, die angibt, dass die Achsengrenze automatisch von einer Textverarbeitungsanwendung bestimmt werden soll. |
| [AxisBound](./axisbound/)(double) | Erstellt eine Achsengrenze, die als Zahl dargestellt wird. |
| [AxisBound](./axisbound/)(System::DateTime) | Erstellt eine Achsengrenze, die als Datums‑Uhrzeit‑Wert dargestellt wird. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_IsAuto](./get_isauto/)() const | Gibt ein Flag zurück, das anzeigt, dass die Achsengrenze automatisch bestimmt werden soll. |
| [get_Value](./get_value/)() const | Gibt den numerischen Wert der Achsengrenze zurück. |
| [get_ValueAsDate](./get_valueasdate/)() | Gibt den als Datum/Uhrzeit dargestellten Wert der Achsengrenze zurück. |
| [GetHashCode](./gethashcode/)() const override | Dient als Hash-Funktion für diesen Typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Gibt eine benutzerfreundliche Zeichenkette zurück, die den Wert dieses Objekts anzeigt. |
| static [Type](./type/)() |  |
## Hinweise


Die Grenze kann als numerischer, Datum/Uhrzeit‑ oder ein spezieller "auto"‑Wert angegeben werden.

Die Instanzen dieser Klasse sind unveränderlich.

## Beispiele



Zeigt, wie man ein Diagramm mit Datum/Uhrzeit‑Werten einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine benutzerdefinierte Serie hinzu, die Datum/Uhrzeit‑Werte für die X‑Achse und entsprechende Dezimalwerte für die Y‑Achse enthält.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Legen Sie untere und obere Grenzen für die X‑Achse fest.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// Setzen Sie die Haupteinheiten der X‑Achse auf eine Woche und die Nebeneinheiten auf einen Tag.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Definieren Sie Y‑Achsen‑Eigenschaften für Dezimalwerte.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
