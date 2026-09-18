---
title: "Aspose::Words::Tables::Cell::get_CellFormat-Methode"
linktitle: "get_CellFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Cell::get_CellFormat-Methode. Bietet Zugriff auf die Formatierungseigenschaften der Zelle in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.tables/cell/get_cellformat/
---
## Cell::get_CellFormat method


Stellt Zugriff auf die Formatierungseigenschaften der Zelle bereit.

```cpp
System::SharedPtr<Aspose::Words::Tables::CellFormat> Aspose::Words::Tables::Cell::get_CellFormat()
```


## Beispiele



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


Zeigt, wie man die Zeilen aus zwei Tabellen zu einer kombiniert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Unten sind zwei Möglichkeiten, eine Tabelle aus einem Dokument zu erhalten.
// 1 -  Aus der "Tables"-Sammlung eines Body-Knotens:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  Verwendung der "GetChild"-Methode:
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Füge alle Zeilen der aktuellen Tabelle zur nächsten hinzu.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Entferne den leeren Tabellenkontainer.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## Siehe auch

* Class [CellFormat](../../cellformat/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
