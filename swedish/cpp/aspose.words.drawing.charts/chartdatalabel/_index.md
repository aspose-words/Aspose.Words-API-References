---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. Representerar dataetikett på en diagrampunkt eller trendlinje. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Representerar datamärkning på en diagrampunkt eller trendlinje. För att lära dig mer, besök dokumentationsartikeln [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [ClearFormat](./clearformat/)() | Rensar formatet för denna dataetikett. Egenskaperna sätts till standardvärdena som definieras i den överordnade dataetikettssamlingen. |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för denna dataetikett. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllnings- och linjeformatering för dataetiketten. |
| [get_Index](./get_index/)() | Anger indexet för det innehållande elementet. Detta index ska bestämma vilken av förälderns underordnade samling detta element gäller för. Standardvärdet är 0. |
| [get_IsHidden](./get_ishidden/)() | Hämtar/ställer in en flagga som indikerar om denna etikett är dold. Standardvärdet är **false**. |
| [get_IsVisible](./get_isvisible/)() | Returnerar **true** om denna dataetikett har något att visa. |
| [get_Left](./get_left/)() | Hämtar eller anger avståndet för dataetiketten i punkter från diagrammets vänstra kant eller från den position som anges av dess [Position](./get_position/) egenskap, beroende på värdet av [LeftMode](./get_leftmode/) egenskapen. |
| [get_LeftMode](./get_leftmode/)() | Hämtar eller anger tolkningsläget för värdet i [Left](./get_left/) egenskapen: om den anger placeringen av dataetiketten från diagrammets vänstra kant eller från den position som anges av dess [Position](./get_position/) egenskap. |
| [get_NumberFormat](./get_numberformat/)() | Returnerar talformatet för det överordnade elementet. |
| [get_Orientation](./get_orientation/)() | Hämtar eller anger orienteringen för etiketttexten. |
| [get_Position](./get_position/)() | Hämtar eller anger positionen för dataetiketten. |
| [get_Rotation](./get_rotation/)() | Hämtar eller anger rotationen för etiketten i grader. |
| [get_Separator](./get_separator/)() | Hämtar strängseparatorn som används för dataetiketterna i ett diagram. Standard är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procent, då en radbrytning ska användas istället. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Tillåter att ange om bubbelstorlek ska visas för dataetiketterna i ett diagram. Gäller endast för bubbeldiagram. Standardvärdet är **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Tillåter att ange om kategorinamn ska visas för dataetiketterna i ett diagram. Standardvärdet är **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Tillåter att ange om värden från dataetikettintervallet ska visas i dataetiketterna. Standardvärdet är **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Tillåter att ange om ledarlinjer för dataetiketter ska visas. Standardvärdet är **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Tillåter att ange om legendnyckeln ska visas för datamärkningarna på ett diagram. Standardvärdet är **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Tillåter att ange om procentvärdet ska visas för datamärkningarna på ett diagram. Standardvärdet är **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Returnerar en Boolean för att ange hur serienamnet ska visas för datamärkningarna på ett diagram. **true** för att visa serienamnet; **false** för att dölja. Standard är **false**. |
| [get_ShowValue](./get_showvalue/)() | Tillåter att ange om värden ska visas i datamärkningarna. Standardvärdet är **false**. |
| [get_Top](./get_top/)() | Hämtar eller anger avståndet för datamärket i punkter från diagrammets övre kant eller från den position som anges av dess [Position](./get_position/) egenskap, beroende på värdet i [TopMode](./get_topmode/) egenskapen. |
| [get_TopMode](./get_topmode/)() | Hämtar eller anger tolkningsläget för värdet i [Top](./get_top/) egenskapen: om det anger placeringen av datamärket från diagrammets övre kant eller från den position som anges av dess [Position](./get_position/) egenskap. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Hämtar/ställer in en flagga som indikerar om denna etikett är dold. Standardvärdet är **false**. |
| [set_Left](./set_left/)(double) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Anger teckenseparatorn som används för datamärkningarna på ett diagram. Standard är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procent, då ska en radbrytning användas istället. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Tillåter att ange om kategorinamn ska visas för dataetiketterna i ett diagram. Standardvärdet är **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Tillåter att ange om värden från dataetikettintervallet ska visas i dataetiketterna. Standardvärdet är **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Tillåter att ange om ledarlinjer för dataetiketter ska visas. Standardvärdet är **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Tillåter att ange om legendnyckeln ska visas för datamärkningarna på ett diagram. Standardvärdet är **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Tillåter att ange om procentvärdet ska visas för datamärkningarna på ett diagram. Standardvärdet är **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Anger en Boolean för att ange hur serienamnet ska visas för datamärkningarna på ett diagram. **true** för att visa serienamnet; **false** för att dölja. Standard är **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Tillåter att ange om värden ska visas i datamärkningarna. Standardvärdet är **false**. |
| [set_Top](./set_top/)(double) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
