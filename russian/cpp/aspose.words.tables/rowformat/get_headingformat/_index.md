---
title: "Aspose::Words::Tables::RowFormat::get_HeadingFormat метод"
linktitle: "get_HeadingFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::RowFormat::get_HeadingFormat метод. Истинно, если строка повторяется как заголовок таблицы на каждой странице, когда таблица занимает более одной страницы в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


Истина, если строка повторяется в качестве заголовка таблицы на каждой странице, когда таблица занимает более одной страницы.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Примеры



Показывает, как создать таблицу со строками, повторяющимися на каждой странице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Любые строки, вставленные, пока флаг "HeadingFormat" установлен в "true"
// будут отображаться в верхней части таблицы на каждой странице, которую она занимает.
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

// Добавьте достаточно строк, чтобы таблица занимала две страницы.
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

## См. также

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
