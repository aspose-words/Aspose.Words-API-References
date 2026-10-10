---
title: "Aspose::Words::Drawing::Charts::ChartTitle Klasse"
linktitle: "ChartTitle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartTitle Klasse. Bietet Zugriff auf die Eigenschaften des Diagrammtitels. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 18000
url: /de/cpp/aspose.words.drawing.charts/charttitle/
---
## ChartTitle class


Bietet Zugriff auf die Eigenschaften des Diagrammtitels. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartTitle : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Font](./get_font/)() | Bietet Zugriff auf die Schriftformatierung des Diagrammtitels. |
| [get_Format](./get_format/)() | Bietet Zugriff auf die Füll- und Linienformatierung des Diagrammtitels. |
| [get_Orientation](./get_orientation/)() | Liest oder setzt die Ausrichtung des Diagrammtiteltextes. |
| [get_Overlay](./get_overlay/)() | Bestimmt, ob andere Diagrammelemente den Titel überlappen dürfen. Standardmäßig ist das Overlay **false**. |
| [get_Rotation](./get_rotation/)() | Liest oder setzt die Drehung des Diagrammtitels in Grad. |
| [get_Show](./get_show/)() | Bestimmt, ob der Titel für dieses Diagramm angezeigt werden soll. Der Standardwert ist **true**. |
| [get_Text](./get_text/)() | Liest oder setzt den Text des Diagrammtitels. Wenn **null** oder ein leerer Wert angegeben wird, wird ein automatisch generierter Titel angezeigt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Setter für [Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation](./get_orientation/). |
| [set_Overlay](./set_overlay/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartTitle::get_Overlay](./get_overlay/). |
| [set_Rotation](./set_rotation/)(int32_t) | Setter für [Aspose::Words::Drawing::Charts::ChartTitle::get_Rotation](./get_rotation/). |
| [set_Show](./set_show/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartTitle::get_Show](./get_show/). |
| [set_Text](./set_text/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::ChartTitle::get_Text](./get_text/). |
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
