---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint klass"
linktitle: "ChartDataPoint"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint klass. Tillåter att ange formatering av en enskild datapunkt i diagrammet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Tillåter att ange formatering av en enskild datapunkt på diagrammet. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormat](./clearformat/)() | Rensar formatet för denna datapunkt. Egenskaperna sätts till standardvärdena som definieras i den överordnade serien. |
| [get_Bubble3D](./get_bubble3d/)() override | Anger om bubblorna i bubbeldiagrammet ska ha en 3‑D‑effekt tillämpad. |
| [get_Explosion](./get_explosion/)() override | Anger hur mycket datapunkten ska flyttas från mitten av pajen. Kan vara negativt, negativt betyder att egenskapen inte är satt och ingen explosion ska tillämpas. Gäller endast pajdiagram. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllnings- och linjeformatering för denna datapunkt. |
| [get_Index](./get_index/)() | Index för den datapunkt som detta objekt tillämpar formatering på. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| [get_Marker](./get_marker/)() override | Anger diagramdatamarkör. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Anger om bubblorna i bubbeldiagrammet ska ha en 3‑D‑effekt tillämpad. |
| [set_Explosion](./set_explosion/)(int32_t) override | Inställningsmetod för [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| static [Type](./type/)() |  |
## Se även

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
