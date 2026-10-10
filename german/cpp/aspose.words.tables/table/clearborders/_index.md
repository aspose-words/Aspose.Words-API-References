---
title: "Aspose::Words::Tables::Table::ClearBorders Methode"
linktitle: "ClearBorders"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::ClearBorders Methode. Entfernt alle Tabellen- und Zellenränder dieser Tabelle in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.tables/table/clearborders/
---
## Table::ClearBorders method


Entfernt alle Tabellen- und Zellenränder in dieser Tabelle.

```cpp
void Aspose::Words::Tables::Table::ClearBorders()
```


## Beispiele



Zeigt, wie man einer Tabelle einen Umrandungsrahmen hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Richtet die Tabelle zentriert auf der Seite aus.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Entfernt alle vorhandenen Rahmen und Schattierungen aus der Tabelle.
table->ClearBorders();
table->ClearShading();

// Fügt der Umrandung der Tabelle grüne Rahmen hinzu.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Füllt die Zellen mit einer hellgrünen Vollfarbe.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```


Zeigt, wie man alle Rahmen einer Tabelle entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

// Ändern Sie die Farbe und Dicke des oberen Rahmens.
System::SharedPtr<Aspose::Words::Border> topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Double, 1.5, System::Drawing::Color::get_Red(), true);

ASPOSE_ASSERT_EQ(1.5, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Double, topBorder->get_LineStyle());

// Löschen Sie die Rahmen aller Zellen in der Tabelle und speichern Sie anschließend das Dokument.
table->ClearBorders();
doc->Save(get_ArtifactsDir() + u"Table.ClearBorders.docx");

// Überprüfen Sie die Werte der Tabelleneigenschaften, nachdem das Dokument erneut geöffnet wurde.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.ClearBorders.docx");
table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);

ASPOSE_ASSERT_EQ(0.0, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::None, topBorder->get_LineStyle());
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
