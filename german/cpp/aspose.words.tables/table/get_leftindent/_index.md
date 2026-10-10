---
title: "Aspose::Words::Tables::Table::get_LeftIndent Methode"
linktitle: "get_LeftIndent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::get_LeftIndent Methode. Liest oder setzt den Wert, der den linken Einzug der Tabelle in C++ darstellt."
type: docs
weight: 26000
url: /de/cpp/aspose.words.tables/table/get_leftindent/
---
## Table::get_LeftIndent method


Liest oder legt den Wert fest, der den linken Einzug der Tabelle darstellt.

```cpp
double Aspose::Words::Tables::Table::get_LeftIndent()
```


## Beispiele



Zeigt, wie man eine formatierte Tabelle mit [DocumentBuilder](../../../aspose.words/documentbuilder/) erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// Legen Sie einige Formatierungsoptionen für Text und Tabellendarstellung fest.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// Das Konfigurieren der Formatierungsoptionen in einem DocumentBuilder wendet sie an
// auf die aktuelle Zelle/Zeile, in der sich der Cursor befindet,
// sowie auf alle neuen Zellen und Zeilen, die mit diesem Builder erstellt werden.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// Konfigurieren Sie die Formatierungsobjekte des Builders neu für die neuen Zeilen und Zellen, die wir gleich erstellen.
// Der Builder wird diese nicht auf die bereits erstellte erste Zeile anwenden, damit sie als Kopfzeile hervorsticht.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
