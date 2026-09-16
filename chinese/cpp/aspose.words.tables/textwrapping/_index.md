---
title: "Aspose::Words::Tables::TextWrapping 枚举"
linktitle: "TextWrapping"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::TextWrapping 枚举。指定在 C++ 中文本如何环绕表格。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


指定文本如何环绕表格换行。

```cpp
enum class TextWrapping
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 文本和表格按照它们在文档中出现的顺序显示。 |
| Around | 1 | 文本环绕表格，占用可用的侧边空间。 |
| Default | n/a | 默认值。 |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
