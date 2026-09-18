---
title: "Aspose::Words::Drawing::Charts::ChartLegend class"
linktitle: "ChartLegend"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartLegend class. Stellt Eigenschaften der Diagrammlegende dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Stellt Eigenschaften der Diagrammlegende dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Font](./get_font/)() | Bietet Zugriff auf die Standard‑Schriftformatierung von Legendeneinträgen. Um die Schriftformatierung für einen bestimmten Legendeneintrag zu überschreiben, verwenden Sie die[Font](../chartlegendentry/get_font/)‑Eigenschaft. |
| [get_Format](./get_format/)() | Bietet Zugriff auf die Füll‑ und Linienformatierung der Legende. |
| [get_LegendEntries](./get_legendentries/)() const | Gibt eine Sammlung von Legendeneinträgen für alle Reihen und Trendlinien des übergeordneten Diagramms zurück. |
| [get_Overlay](./get_overlay/)() const | Bestimmt, ob andere Diagrammelemente die Legende überlappen dürfen. Der Standardwert ist **false**. |
| [get_Position](./get_position/)() | Gibt die Position der Legende in einem Diagramm an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Setter für [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie das Aussehen der Legende eines Diagramms bearbeitet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Verschieben Sie die Legende des Diagramms in die obere rechte Ecke.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Geben Sie anderen Diagrammelementen, wie dem Diagramm selbst, mehr Platz, indem Sie ihnen erlauben, die Legende zu überlappen.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
