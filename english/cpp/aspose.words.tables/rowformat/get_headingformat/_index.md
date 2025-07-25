---
title: Aspose::Words::Tables::RowFormat::get_HeadingFormat method
linktitle: get_HeadingFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::RowFormat::get_HeadingFormat method. True if the row is repeated as a table heading on every page when the table spans more than one page in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


True if the row is repeated as a table heading on every page when the table spans more than one page.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Examples



Shows how to build a table with rows that repeat on every page. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Any rows inserted while the "HeadingFormat" flag is set to "true"
// will show up at the top of the table on every page that it spans.
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

// Add enough rows for the table to span two pages.
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

## See Also

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
