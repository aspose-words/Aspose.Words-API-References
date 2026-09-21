---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection klass"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection klass. Representerar en samling av ChartDataLabel. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Representerar en samling av [ChartDataLabel](../chartdatalabel/). För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormat](./clearformat/)() | Rensar formatet för alla [ChartDataLabel](../chartdatalabel/) i denna samling. |
| [get_Count](./get_count/)() | Returnerar antalet [ChartDataLabel](../chartdatalabel/) i denna samling. |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för dataetiketterna i hela serien. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllnings- och linjeformatering för dataetiketterna. |
| [get_NumberFormat](./get_numberformat/)() | Hämtar en [ChartNumberFormat](../chartnumberformat/)-instans som möjliggör att ange talformat för dataetiketterna i hela serien. |
| [get_Orientation](./get_orientation/)() | Hämtar eller anger textorienteringen för dataetiketterna i hela serien. |
| [get_Position](./get_position/)() | Hämtar eller anger positionen för dataetiketterna. |
| [get_Rotation](./get_rotation/)() | Hämtar eller anger rotationen för dataetiketterna i hela serien i grader. |
| [get_Separator](./get_separator/)() | Hämtar eller anger strängseparatorn som används för dataetiketterna i hela serien. Standardvärdet är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procentandel, då en radbrytning ska användas istället. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Tillåter att ange om bubbelstorlek ska visas för dataetiketterna i hela serien. Gäller endast för bubbeldiagram. Standardvärdet är **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Tillåter att ange om kategorinamn ska visas för dataetiketterna i hela serien. Standardvärdet är **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Tillåter att ange om värden från dataetikettintervallet ska visas i dataetiketterna i hela serien. Standardvärdet är **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Tillåter att ange om ledarlinjer för dataetiketter ska visas för dataetiketterna i hela serien. Standardvärdet är **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Tillåter att ange om legendnyckeln ska visas för dataetiketterna i hela serien. Standardvärdet är **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Tillåter att ange om procentvärdet ska visas för dataetiketterna i hela serien. Standardvärdet är **false**. Gäller endast för cirkeldiagram. |
| [get_ShowSeriesName](./get_showseriesname/)() | Returnerar eller anger ett Boolean‑värde för att indikera hur serienamnet ska visas för dataetiketterna i hela serien. **true** för att visa serienamnet; **false** för att dölja. Standard är **false**. |
| [get_ShowValue](./get_showvalue/)() | Tillåter att ange om värden ska visas i dataetiketterna i hela serien. Standardvärdet är **false**. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar [ChartDataLabel](../chartdatalabel/) för det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Tillåter att ange om värden från dataetikettintervallet ska visas i dataetiketterna i hela serien. Standardvärdet är **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Inställare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Inställare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Inställare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Inställare för [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
