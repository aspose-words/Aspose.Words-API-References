---
title: "Aspose::Words::Tables::Table::get_StyleIdentifier 方法"
linktitle: "get_StyleIdentifier"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_StyleIdentifier 方法。获取或设置在 C++ 中应用于此表的表样式的与区域无关的样式标识符。"
type: docs
weight: 35000
url: /zh/cpp/aspose.words.tables/table/get_styleidentifier/
---
## Table::get_StyleIdentifier method


获取或设置应用于此表格的表格样式的区域无关样式标识符。

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Tables::Table::get_StyleIdentifier()
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

* Enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
