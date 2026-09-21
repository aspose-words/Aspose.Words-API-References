---
title: "Aspose::Words::Tables::RowFormat::get_HeadingFormat‑metod"
linktitle: "get_HeadingFormat"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::RowFormat::get_HeadingFormat‑metod. Sant om raden upprepas som tabellrubrik på varje sida när tabellen sträcker sig över mer än en sida i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


Sant om raden upprepas som tabellrubrik på varje sida när tabellen sträcker sig över mer än en sida.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Exempel



Visar hur man bygger en tabell med rader som upprepas på varje sida.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Alla rader som infogas medan flaggan "HeadingFormat" är satt till "true"
// kommer att visas högst upp i tabellen på varje sida som den sträcker sig över.
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

// Lägg till tillräckligt många rader så att tabellen sträcker sig över två sidor.
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

## Se även

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
