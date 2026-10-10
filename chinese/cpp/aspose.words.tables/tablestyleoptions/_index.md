---
title: "Aspose::Words::Tables::TableStyleOptions 枚举"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::TableStyleOptions 枚举。指定在 C++ 中如何将表格样式应用于表格。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


指定表格样式如何应用于表格。

```cpp
enum class TableStyleOptions
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 未应用任何表格样式格式。 |
| FirstRow | 32 | 应用首行条件格式。 |
| LastRow | 64 | 应用末行条件格式。 |
| FirstColumn | 128 | 应用第一列条件格式。 |
| LastColumn | 256 | 应用末列条件格式。 |
| RowBands | 512 | 应用行分带条件格式。 |
| ColumnBands | 1024 | 应用列分带条件格式。 |
| Default2003 | n/a | [Row](../row/) 和列分带已应用。这是 Microsoft Word 对旧格式（如 DOC、WML 和 RTF）的默认设置。 |
| Default | n/a | 这是 Microsoft Word 的默认设置。 |


## 示例



展示如何在应用样式的同时构建新表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// 在设置任何表格格式之前，必须至少插入一行。
builder->InsertCell();

// 根据样式标识符设置使用的表格样式。
// 请注意，保存为 .doc 格式时并非所有表格样式都可用。
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// 基于谓词将样式部分应用于表格的特性，然后构建表格。
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## 另见

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
