---
title: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment 方法"
linktitle: "get_RelativeHorizontalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment 方法。获取或设置 C++ 中浮动表的相对水平对齐方式。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words.tables/table/get_relativehorizontalalignment/
---
## Table::get_RelativeHorizontalAlignment method


获取或设置浮动表格的相对水平对齐方式。

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment()
```


## 示例



展示如何设置浮动表格的位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// 将表格的位置设置到页面上的某个位置，例如在本例中设置为右下角。
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// 我们还可以从插入表格的段落位置设置水平和垂直的点偏移量。
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## 另见

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
