---
title: "Aspose::Words::Tables::Table::ClearShading Methode"
linktitle: "ClearShading"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::ClearShading Methode. Entfernt alle Schattierungen der Tabelle in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.tables/table/clearshading/
---
## Table::ClearShading method


Entfernt alle Schattierungen in der Tabelle.

```cpp
void Aspose::Words::Tables::Table::ClearShading()
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

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
