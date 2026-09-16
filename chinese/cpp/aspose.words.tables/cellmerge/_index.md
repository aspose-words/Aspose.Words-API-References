---
title: "Aspose::Words::Tables::CellMerge 枚举"
linktitle: "CellMerge"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellMerge 枚举。指定表格中的单元格在 C++ 中如何与其他单元格合并。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


指定表格中的单元格如何与其他单元格合并。

```cpp
enum class CellMerge
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 该单元格未合并。 |
| First | 1 | 该单元格是合并单元格范围中的第一个单元格。 |
| Previous | 2 | 该单元格已水平或垂直合并到前一个单元格。 |


## 示例



展示如何垂直合并表格单元格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在第一行的第一列插入一个单元格。
// 此单元格将成为垂直合并单元格范围中的第一个。
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// 在第一行的第二列插入一个单元格，然后结束该行。
// 此外，配置构建器以在创建的单元格中禁用垂直合并。
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// 在第二行的第一列插入一个单元格。
// 我们将不添加文本内容，而是将此单元格与直接上方添加的第一个单元格合并。
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// 在第二行的第二列插入另一个独立的单元格。
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
