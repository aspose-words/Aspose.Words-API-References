---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry Klasse"
linktitle: "ChartLegendEntry"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry Klasse. Stellt einen Diagrammlegendeeintrag dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Stellt einen Eintrag der Diagrammlegende dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Font](./get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Legendeeintrags bereit. |
| [get_IsHidden](./get_ishidden/)() const | Liest oder legt einen Wert fest, der angibt, ob dieser Eintrag in der Diagrammlegende ausgeblendet ist. Der Standardwert ist **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Hinweise


Ein Legendeeintrag entspricht einer bestimmten Diagrammreihe oder Trendlinie.

Der Text des Eintrags ist der Name der Reihe oder Trendlinie. Der Text kann nicht geändert werden.

## Beispiele



Zeigt, wie man mit einer Legenden‑Schriftart arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Standard‑Schriftgröße für alle Legendeeinträge festlegen.
chartLegend->get_Font()->set_Size(14);
// Schriftart für einen bestimmten Legendeeintrag ändern.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Legendeeintrag für Diagrammreihe abrufen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
