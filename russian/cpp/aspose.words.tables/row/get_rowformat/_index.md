---
title: "Aspose::Words::Tables::Row::get_RowFormat метод"
linktitle: "get_RowFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Row::get_RowFormat метод. Предоставляет доступ к свойствам форматирования строки в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.tables/row/get_rowformat/
---
## Row::get_RowFormat method


Предоставляет доступ к свойствам форматирования строки.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowFormat> Aspose::Words::Tables::Row::get_RowFormat()
```


## Примеры



Показывает, как изменить формат строк и ячеек в таблице.
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

// Используйте свойство "RowFormat" первой строки, чтобы изменить форматирование
// содержимого всех ячеек в этой строке.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Используйте свойство "CellFormat" первой ячейки в последней строке, чтобы изменить форматирование содержимого этой ячейки.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Показывает, как изменить форматирование строки таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Используйте свойство "RowFormat" первой строки, чтобы задать форматирование, изменяющее внешний вид всей строки.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## См. также

* Class [RowFormat](../../rowformat/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
