---
title: "Aspose::Words::Tables::CellFormat::SetPaddings 方法"
linktitle: "SetPaddings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellFormat::SetPaddings 方法。设置在单元格内容的左/上/右/下添加的空间量（以点为单位）（C++）。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


设置要在单元格内容的左/上/右/下添加的空间量（以点为单位）。

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## 示例



展示如何使用空白为单元格内容添加填充。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 设置边框与文本内容之间的填充距离（以点为单位）
// 对我们使用文档生成器创建的每个表格单元格而言。
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// 创建一个包含单元格的表格，该单元格的内容将具有空白填充。
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## 另见

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
