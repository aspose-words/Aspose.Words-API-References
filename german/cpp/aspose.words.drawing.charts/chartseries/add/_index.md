---
title: "Aspose::Words::Drawing::Charts::ChartSeries::Add Methode"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::Add Methode. Fügt den angegebenen X‑Wert zur Diagrammreihe hinzu. Unterstützt die Reihe Y‑Werte und Blasengrößen, bleiben diese für den X‑Wert leer in C++."
type: docs
weight: 1250
url: /de/cpp/aspose.words.drawing.charts/chartseries/add/
---
## ChartSeries::Add(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) method


Fügt den angegebenen X-Wert zur Diagrammserie hinzu. Unterstützt die Serie Y-Werte und Blasengrößen, bleiben diese für den X-Wert leer.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Add(const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue)
```


## Beispiele



Zeigt, wie Diagrammreihen mit Daten gefüllt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Löscht X‑ und Y‑Werte der ersten Reihe.
series1->ClearValues();

// Füllen Sie die Reihe mit Daten.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Löscht X‑ und Y‑Werte der zweiten Reihe.
series2->Clear();

// Füllen Sie die Reihe mit Daten.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Siehe auch

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Add(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) method


Fügt die angegebenen X- und Y-Werte zur Diagrammserie hinzu.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Add(const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue)
```


## Beispiele



Zeigt, wie Diagrammreihen mit Daten gefüllt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Löscht X‑ und Y‑Werte der ersten Reihe.
series1->ClearValues();

// Füllen Sie die Reihe mit Daten.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Löscht X‑ und Y‑Werte der zweiten Reihe.
series2->Clear();

// Füllen Sie die Reihe mit Daten.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```


Zeigt, wie Diagrammdatenwerte hinzugefügt/entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department1Series = chart->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> department2Series = chart->get_Series()->idx_get(1);

// Entfernen Sie den ersten Wert in beiden Serien.
department1Series->Remove(0);
department2Series->Remove(0);

// Fügen Sie neue Werte zu beiden Serien hinzu.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> newXCategory = Aspose::Words::Drawing::Charts::ChartXValue::FromString(u"Q1, 2023");
department1Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10.3));
department2Series->Add(newXCategory, Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5.7));

doc->Save(get_ArtifactsDir() + u"Charts.ChartDataValues.docx");
```

## Siehe auch

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## ChartSeries::Add(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) method


Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße zur Diagrammserie hinzu.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeries::Add(const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartXValue> &xValue, const System::SharedPtr<Aspose::Words::Drawing::Charts::ChartYValue> &yValue, double bubbleSize)
```


## Beispiele



Zeigt, wie Diagrammreihen mit Daten gefüllt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = chart->get_Series()->idx_get(0);

// Löscht X‑ und Y‑Werte der ersten Reihe.
series1->ClearValues();

// Füllen Sie die Reihe mit Daten.
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(3), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(10), 10);
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(5), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(5));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(7), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(11));
series1->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(9));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series2 = chart->get_Series()->idx_get(1);
// Löscht X‑ und Y‑Werte der zweiten Reihe.
series2->Clear();

// Füllen Sie die Reihe mit Daten.
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(2), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(4));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(4), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(6), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(14));
series2->Add(Aspose::Words::Drawing::Charts::ChartXValue::FromDouble(8), Aspose::Words::Drawing::Charts::ChartYValue::FromDouble(7));

doc->Save(get_ArtifactsDir() + u"Charts.PopulateChartWithData.docx");
```

## Siehe auch

* Class [ChartXValue](../../chartxvalue/)
* Class [ChartYValue](../../chartyvalue/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
