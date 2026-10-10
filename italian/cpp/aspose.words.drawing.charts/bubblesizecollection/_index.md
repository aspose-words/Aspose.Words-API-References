---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Rappresenta una raccolta di dimensioni delle bolle per una serie di grafico in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Rappresenta una raccolta di dimensioni delle bolle per una serie di grafico.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Restituisce il numero di elementi in questa raccolta. |
| [get_FormatCode](./get_formatcode/)() | Ottiene o imposta il codice di formato applicato alle dimensioni delle bolle. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta il valore della dimensione della bolla all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, double) | Ottiene o imposta il valore della dimensione della bolla all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Metodo impostatore per [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Note


La raccolta consente solo la modifica delle dimensioni delle bolle. Per aggiungere o inserire nuovi valori a una serie di grafico, o rimuovere valori, è possibile utilizzare i metodi appropriati della classe [ChartSeries](../chartseries/).

I valori vuoti delle dimensioni delle bolle sono rappresentati come **NaN**.

## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
