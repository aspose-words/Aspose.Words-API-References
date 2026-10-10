---
title: "Aspose::Words::Drawing::Charts::ChartFormat Klasse"
linktitle: "ChartFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartFormat Klasse. Stellt die Formatierung eines Diagrammelements dar. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 10000
url: /de/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Stellt die Formatierung eines Diagrammelements dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Fill](./get_fill/)() | Liefert die Füllformatierung für das übergeordnete Diagrammelement. |
| [get_IsDefined](./get_isdefined/)() | Liefert ein Flag, das angibt, ob ein Format definiert ist. |
| [get_ShapeType](./get_shapetype/)() | Liefert oder setzt den Formtyp des übergeordneten Diagrammelements. |
| [get_Stroke](./get_stroke/)() | Liefert die Linienformatierung für das übergeordnete Diagrammelement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | Setter für [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | Setzt die Füllung des Diagrammelements auf den Standardwert zurück. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man Diagrammformatierung verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Standardmäßig erzeugte Serien löschen.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Diagrammhintergrund formatieren.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Achsenbeschriftungen ausblenden.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Diagrammtitel formatieren.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Achsentitel formatieren.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Legende formatieren.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
