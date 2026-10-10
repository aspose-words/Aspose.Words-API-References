---
title: "Aspose::Words::Tables::Table::get_TopPadding method"
linktitle: "get_TopPadding"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_TopPadding 方法。获取或设置在 C++ 中向单元格内容上方添加的空间量（以点为单位）。"
type: docs
weight: 40000
url: /zh/cpp/aspose.words.tables/table/get_toppadding/
---
## Table::get_TopPadding method


获取或设置要在单元格内容上方添加的空间量（以点为单位）。

```cpp
double Aspose::Words::Tables::Table::get_TopPadding()
```


## 示例



展示如何在表格中配置内容填充。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// 对于表格中的每个单元格，设置其内容与各边框之间的距离。
// 此表格将在换行文本时保持最小填充距离。
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
