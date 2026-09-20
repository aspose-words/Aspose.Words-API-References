---
title: "Aspose::Words::Tables::Table::get_StyleOptions 方法"
linktitle: "get_StyleOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_StyleOptions 方法。获取或设置位标志，以指定在 C++ 中如何将表格样式应用于此表。"
type: docs
weight: 37000
url: /zh/cpp/aspose.words.tables/table/get_styleoptions/
---
## Table::get_StyleOptions method


获取或设置指定表格样式如何应用于此表格的位标志。

```cpp
Aspose::Words::Tables::TableStyleOptions Aspose::Words::Tables::Table::get_StyleOptions()
```


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

* Enum [TableStyleOptions](../../tablestyleoptions/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
