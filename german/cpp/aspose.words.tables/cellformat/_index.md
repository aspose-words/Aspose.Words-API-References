---
title: "Aspose::Words::Tables::CellFormat Klasse"
linktitle: "CellFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat Klasse. Stellt alle Formatierungen für eine Tabellenzelle dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Stellt die gesamte Formatierung für eine Tabellenzelle dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Setzt die Zellformatierung auf die Standardwerte zurück. Ändert nicht die Breite der Zelle. |
| [get_Borders](./get_borders/)() | Liefert die Sammlung der Zellrahmen. |
| [get_BottomPadding](./get_bottompadding/)() | Gibt die Menge des (in Punkten) hinzuzufügenden Abstands unter dem Zellinhalt zurück oder legt sie fest. |
| [get_FitText](./get_fittext/)() | Wenn **true**, wird der Text in der Zelle angepasst, indem jeder Absatz auf die Zellbreite komprimiert wird. |
| [get_HideMark](./get_hidemark/)() | Gibt die Sichtbarkeit der Zellmarkierung zurück. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Gibt an, wie die Zelle horizontal mit anderen Zellen in der Zeile zusammengeführt wird. |
| [get_LeftPadding](./get_leftpadding/)() | Gibt die Menge des (in Punkten) hinzuzufügenden Abstands links vom Zellinhalt zurück oder legt sie fest. |
| [get_Orientation](./get_orientation/)() | Gibt die Ausrichtung des Textes in einer Tabellenzelle zurück oder legt sie fest. |
| [get_PreferredWidth](./get_preferredwidth/)() | Gibt die bevorzugte Breite der Zelle zurück oder legt sie fest. |
| [get_RightPadding](./get_rightpadding/)() | Gibt die Menge des (in Punkten) hinzuzufügenden Abstands rechts vom Zellinhalt zurück oder legt sie fest. |
| [get_Shading](./get_shading/)() | Gibt ein [Shading](../../aspose.words/shading/) Objekt zurück, das sich auf die Schattierungsformatierung der Zelle bezieht. |
| [get_TopPadding](./get_toppadding/)() | Gibt die Menge des (in Punkten) hinzuzufügenden Abstands über dem Zellinhalt zurück oder legt sie fest. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Gibt die vertikale Ausrichtung des Textes in der Zelle zurück oder legt sie fest. |
| [get_VerticalMerge](./get_verticalmerge/)() | Gibt an, wie die Zelle vertikal mit anderen Zellen zusammengeführt wird. |
| [get_Width](./get_width/)() | Ermittelt die Breite der Zelle in Punkten. |
| [get_WrapText](./get_wraptext/)() | Wenn **true**, wird der Text für die Zelle umgebrochen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Setter für [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Setter für [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Legt die Sichtbarkeit der Zellmarkierung fest. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Setter für [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Setter für [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Setter für [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Setter für [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Setter für [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Setter für [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Setter für [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Setter für [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Setter für [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Setter für [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Legt die Menge an Abstand (in Punkten) fest, die links/oben/rechts/unten zum Inhalt der Zelle hinzugefügt wird. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man eine Tabelle mit benutzerdefinierten Rahmen erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Festlegen von Tabellenformatierungsoptionen für einen DocumentBuilder
// wird sie auf jede Zeile und Zelle anwenden, die wir damit hinzufügen.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Das Ändern der Formatierung wird sie auf die aktuelle Zelle anwenden,
// und auf alle neuen Zellen, die wir anschließend mit dem Builder erstellen.
// Dies wird die bereits zuvor hinzugefügten Zellen nicht beeinflussen.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Erhöhen Sie die Zeilenhöhe, um den vertikalen Text anzupassen.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


Zeigt, wie das Format von Zeilen und Zellen in einer Tabelle geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// Verwenden Sie die "RowFormat"-Eigenschaft der ersten Zeile, um die Formatierung zu ändern
// des Inhalts aller Zellen in dieser Zeile.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Verwenden Sie die "CellFormat"-Eigenschaft der ersten Zelle in der letzten Zeile, um die Formatierung des Inhalts dieser Zelle zu ändern.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Zeigt, wie die Formatierung einer Tabellenzelle geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Verwenden Sie die "CellFormat"-Eigenschaft einer Zelle, um die Formatierung festzulegen, die das Erscheinungsbild dieser Zelle ändert.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
