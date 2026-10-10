---
title: "Aspose::Words::Tables::RowFormat::get_HeadingFormat Methode"
linktitle: "get_HeadingFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::RowFormat::get_HeadingFormat Methode. Wahr, wenn die Zeile als Tabellenüberschrift auf jeder Seite wiederholt wird, wenn die Tabelle mehr als eine Seite umfasst, in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


True, wenn die Zeile als Tabellenüberschrift auf jeder Seite wiederholt wird, wenn die Tabelle mehr als eine Seite umfasst.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Beispiele



Zeigt, wie man eine Tabelle mit Zeilen erstellt, die auf jeder Seite wiederholt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Alle Zeilen, die eingefügt werden, während das Flag "HeadingFormat" auf "true" gesetzt ist
// werden oben in der Tabelle auf jeder Seite, die sie erstreckt, angezeigt.
builder->get_RowFormat()->set_HeadingFormat(true);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_CellFormat()->set_Width(100);
builder->InsertCell();
builder->Write(u"Heading row 1");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Heading row 2");
builder->EndRow();

builder->get_CellFormat()->set_Width(50);
builder->get_ParagraphFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeadingFormat(false);

// Fügen Sie genügend Zeilen hinzu, damit die Tabelle zwei Seiten umfasst.
for (int32_t i = 0; i < 50; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 1.", table->get_Rows()->get_Count()));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 2.", table->get_Rows()->get_Count()));
    builder->EndRow();
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableSetHeadingRow.docx");
```

## Siehe auch

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
