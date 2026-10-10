---
title: "Aspose::Words::Drawing::Charts::ChartDataPoint Klasse"
linktitle: "ChartDataPoint"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataPoint Klasse. Ermöglicht die Angabe der Formatierung eines einzelnen Datenpunkts im Diagramm. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Ermöglicht die Angabe der Formatierung eines einzelnen Datenpunkts im Diagramm. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormat](./clearformat/)() | Löscht das Format dieses Datenpunkts. Die Eigenschaften werden auf die Standardwerte zurückgesetzt, die in der übergeordneten Serie definiert sind. |
| [get_Bubble3D](./get_bubble3d/)() override | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [get_Explosion](./get_explosion/)() override | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; negativ bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosionsverschiebung angewendet wird. Gilt nur für Kuchendiagramme. |
| [get_Format](./get_format/)() | Stellt Zugriff auf die Füll- und Linienformatierung dieses Datenpunkts bereit. |
| [get_Index](./get_index/)() | Index des Datenpunkts, für den dieses Objekt die Formatierung anwendet. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| [get_Marker](./get_marker/)() override | Gibt den Diagrammdatenmarker an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [set_Explosion](./set_explosion/)(int32_t) override | Setter für [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| static [Type](./type/)() |  |
## Siehe auch

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
