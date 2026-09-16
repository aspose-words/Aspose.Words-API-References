---
title: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance method"
linktitle: "get_AbsoluteVerticalDistance"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance 方法。获取或设置由表属性指定的绝对垂直浮动表位置，单位为点。默认值在 C++ 中为 0。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.tables/table/get_absoluteverticaldistance/
---
## Table::get_AbsoluteVerticalDistance method


获取或设置由表格属性指定的绝对垂直浮动表格位置，单位为点。默认值为 0。

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
