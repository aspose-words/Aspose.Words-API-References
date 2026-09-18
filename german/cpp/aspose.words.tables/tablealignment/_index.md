---
title: "Aspose::Words::Tables::TableAlignment enum"
linktitle: "TableAlignment"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::TableAlignment enum. Gibt die Ausrichtung für eine Inline-Tabelle in C++ an."
type: docs
weight: 14000
url: /de/cpp/aspose.words.tables/tablealignment/
---
## TableAlignment enum


Gibt die Ausrichtung für eine Inline-Tabelle an.

```cpp
enum class TableAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Links | 0 | Die Tabelle ist linksbündig ausgerichtet. |
| Mitte | 1 | Die Tabelle ist zentriert. |
| Rechts | 2 | Die Tabelle ist rechtsbündig ausgerichtet. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
