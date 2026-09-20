---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing 方法"
linktitle: "get_AllowCellSpacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing 方法。获取或设置 C++ 中的 \"允许单元格之间的间距\" 选项。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


获取或设置 "Allow spacing between cells" 选项。

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## 示例



展示如何在表格中启用单元格之间的间距。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// 将 "AllowCellSpacing" 属性设置为 "true" 以启用单元格之间的间距
// 其大小等于 "CellSpacing" 属性的值，单位为点。
// 将 "AllowCellSpacing" 属性设置为 "false" 以禁用单元格间距
// 并忽略 "CellSpacing" 属性的值。
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// 调整 "CellSpacing" 属性将自动启用单元格间距。
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
