---
title: "Aspose::Words::Drawing::Charts::ChartSeries class"
linktitle: "ChartSeries"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries class. Stellt Eigenschaften der Diagrammserie dar. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Stellt Eigenschaften einer Diagrammreihe dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Fügt den angegebenen X-Wert zur Diagrammserie hinzu. Unterstützt die Serie Y-Werte und Blasengrößen, bleiben diese für den X-Wert leer. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Fügt die angegebenen X- und Y-Werte zur Diagrammserie hinzu. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße zur Diagrammserie hinzu. |
| [Clear](./clear/)() | Entfernt alle Datenwerte aus der Diagrammserie. Das Format aller einzelnen Datenpunkte und Datenbeschriftungen wird zurückgesetzt. |
| [ClearValues](./clearvalues/)() | Entfernt alle Datenwerte aus der Diagrammserie, wobei das Format der Datenpunkte und Datenbeschriftungen erhalten bleibt. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Kopiert das Standardformat des Datenpunkts vom Datenpunkt mit dem angegebenen Index. |
| [get_Bubble3D](./get_bubble3d/)() override | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [get_BubbleSizes](./get_bubblesizes/)() | Ermittelt eine Sammlung von Blasengrößen für diese Diagrammserie. |
| [get_DataLabels](./get_datalabels/)() | Gibt die Einstellungen für die Datenbeschriftungen der gesamten Serie an. |
| [get_DataPoints](./get_datapoints/)() const | Gibt eine Sammlung von Formatierungsobjekten für alle Datenpunkte in dieser Serie zurück. |
| [get_Explosion](./get_explosion/)() override | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; negativ bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosionsverschiebung angewendet wird. Gilt nur für Kuchendiagramme. |
| [get_Format](./get_format/)() | Bietet Zugriff auf Füll‑ und Linienformatierung der Serie. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Ermittelt oder legt ein Flag fest, das angibt, ob Datenbeschriftungen für die Serie angezeigt werden. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| [get_LegendEntry](./get_legendentry/)() | Ermittelt einen Legendeintrag für diese Diagrammserie. |
| [get_Marker](./get_marker/)() override | Gibt einen Datenmarker an. Der Marker wird bei Bedarf automatisch erstellt. |
| [get_Name](./get_name/)() | Liefert den Namen der Serie, wenn der Name nicht explizit festgelegt ist, wird er anhand des Index generiert. Standardmäßig wird Series plus eins basierend auf dem Index zurückgegeben. |
| [get_SeriesType](./get_seriestype/)() | Liefert den Typ dieser Diagrammserie. |
| [get_Smooth](./get_smooth/)() const | Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mithilfe von Catmull‑Rom‑Splines geglättet werden soll. |
| [get_XValues](./get_xvalues/)() | Liefert eine Sammlung von X‑Werten für diese Diagrammserie. |
| [get_YValues](./get_yvalues/)() | Liefert eine Sammlung von Y‑Werten für diese Diagrammserie. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Fügt den angegebenen X‑Wert an der angegebenen Position in die Diagrammserie ein. Unterstützt die Serie Y‑Werte und Blasengrößen, bleiben diese für den X‑Wert leer. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Fügt die angegebenen X‑ und Y‑Werte an der angegebenen Position in die Diagrammserie ein. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Fügt den angegebenen X‑Wert, Y‑Wert und die Blasengröße an der angegebenen Position in die Diagrammserie ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Entfernt den X‑Wert, Y‑Wert und, falls unterstützt, die Blasengröße aus der Diagrammserie an der angegebenen Position. Der entsprechende Datenpunkt und das Datenbeschriftung werden ebenfalls entfernt. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Setter für [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; negativ bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosionsverschiebung angewendet wird. Gilt nur für Kuchendiagramme. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| [set_Name](./set_name/)(const System::String\&) | Setzt den Namen der Serie; ist der Name nicht explizit festgelegt, wird er anhand des Index generiert. Standardmäßig wird Series plus eins basierend auf dem Index zurückgegeben. |
| [set_Smooth](./set_smooth/)(bool) | Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mithilfe von Catmull‑Rom‑Splines geglättet werden soll. |
| static [Type](./type/)() |  |
## Siehe auch

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
