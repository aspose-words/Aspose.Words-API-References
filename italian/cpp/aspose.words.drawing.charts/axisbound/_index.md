---
title: "Classe Aspose::Words::Drawing::Charts::AxisBound"
linktitle: "AxisBound"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Drawing::Charts::AxisBound. Rappresenta il limite minimo o massimo dei valori dell'asse. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Rappresenta il limite minimo o massimo dei valori dell'asse. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [AxisBound](./axisbound/)() | Crea una nuova istanza che indica che il limite dell'asse deve essere determinato automaticamente da un'applicazione di elaborazione testi. |
| [AxisBound](./axisbound/)(double) | Crea un limite dell'asse rappresentato come numero. |
| [AxisBound](./axisbound/)(System::DateTime) | Crea un limite dell'asse rappresentato come valore data/ora. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |
| [get_IsAuto](./get_isauto/)() const | Restituisce un flag che indica che il limite dell'asse deve essere determinato automaticamente. |
| [get_Value](./get_value/)() const | Restituisce il valore numerico del limite dell'asse. |
| [get_ValueAsDate](./get_valueasdate/)() | Restituisce il valore del limite dell'asse rappresentato come data/ora. |
| [GetHashCode](./gethashcode/)() const override | Funziona come funzione hash per questo tipo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Restituisce una stringa leggibile dall'utente che visualizza il valore di questo oggetto. |
| static [Type](./type/)() |  |
## Note


Il limite può essere specificato come numerico, data/ora o come valore speciale "auto".

Le istanze di questa classe sono immutabili.

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
