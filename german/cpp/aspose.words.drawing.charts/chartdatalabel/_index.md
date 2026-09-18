---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. Stellt eine Datenbeschriftung an einem Diagrammpunkt oder einer Trendlinie dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Stellt ein Datenbeschriftungselement an einem Diagrammpunkt oder einer Trendlinie dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormat](./clearformat/)() | Löscht das Format dieser Datenbeschriftung. Die Eigenschaften werden auf die Standardwerte zurückgesetzt, die in der übergeordneten Datenbeschriftungssammlung definiert sind. |
| [get_Font](./get_font/)() | Bietet Zugriff auf die Schriftformatierung dieser Datenbeschriftung. |
| [get_Format](./get_format/)() | Bietet Zugriff auf die Füll- und Linienformatierung der Datenbeschriftung. |
| [get_Index](./get_index/)() | Gibt den Index des enthaltenden Elements an. Dieser Index bestimmt, auf welche Kindersammlung des übergeordneten Elements dieses Element angewendet wird. Standardwert ist 0. |
| [get_IsHidden](./get_ishidden/)() | Liest/setzt ein Flag, das angibt, ob diese Beschriftung ausgeblendet ist. Der Standardwert ist **false**. |
| [get_IsVisible](./get_isvisible/)() | Gibt **true** zurück, wenn diese Datenbeschriftung etwas anzuzeigen hat. |
| [get_Left](./get_left/)() | Liest oder setzt den Abstand der Datenbeschriftung in Punkten vom linken Rand des Diagramms oder von der durch die [Position](./get_position/) Eigenschaft angegebenen Position, abhängig vom Wert der [LeftMode](./get_leftmode/) Eigenschaft. |
| [get_LeftMode](./get_leftmode/)() | Liest oder setzt den Interpretationsmodus des [Left](./get_left/) Eigenschaftswerts: ob er den Ort der Datenbeschriftung vom linken Rand des Diagramms oder von der durch die [Position](./get_position/) Eigenschaft angegebenen Position festlegt. |
| [get_NumberFormat](./get_numberformat/)() | Gibt das Zahlenformat des übergeordneten Elements zurück. |
| [get_Orientation](./get_orientation/)() | Liest oder setzt die Ausrichtung des Beschriftungstextes. |
| [get_Position](./get_position/)() | Liest oder setzt die Position der Datenbeschriftung. |
| [get_Rotation](./get_rotation/)() | Liest oder setzt die Drehung der Beschriftung in Grad. |
| [get_Separator](./get_separator/)() | Liest das Zeichenketten-Trennzeichen, das für die Datenbeschriftungen in einem Diagramm verwendet wird. Standard ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und Prozentsatz anzeigen, wo stattdessen ein Zeilenumbruch verwendet wird. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Gilt nur für Blasendiagramme. Standardwert ist **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen angezeigt werden sollen. Standardwert ist **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Ermöglicht die Angabe, ob Datenbeschriftungs-Leitlinien angezeigt werden sollen. Standardwert ist **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Ermöglicht die Angabe, ob der Legenden-Schlüssel für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Ermöglicht die Angabe, ob der Prozentwert für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Gibt einen Boolean zurück, der das Anzeigeverhalten des Seriennamens für die Datenbeschriftungen in einem Diagramm angibt. **true**, um den Seriennamen anzuzeigen; **false**, um ihn zu verbergen. Standardmäßig **false**. |
| [get_ShowValue](./get_showvalue/)() | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen angezeigt werden sollen. Standardwert ist **false**. |
| [get_Top](./get_top/)() | Liest oder setzt den Abstand der Datenbeschriftung in Punkten vom oberen Rand des Diagramms oder von der durch die Eigenschaft [Position](./get_position/) angegebenen Position, abhängig vom Wert der Eigenschaft [TopMode](./get_topmode/). |
| [get_TopMode](./get_topmode/)() | Liest oder setzt den Interpretationsmodus des Werts der Eigenschaft [Top](./get_top/): ob er den Ort der Datenbeschriftung vom oberen Rand des Diagramms oder von der durch die Eigenschaft [Position](./get_position/) angegebenen Position festlegt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Liest/setzt ein Flag, das angibt, ob diese Beschriftung ausgeblendet ist. Der Standardwert ist **false**. |
| [set_Left](./set_left/)(double) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Legt das Zeichen fest, das als Trennzeichen für die Datenbeschriftungen in einem Diagramm verwendet wird. Standardmäßig ist es ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, dann wird stattdessen ein Zeilenumbruch verwendet. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen angezeigt werden sollen. Standardwert ist **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Ermöglicht die Angabe, ob Datenbeschriftungs-Leitlinien angezeigt werden sollen. Standardwert ist **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Ermöglicht die Angabe, ob der Legenden-Schlüssel für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Ermöglicht die Angabe, ob der Prozentwert für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Legt einen Boolean fest, der das Anzeigeverhalten des Seriennamens für die Datenbeschriftungen in einem Diagramm angibt. **true**, um den Seriennamen anzuzeigen; **false**, um ihn zu verbergen. Standardmäßig **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen angezeigt werden sollen. Standardwert ist **false**. |
| [set_Top](./set_top/)(double) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
