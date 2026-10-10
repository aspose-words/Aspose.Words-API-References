---
title: "Aspose::Words::Tables::Cell::get_FirstParagraph 方法"
linktitle: "get_FirstParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Cell::get_FirstParagraph 方法。获取 C++ 中直接子节点中的第一个段落。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


获取直接子项中的第一个段落。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## 示例



展示如何使用文档生成器创建嵌套表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 构建外部表格。
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// 移动到外部表格的第一个单元格，然后在该单元格内构建另一个表格。
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## 另见

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
