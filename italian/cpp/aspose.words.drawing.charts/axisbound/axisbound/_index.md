---
title: "Costruttore Aspose::Words::Drawing::Charts::AxisBound::AxisBound"
linktitle: "AxisBound"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::Drawing::Charts::AxisBound::AxisBound. Crea una nuova istanza che indica che il limite dell'asse deve essere determinato automaticamente da un'applicazione di elaborazione testi in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.drawing.charts/axisbound/axisbound/
---
## AxisBound::AxisBound() constructor


Crea una nuova istanza che indica che il limite dell'asse deve essere determinato automaticamente da un'applicazione di elaborazione testi.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound()
```


## Esempi



Mostra come impostare limiti personalizzati dell'asse.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart->get_Series()->Clear();

// Aggiungi una serie con due array decimali. Il primo array contiene i valori X,
// e il secondo contiene i valori Y corrispondenti per i punti nel grafico a dispersione.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.1, 5.4, 7.9, 3.5, 2.1, 9.7}), System::MakeArray<double>({2.1, 0.3, 0.6, 3.3, 1.4, 1.9}));

// Per impostazione predefinita, viene applicata una scala predefinita agli assi X e Y del grafico,
// in modo che entrambi i loro intervalli siano sufficientemente ampi da includere ogni valore X e Y di ogni serie.
ASSERT_TRUE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());

// Possiamo definire i nostri limiti dell'asse.
// In questo caso, faremo in modo che sia gli assi X che Y mostrino un intervallo da 0 a 10.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));
chart->get_AxisY()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(0.0));
chart->get_AxisY()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(10.0));

ASSERT_FALSE(chart->get_AxisX()->get_Scaling()->get_Minimum()->get_IsAuto());
ASSERT_FALSE(chart->get_AxisY()->get_Scaling()->get_Minimum()->get_IsAuto());

// Crea un grafico a linee con una serie che richiede un intervallo di date sull'asse X e valori decimali per l'asse Y.
chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
chart = chartShape->get_Chart();
chart->get_Series()->Clear();

System::ArrayPtr<System::DateTime> dates = System::MakeArray<System::DateTime>({System::DateTime(1973, 5, 11), System::DateTime(1981, 2, 4), System::DateTime(1985, 9, 23), System::DateTime(1989, 6, 28), System::DateTime(1994, 12, 15)});

chart->get_Series()->Add(u"Series 1", dates, System::MakeArray<double>({3.0, 4.7, 5.9, 7.1, 8.9}));

// Possiamo impostare i limiti dell'asse anche sotto forma di date, limitando il grafico a un periodo.
// Impostare l'intervallo a 1980-1990 escluderà due dei valori della serie
// che sono al di fuori dell'intervallo dal grafico.
chart->get_AxisX()->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1980, 1, 1)));
chart->get_AxisX()->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(1990, 1, 1)));

doc->Save(get_ArtifactsDir() + u"Charts.AxisBound.docx");
```

## Vedi anche

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## AxisBound::AxisBound(double) constructor


Crea un limite dell'asse rappresentato come numero.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(double value)
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

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
## AxisBound::AxisBound(System::DateTime) constructor


Crea un limite dell'asse rappresentato come valore data/ora.

```cpp
Aspose::Words::Drawing::Charts::AxisBound::AxisBound(System::DateTime datetime)
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

* Class [AxisBound](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
