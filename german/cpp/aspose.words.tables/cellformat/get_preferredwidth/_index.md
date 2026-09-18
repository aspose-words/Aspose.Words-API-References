---
title: "Aspose::Words::Tables::CellFormat::get_PreferredWidth-Methode"
linktitle: "get_PreferredWidth"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellFormat::get_PreferredWidth-Methode. Gibt die bevorzugte Breite der Zelle zurück oder legt sie fest in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Gibt die bevorzugte Breite der Zelle zurück oder legt sie fest.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Hinweise


Die bevorzugte Breite (zusammen mit der Auto-Fit-Option der Tabelle) bestimmt, wie die tatsächliche Breite der Zelle vom Tabellenlayout-Algorithmus berechnet wird. Das [Table](../../table/)-Layout kann von Aspose.Words durchgeführt werden, wenn es das Dokument speichert, oder von Microsoft Word, wenn es das Dokument anzeigt.

Die bevorzugte Breite kann in Punkten oder in Prozent angegeben werden. Die bevorzugte Breite kann auch als "auto" angegeben werden, was bedeutet, dass keine bevorzugte Breite festgelegt ist.

Der Standardwert ist [Auto](../../preferredwidth/auto/).

## Beispiele



Zeigt, wie man eine bevorzugte Breite für Tabellenzellen festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Es gibt zwei Möglichkeiten, die "PreferredWidth"-Klasse auf Tabellenzellen anzuwenden.
// 1 - Setzen einer absoluten bevorzugten Breite basierend auf Punkten:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 - Setzen einer relativen bevorzugten Breite basierend auf dem Prozentsatz der Tabellenbreite:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Eine Zelle ohne angegebene bevorzugte Breite nimmt den restlichen verfügbaren Platz ein.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Jede Konfiguration der "PreferredWidth"-Eigenschaft erstellt ein neues Objekt.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Siehe auch

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
