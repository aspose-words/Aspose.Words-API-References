---
title: "Aspose::Words::Tables::RowFormat::get_HeadingFormat 方法"
linktitle: "get_HeadingFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::RowFormat::get_HeadingFormat 方法。如果表格跨越多页时，该行在每页上都作为表头重复，则返回 true（在 C++ 中）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


如果表格跨越多页时，行在每页上作为表格标题重复，则为 True。

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## 示例



展示如何构建在每页都重复行的表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// 在 "HeadingFormat" 标志设置为 "true" 时插入的任何行
// 将在其跨越的每页表格顶部显示。
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

// 添加足够的行，使表格跨越两页。
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

## 另见

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
