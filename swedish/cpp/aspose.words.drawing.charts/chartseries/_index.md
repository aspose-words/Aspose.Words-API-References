---
title: "Aspose::Words::Drawing::Charts::ChartSeries class"
linktitle: "ChartSeries"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartSeries class. Representerar diagramseriens egenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Representerar egenskaper för diagramserier. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Lägger till det angivna X‑värdet i diagramserien. Om serien stöder Y‑värden och bubbla‑storlekar kommer de att vara tomma för X‑värdet. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Lägger till de angivna X‑ och Y‑värdena i diagramserien. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Lägger till det angivna X‑värdet, Y‑värdet och bubbla‑storleken i diagramserien. |
| [Clear](./clear/)() | Tar bort alla datavärden från diagramserien. Formatet för alla enskilda datapunkter och datamärkningar rensas. |
| [ClearValues](./clearvalues/)() | Tar bort alla datavärden från diagramserien men bevarar formatet för datapunkterna och datamärkningarna. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Kopierar standardformatet för datapunkten från datapunkten med det angivna indexet. |
| [get_Bubble3D](./get_bubble3d/)() override | Anger om bubblorna i bubbeldiagrammet ska ha en 3‑D‑effekt tillämpad. |
| [get_BubbleSizes](./get_bubblesizes/)() | Hämtar en samling av bubbla‑storlekar för denna diagramserie. |
| [get_DataLabels](./get_datalabels/)() | Anger inställningarna för datamärkningarna för hela serien. |
| [get_DataPoints](./get_datapoints/)() const | Returnerar en samling formateringsobjekt för alla datapunkter i denna serie. |
| [get_Explosion](./get_explosion/)() override | Anger hur mycket datapunkten ska flyttas från mitten av pajen. Kan vara negativt, negativt betyder att egenskapen inte är satt och ingen explosion ska tillämpas. Gäller endast pajdiagram. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllnings- och linjeformatering för serien. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Hämtar eller anger en flagga som indikerar om datamärkningar visas för serien. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| [get_LegendEntry](./get_legendentry/)() | Hämtar ett förklaringspost för denna diagramserie. |
| [get_Marker](./get_marker/)() override | Anger en datamarkör. Markören skapas automatiskt när den begärs. |
| [get_Name](./get_name/)() | Hämtar namnet på serien, om namnet inte är angivet explicit genereras det med hjälp av index. Som standard returneras Series plus ett baserat på index. |
| [get_SeriesType](./get_seriestype/)() | Hämtar typen av denna diagramserie. |
| [get_Smooth](./get_smooth/)() const | Tillåter att ange om linjen som förbinder punkterna i diagrammet ska jämnas med Catmull-Rom-splines. |
| [get_XValues](./get_xvalues/)() | Hämtar en samling av X‑värden för denna diagramserie. |
| [get_YValues](./get_yvalues/)() | Hämtar en samling av Y‑värden för denna diagramserie. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Infogar det angivna X‑värdet i diagramserien på det angivna indexet. Om serien stöder Y‑värden och bubbla‑storlekar kommer de att vara tomma för X‑värdet. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Infogar de angivna X‑ och Y‑värdena i diagramserien på det angivna indexet. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Infogar det angivna X‑värdet, Y‑värdet och bubbla‑storleken i diagramserien på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Tar bort X‑värdet, Y‑värdet och bubbla‑storleken, om de stöds, från diagramserien på det angivna indexet. Motsvarande datapunkt och datalabel tas också bort. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Sättare för [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Anger hur mycket datapunkten ska flyttas från mitten av pajen. Kan vara negativt, negativt betyder att egenskapen inte är satt och ingen explosion ska tillämpas. Gäller endast pajdiagram. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| [set_Name](./set_name/)(const System::String\&) | Ställer in namnet på serien, om namnet inte är angivet explicit genereras det med hjälp av index. Som standard returneras Series plus ett baserat på index. |
| [set_Smooth](./set_smooth/)(bool) | Tillåter att ange om linjen som förbinder punkterna i diagrammet ska jämnas med Catmull-Rom-splines. |
| static [Type](./type/)() |  |
## Se även

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
