---
title: "Aspose::Words::Tables::CellFormat::ClearFormatting 方法"
linktitle: "ClearFormatting"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::CellFormat::ClearFormatting 方法。将单元格格式重置为默认。不会更改 C++ 中单元格的宽度。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat::ClearFormatting method


重置为默认单元格格式。不会更改单元格的宽度。

```cpp
void Aspose::Words::Tables::CellFormat::ClearFormatting()
```


## 示例



展示如何将两个表的行合并为一个。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// 下面是从文档中获取表的两种方法。
// 1 -  来自 Body 节点的 "Tables" 集合：
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 - 使用 "GetChild" 方法：
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// 将当前表格的所有行追加到下一个表格。
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// 移除空的表格容器。
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## 另见

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
