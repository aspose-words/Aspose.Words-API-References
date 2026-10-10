---
title: "Classe Aspose::Words::Drawing::Charts::ChartDataPoint"
linktitle: "ChartDataPoint"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Drawing::Charts::ChartDataPoint. Consente di specificare la formattazione di un singolo punto dati nel grafico. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Consente di specificare la formattazione di un singolo punto dati sul grafico. Per saperne di più, visita l'articolo di documentazione [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [ClearFormat](./clearformat/)() | Cancella la formattazione di questo punto dati. Le proprietà vengono impostate ai valori predefiniti definiti nella serie genitore. |
| [get_Bubble3D](./get_bubble3d/)() override | Specifica se le bolle nel grafico a bolle devono avere un effetto 3-D applicato. |
| [get_Explosion](./get_explosion/)() override | Specifica la quantità di spostamento del punto dati dal centro della torta. Può essere negativo; un valore negativo indica che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| [get_Format](./get_format/)() | Fornisce l'accesso alla formattazione di riempimento e linea di questo punto dati. |
| [get_Index](./get_index/)() | Indice del punto dati a cui questo oggetto applica la formattazione. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| [get_Marker](./get_marker/)() override | Specifica il marcatore dei dati del grafico. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Specifica se le bolle nel grafico a bolle devono avere un effetto 3-D applicato. |
| [set_Explosion](./set_explosion/)(int32_t) override | Metodo impostatore per [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| static [Type](./type/)() |  |
## Vedi anche

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
