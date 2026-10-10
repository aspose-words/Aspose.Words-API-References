---
title: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge 方法"
linktitle: "get_HorizontalMerge"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge 方法。指定单元格在 C++ 中如何在行内水平与其他单元格合并。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


指定单元格在行中如何水平合并到其他单元格。

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## 示例



展示如何水平合并表格单元格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在第一行的第一列插入一个单元格。
// 此单元格将成为水平合并单元格范围中的第一个。
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// 在第一行的第二列插入一个单元格。不是添加文本内容，
// 我们将把此单元格与直接在左侧添加的第一个单元格合并。
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// 在第二行插入另外两个未合并的单元格。
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## 另见

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
