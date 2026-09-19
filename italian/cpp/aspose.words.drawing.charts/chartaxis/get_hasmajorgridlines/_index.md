---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines metodo"
linktitle: "get_HasMajorGridlines"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines metodo. Ottiene o imposta un flag che indica se l'asse ha linee della griglia principali in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.drawing.charts/chartaxis/get_hasmajorgridlines/
---
## ChartAxis::get_HasMajorGridlines method


Ottiene o imposta un flag che indica se l'asse ha linee di griglia principali.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_HasMajorGridlines()
```


## Esempi



Mostra come inserire un grafico con valori data/ora.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Aggiungi una serie personalizzata contenente valori data/ora per l'asse X e i rispettivi valori decimali per l'asse Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Imposta i limiti inferiore e superiore per l'asse X.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// Imposta le unità principali dell'asse X a una settimana e le unità secondarie a un giorno.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Definisci le proprietà dell'asse Y per valori decimali.
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

## Vedi anche

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
