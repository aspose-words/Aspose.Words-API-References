---
title: "Aspose::Words::Tables::Table::get_PreferredWidth 方法"
linktitle: "get_PreferredWidth"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_PreferredWidth 方法。获取或设置表格的首选宽度（C++）。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


获取或设置表格的首选宽度。

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## 备注


默认值是 [Auto](../../preferredwidth/auto/)。

## 示例



展示如何将表格自动适配为页面宽度的 50%。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## 另见

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
