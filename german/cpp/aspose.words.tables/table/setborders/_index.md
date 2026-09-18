---
title: "Aspose::Words::Tables::Table::SetBorders-Methode"
linktitle: "SetBorders"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::SetBorders-Methode. Setzt alle Tabellengrenzen auf den angegebenen Linienstil, die Breite und die Farbe in C++."
type: docs
weight: 69000
url: /de/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


Setzt alle Tabellenränder auf den angegebenen Linienstil, die Breite und die Farbe.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | Der anzuwendende Linienstil. |
| lineWidth | double | Die einzustellende Linienbreite (in Punkten). |
| color | System::Drawing::Color | Die für den Rand zu verwendende Farbe. |

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


Zeigt, wie man alle Tabellengrenzen auf einmal formatiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Entfernt alle vorhandenen Grenzen aus der Tabelle.
table->ClearBorders();

// Setzen Sie eine einzelne grüne Linie, die als jeder äußere und innere Rand dieser Tabelle dient.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## Siehe auch

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
