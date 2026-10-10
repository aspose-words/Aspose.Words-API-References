---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint interfaccia"
linktitle: "IChartDataPoint"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint interfaccia. Contiene le proprietà di un singolo punto dati sul grafico in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Contiene le proprietà di un singolo punto dati sul grafico.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Specifica se le bolle nel grafico a bolle devono avere un effetto 3-D applicato. |
| virtual [get_Explosion](./get_explosion/)() | Specifica la quantità di spostamento del punto dati dal centro della torta. Può essere negativo; un valore negativo indica che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| virtual [get_Marker](./get_marker/)() | Specifica un marcatore dati. Il marcatore viene creato automaticamente quando richiesto. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Impostatore per [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Impostatore per [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
