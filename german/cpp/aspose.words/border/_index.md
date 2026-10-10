---
title: "Aspose::Words::Border Klasse"
linktitle: "Border"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border Klasse. Stellt einen Rahmen eines Objekts dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words/border/
---
## Border class


Stellt einen Rahmen eines Objekts dar. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Border : public Aspose::Words::InternableComplexAttr,
               public Aspose::Words::IComplexAttr
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Setzt Rahmen-Eigenschaften auf Standardwerte zurück. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Border\>\&) | Bestimmt, ob der angegebene Rahmen im Wert dem aktuellen Rahmen entspricht. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_Color](./get_color/)() | Liefert oder setzt die Rahmenfarbe. |
| [get_DistanceFromText](./get_distancefromtext/)() | Liest oder setzt den Abstand des Rahmens vom Text oder vom Seitenrand in Punkten. |
| [get_IsVisible](./get_isvisible/)() | Gibt **true** zurück, wenn der [LineStyle](./get_linestyle/) nicht [None](../linestyle/) ist. |
| [get_LineStyle](./get_linestyle/)() | Liefert oder setzt den Rahmenstil. |
| [get_LineWidth](./get_linewidth/)() | Liefert oder setzt die Rahmenbreite in Punkten. |
| [get_Shadow](./get_shadow/)() | Liefert oder setzt einen Wert, der angibt, ob der Rahmen einen Schatten hat. |
| [get_ThemeColor](./get_themecolor/)() | Liest oder setzt die Themenfarbe im angewendeten Farbschema, die mit diesem [Border](./)-Objekt verknüpft ist. |
| [get_TintAndShade](./get_tintandshade/)() | Liest oder setzt einen Double-Wert, der eine Farbe aufhellt oder abdunkelt. |
| [GetHashCode](./gethashcode/)() const override | Dient als Hash-Funktion für diesen Typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Setter für [Aspose::Words::Border::get_Color](./get_color/). |
| [set_DistanceFromText](./set_distancefromtext/)(double) | Setter für [Aspose::Words::Border::get_DistanceFromText](./get_distancefromtext/). |
| [set_LineStyle](./set_linestyle/)(Aspose::Words::LineStyle) | Setter für [Aspose::Words::Border::get_LineStyle](./get_linestyle/). |
| [set_LineWidth](./set_linewidth/)(double) | Setter für [Aspose::Words::Border::get_LineWidth](./get_linewidth/). |
| [set_Shadow](./set_shadow/)(bool) | Setter für [Aspose::Words::Border::get_Shadow](./get_shadow/). |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | Setter für [Aspose::Words::Border::get_ThemeColor](./get_themecolor/). |
| [set_TintAndShade](./set_tintandshade/)(double) | Setter für [Aspose::Words::Border::get_TintAndShade](./get_tintandshade/). |
| static [Type](./type/)() |  |
## Hinweise


Rahmen können auf verschiedene Dokumentelemente angewendet werden, einschließlich Absatz, Textlauf innerhalb eines Absatzes oder einer Tabellenzelle.

## Beispiele



Zeigt, wie man eine von einem Rahmen umgebene Zeichenkette in ein Dokument einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


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

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
