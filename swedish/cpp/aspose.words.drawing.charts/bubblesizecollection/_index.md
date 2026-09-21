---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Representerar en samling av bubbelformsstorlekar för en diagramserie i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Representerar en samling av bubbelformer för en diagramserie.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Count](./get_count/)() | Hämtar antalet objekt i denna samling. |
| [get_FormatCode](./get_formatcode/)() | Hämtar eller anger formatkoden som tillämpas på bubbelformsstorlekarna. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar eller anger bubbelformsstorleksvärdet på det angivna indexet. |
| [idx_set](./idx_set/)(int32_t, double) | Hämtar eller anger bubbelformsstorleksvärdet på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Anmärkningar


Samlingen tillåter endast att ändra bubbelformsstorlekar. För att lägga till eller infoga nya värden i en diagramserie, eller ta bort värden, kan lämpliga metoder i klassen [ChartSeries](../chartseries/) användas.

Tomma bubbelformsstorleksvärden representeras som **NaN**.

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
