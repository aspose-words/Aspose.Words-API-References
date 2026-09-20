---
title: "Aspose::Words::Tables::Table::get_AllowAutoFit 方法"
linktitle: "get_AllowAutoFit"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_AllowAutoFit 方法。允许 Microsoft Word 和 Aspose.Words 在 C++ 中自动调整表格单元格大小以适应其内容。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


允许 Microsoft Word 和 Aspose.Words 自动调整表格中单元格的大小以适应其内容。

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## 备注


默认值为 **true**。

## 示例



展示如何启用/禁用自动表格单元格大小调整。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// 将 "AllowAutoFit" 属性设置为 "false"，使表格保持原有尺寸。
// 对所有行和单元格进行处理，如果内容过大而无法容纳，则截断内容。
// 将 "AllowAutoFit" 属性设置为 "true"，以允许表格更改单元格的宽度和高度。
// 以容纳其内容。
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
