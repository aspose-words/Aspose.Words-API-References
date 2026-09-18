---
title: "Aspose::Words::Drawing::Charts::Chart‑Klasse"
linktitle: "Diagramm"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::Chart‑Klasse. Bietet Zugriff auf die Eigenschaften der Diagrammform. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Bietet Zugriff auf die Eigenschaften der Diagrammform. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Axes](./get_axes/)() | Gibt eine Sammlung aller Achsen dieses Diagramms zurück. |
| [get_AxisX](./get_axisx/)() | Bietet Zugriff auf die Eigenschaften der primären X‑Achse des Diagramms. |
| [get_AxisY](./get_axisy/)() | Bietet Zugriff auf die Eigenschaften der primären Y‑Achse des Diagramms. |
| [get_AxisZ](./get_axisz/)() | Bietet Zugriff auf die Eigenschaften der Z‑Achse des Diagramms. |
| [get_DataTable](./get_datatable/)() | Bietet Zugriff auf die Eigenschaften einer Datentabelle dieses Diagramms. Die Datentabelle kann über die Eigenschaft [Show](../chartdatatable/get_show/) angezeigt werden. |
| [get_Format](./get_format/)() | Bietet Zugriff auf die Füll‑ und Linienformatierung des Diagramms. |
| [get_Legend](./get_legend/)() | Stellt Zugriff auf die Eigenschaften der Diagrammlegende bereit. |
| [get_Series](./get_series/)() | Stellt Zugriff auf die Series-Sammlung bereit. |
| [get_SeriesGroups](./get_seriesgroups/)() | Stellt Zugriff auf eine Series-Gruppensammlung dieses Diagramms bereit. |
| [get_SourceFullName](./get_sourcefullname/)() | Ermittelt den Pfad und Namen einer xls/xlsx-Datei, mit der dieses Diagramm verknüpft ist. |
| [get_Style](./get_style/)() | Ermittelt den Stil des Diagramms. |
| [get_Title](./get_title/)() | Stellt Zugriff auf die Eigenschaften des Diagrammtitels bereit. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Setzt den Stil des Diagramms. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man ein Diagramm einfügt und einen Titel festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie mit einem DocumentBuilder ein Diagramm-Shape ein und erhalten Sie dessen Diagramm.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Verwenden Sie die Eigenschaft "Title", um unserem Diagramm einen Titel zu geben, der oben mittig im Diagrammbereich erscheint.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Setzen Sie die Eigenschaft "Show" auf "true", um den Titel sichtbar zu machen.
title->set_Show(true);

// Setzen Sie die Eigenschaft "Overlay" auf "true", um anderen Diagrammelementen mehr Platz zu geben, indem sie den Titel überlappen dürfen.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
