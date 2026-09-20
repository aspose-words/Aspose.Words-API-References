---
title: "Aspose::Words::Tables::Table::get_TextWrapping method"
linktitle: "get_TextWrapping"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::get_TextWrapping 方法。获取或设置 C++ 中表格的 TextWrapping。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


获取或设置表格的 [TextWrapping](./)。

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## 示例



展示如何使用表格文本环绕。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// 将 "TextWrapping" 属性设置为 "TextWrapping.Around" 以使表格环绕文本,
// 并通过设置位置将其向下推到下面的段落中。
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## 另见

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
