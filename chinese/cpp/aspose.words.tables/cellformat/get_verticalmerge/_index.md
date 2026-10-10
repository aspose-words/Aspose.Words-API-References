---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge 方法"
linktitle: "get_VerticalMerge"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge 方法。指定单元格在 C++ 中如何垂直与其他单元格合并。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


指定单元格如何垂直合并到其他单元格。

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## 备注


只有当单元格的左边界和右边界相同，才能进行垂直合并。

当单元格垂直合并时，合并单元格的显示区域会被合并。合并后的区域用于显示第一个垂直合并单元格的内容，所有其他垂直合并的单元格必须为空。

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

## 另见

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
