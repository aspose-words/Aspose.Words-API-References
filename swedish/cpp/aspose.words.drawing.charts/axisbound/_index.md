---
title: "Aspose::Words::Drawing::Charts::AxisBound klass"
linktitle: "AxisBound"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::AxisBound klass. Representerar minimum- eller maximumgräns för axelvärden. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Representerar minimum- eller maximumgräns för axelvärden. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [AxisBound](./axisbound/)() | Skapar en ny instans som indikerar att axelgränsen ska bestämmas automatiskt av ett ordbehandlingsprogram. |
| [AxisBound](./axisbound/)(double) | Skapar en axelgräns representerad som ett tal. |
| [AxisBound](./axisbound/)(System::DateTime) | Skapar en axelgräns representerad som ett datum/tidsvärde. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_IsAuto](./get_isauto/)() const | Returnerar en flagga som indikerar att axelgränsen ska bestämmas automatiskt. |
| [get_Value](./get_value/)() const | Returnerar numeriskt värde för axelgränsen. |
| [get_ValueAsDate](./get_valueasdate/)() | Returnerar värdet för axelgränsen representerat som datum/tid. |
| [GetHashCode](./gethashcode/)() const override | Fungerar som en hash-funktion för denna typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Returnerar en användarvänlig sträng som visar värdet för detta objekt. |
| static [Type](./type/)() |  |
## Anmärkningar


Gränsen kan specificeras som ett numeriskt, datum/tids- eller ett speciellt "auto"-värde.

Instanserna av den här klassen är oföränderliga.

## Exempel



Visar hur man infogar ett diagram med datum/tidsvärden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Rensa diagrammets demodata-serie för att börja med ett rent diagram.
chart->get_Series()->Clear();

// Lägg till en anpassad serie som innehåller datum/tidsvärden för X-axeln och respektive decimala värden för Y-axeln.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Ställ in lägre och övre gränser för X-axeln.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// Ställ in huvudintervallen för X-axeln till en vecka och delintervallen till en dag.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Definiera Y-axelns egenskaper för decimala värden.
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

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
