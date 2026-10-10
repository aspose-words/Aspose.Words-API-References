---
title: "Aspose::Words::Drawing::Charts::ChartAxisTitle class"
linktitle: "ChartAxisTitle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxisTitle class. Bietet Zugriff auf die Eigenschaften des Achsentitels. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 5750
url: /de/cpp/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class


Bietet Zugriff auf die Eigenschaften des Achsentitels. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartAxisTitle : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Font](./get_font/)() | Bietet Zugriff auf die Schriftformatierung des Achsentitels. |
| [get_Format](./get_format/)() | Bietet Zugriff auf die Füll‑ und Linienformatierung des Achsentitels. |
| [get_Orientation](./get_orientation/)() | Liest oder setzt die Ausrichtung des Achsentiteltextes. |
| [get_Overlay](./get_overlay/)() | Bestimmt, ob andere Diagrammelemente den Titel überlappen dürfen. Der Standardwert ist **false**. |
| [get_Rotation](./get_rotation/)() | Liest oder setzt die Drehung des Achsentitels in Grad. |
| [get_Show](./get_show/)() | Bestimmt, ob der Titel für die Achse angezeigt werden soll. Der Standardwert ist **false**. |
| [get_Text](./get_text/)() | Liest oder setzt den Text des Achsentitels. Wenn **null** oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter für [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::ChartAxisTitle::get_Text](./get_text/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man den Achsentitel eines Diagramms festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Lösche standardmäßig generierte Serie.
seriesColl->Clear();

seriesColl->Add(u"AW Series 1", System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"}), System::MakeArray<double>({1, 2}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisXTitle = chart->get_AxisX()->get_Title();
chartAxisXTitle->set_Text(u"Categories");
chartAxisXTitle->set_Show(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisTitle> chartAxisYTitle = chart->get_AxisY()->get_Title();
chartAxisYTitle->set_Text(u"Values");
chartAxisYTitle->set_Show(true);
chartAxisYTitle->set_Overlay(true);
chartAxisYTitle->get_Font()->set_Size(12);
chartAxisYTitle->get_Font()->set_Color(System::Drawing::Color::get_Blue());

doc->Save(get_ArtifactsDir() + u"Charts.ChartAxisTitle.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
