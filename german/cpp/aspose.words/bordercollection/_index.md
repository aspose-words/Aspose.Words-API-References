---
title: "Aspose::Words::BorderCollection class"
linktitle: "BorderCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection class. Eine Sammlung von Border-Objekten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words/bordercollection/
---
## BorderCollection class


Eine Sammlung von [Border](../border/) Objekten. Weitere Informationen finden Sie im Dokumentationsartikel [Programmierung mit Dokumenten](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class BorderCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Border>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Entfernt alle Rahmen eines Objekts. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::BorderCollection\>\&) | Vergleicht Sammlungen von Rahmen. |
| [get_Bottom](./get_bottom/)() | Liefert den unteren Rahmen. |
| [get_Color](./get_color/)() | Liefert oder setzt die Rahmenfarbe. |
| [get_Count](./get_count/)() | Liefert die Anzahl der Rahmen in der Sammlung. |
| [get_DistanceFromText](./get_distancefromtext/)() | Liefert oder setzt den Abstand des Rahmens vom Text in Punkten. |
| [get_Horizontal](./get_horizontal/)() | Liefert den horizontalen Rahmen, der zwischen Zellen oder passenden Absätzen verwendet wird. |
| [get_Left](./get_left/)() | Liefert den linken Rahmen. |
| [get_LineStyle](./get_linestyle/)() | Liefert oder setzt den Rahmenstil. |
| [get_LineWidth](./get_linewidth/)() | Liefert oder setzt die Rahmenbreite in Punkten. |
| [get_Right](./get_right/)() | Liefert den rechten Rahmen. |
| [get_Shadow](./get_shadow/)() | Liefert oder setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat. |
| [get_Top](./get_top/)() | Liefert den oberen Rahmen. |
| [get_Vertical](./get_vertical/)() | Liefert den vertikalen Rahmen, der zwischen Zellen verwendet wird. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator-Objekt zurück, das verwendet werden kann, um über alle Rahmen in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::BorderType) | Ruft ein [Border](../border/) Objekt nach Rahmentyp ab. |
| [idx_get](./idx_get/)(int32_t) | Ruft ein [Border](../border/) Objekt nach Index ab. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::BorderCollection::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Setter für [Aspose::Words::BorderCollection::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Setter für [Aspose::Words::BorderCollection::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Setter für [Aspose::Words::BorderCollection::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Setter für [Aspose::Words::BorderCollection::get_Shadow](./get_shadow/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man einen Absatz mit einem oberen Rand einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// Setze ThemeColor nur, wenn LineWidth oder LineStyle gesetzt ist.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
