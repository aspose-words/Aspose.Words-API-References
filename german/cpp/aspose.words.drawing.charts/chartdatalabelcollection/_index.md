---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection Klasse"
linktitle: "ChartDataLabelCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection Klasse. Stellt eine Sammlung von ChartDataLabel dar. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Stellt eine Sammlung von [ChartDataLabel](../chartdatalabel/) dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormat](./clearformat/)() | Löscht das Format aller [ChartDataLabel](../chartdatalabel/) in dieser Sammlung. |
| [get_Count](./get_count/)() | Gibt die Anzahl der [ChartDataLabel](../chartdatalabel/) in dieser Sammlung zurück. |
| [get_Font](./get_font/)() | Stellt Zugriff auf die Schriftformatierung der Datenbeschriftungen der gesamten Serie bereit. |
| [get_Format](./get_format/)() | Stellt Zugriff auf Füll- und Linienformatierung der Datenbeschriftungen bereit. |
| [get_NumberFormat](./get_numberformat/)() | Ruft eine [ChartNumberFormat](../chartnumberformat/)-Instanz ab, die das Festlegen des Zahlenformats für die Datenbeschriftungen der gesamten Serie ermöglicht. |
| [get_Orientation](./get_orientation/)() | Liest oder legt die Textausrichtung der Datenbeschriftungen der gesamten Serie fest. |
| [get_Position](./get_position/)() | Liest oder legt die Position der Datenbeschriftungen fest. |
| [get_Rotation](./get_rotation/)() | Liest oder legt die Drehung der Datenbeschriftungen der gesamten Serie in Grad fest. |
| [get_Separator](./get_separator/)() | Liest oder legt das Zeichen zur Trennung von Zeichenketten für die Datenbeschriftungen der gesamten Serie fest. Standardmäßig ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und Prozentsatz anzeigen, dann wird stattdessen ein Zeilenumbruch verwendet. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Gilt nur für Blasendiagramme. Standardwert ist **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Standardwert ist **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Standardwert ist **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Ermöglicht die Angabe, ob Führungslinien der Datenbeschriftungen für die Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Standardwert ist **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Ermöglicht die Angabe, ob der Legenden‑Schlüssel für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Standardwert ist **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Ermöglicht die Angabe, ob der Prozentwert für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Standardwert ist **false**. Gilt nur für Kreisdiagramme. |
| [get_ShowSeriesName](./get_showseriesname/)() | Gibt einen Boolean zurück oder legt ihn fest, um das Anzeigeverhalten des Seriennamens für die Datenbeschriftungen der gesamten Serie anzugeben. **true**, um den Seriennamen anzuzeigen; **false**, um ihn zu verbergen. Standardmäßig **false**. |
| [get_ShowValue](./get_showvalue/)() | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Standardwert ist **false**. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Gibt [ChartDataLabel](../chartdatalabel/) für den angegebenen Index zurück. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Standardwert ist **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
