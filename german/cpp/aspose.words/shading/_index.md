---
title: "Aspose::Words::Shading class"
linktitle: "Schattierung"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Shading class. Enthält Schattierungsattribute für ein Objekt. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 60000
url: /de/cpp/aspose.words/shading/
---
## Shading class


Enthält Schattierungsattribute für ein Objekt. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class Shading : public Aspose::Words::InternableComplexAttr,
                public Aspose::Words::IComplexAttr
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Entfernt die Schattierung aus dem Objekt. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Shading\>\&) | Bestimmt, ob das angegebene [Shading](./) im Wert dem aktuellen [Shading](./) entspricht. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht. |
| [get_BackgroundPatternColor](./get_backgroundpatterncolor/)() | Liest oder legt fest die Farbe, die auf den Hintergrund des [Shading](./)-Objekts angewendet wird. |
| [get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/)() | Liest oder legt fest die Hintergrundmuster-Theme-Farbe im angewendeten Farbschema, das mit diesem [Shading](./)-Objekt verknüpft ist. |
| [get_BackgroundTintAndShade](./get_backgroundtintandshade/)() | Liest oder legt fest einen double-Wert, der eine Hintergrund-Theme-Farbe aufhellt oder abdunkelt. |
| [get_ForegroundPatternColor](./get_foregroundpatterncolor/)() | Liest oder legt fest die Farbe, die auf den Vordergrund des [Shading](./)-Objekts angewendet wird. |
| [get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/)() | Liest oder legt fest die Vordergrundmuster-Theme-Farbe im angewendeten Farbschema, das mit diesem [Shading](./)-Objekt verknüpft ist. |
| [get_ForegroundTintAndShade](./get_foregroundtintandshade/)() | Liest oder legt fest einen double-Wert, der eine Vordergrund-Theme-Farbe aufhellt oder abdunkelt. |
| [get_Texture](./get_texture/)() | Liest oder legt fest die Schattierungs-Textur. |
| [GetHashCode](./gethashcode/)() const override | Dient als Hash-Funktion für diesen Typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackgroundPatternColor](./set_backgroundpatterncolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Shading::get_BackgroundPatternColor](./get_backgroundpatterncolor/). |
| [set_BackgroundPatternThemeColor](./set_backgroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter für [Aspose::Words::Shading::get_BackgroundPatternThemeColor](./get_backgroundpatternthemecolor/). |
| [set_BackgroundTintAndShade](./set_backgroundtintandshade/)(double) | Setter für [Aspose::Words::Shading::get_BackgroundTintAndShade](./get_backgroundtintandshade/). |
| [set_ForegroundPatternColor](./set_foregroundpatterncolor/)(System::Drawing::Color) | Setter für [Aspose::Words::Shading::get_ForegroundPatternColor](./get_foregroundpatterncolor/). |
| [set_ForegroundPatternThemeColor](./set_foregroundpatternthemecolor/)(Aspose::Words::Themes::ThemeColor) | Setter für [Aspose::Words::Shading::get_ForegroundPatternThemeColor](./get_foregroundpatternthemecolor/). |
| [set_ForegroundTintAndShade](./set_foregroundtintandshade/)(double) | Setter für [Aspose::Words::Shading::get_ForegroundTintAndShade](./get_foregroundtintandshade/). |
| [set_Texture](./set_texture/)(Aspose::Words::TextureIndex) | Setter für [Aspose::Words::Shading::get_Texture](./get_texture/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man Rahmen- und Schattierungsfarbe beim Erstellen einer Tabelle anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Beginne eine Tabelle und lege eine Standardfarbe/Dicke für ihre Rahmen fest.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// Erstelle eine Zeile mit zwei Zellen, die unterschiedliche Hintergrundfarben haben.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// Setze die Zellenformatierung zurück, um die Hintergrundfarben zu deaktivieren
// setze eine benutzerdefinierte Rahmendicke für alle neuen Zellen, die vom Builder erstellt werden,
// und erstelle dann eine zweite Zeile.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```


Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## Siehe auch

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
