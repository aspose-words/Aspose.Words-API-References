---
title: "Aspose::Words::Tables::Table::AutoFit method"
linktitle: "自动适应"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::AutoFit 方法。根据 C++ 中指定的自动适应行为调整表格和单元格的大小。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


根据指定的自动适应行为调整表格和单元格的大小。

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| behavior | Aspose::Words::Tables::AutoFitBehavior | 指定表格的自动适应方式。 |
## 备注


此方法模拟 Microsoft Word 中表格的“自动适应”菜单中可用的命令。可用的命令包括 "Auto Fit to Contents"（自动适应内容）、"Auto Fit to Window"（自动适应窗口）和 "Fixed Column Width"（固定列宽）。在 Microsoft Word 中，这些命令会设置相关的表格属性，然后更新表格布局，Aspose.Words 为您执行相同的操作。

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

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
