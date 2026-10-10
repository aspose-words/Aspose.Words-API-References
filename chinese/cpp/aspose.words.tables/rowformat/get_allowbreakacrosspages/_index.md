---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages 方法"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages 方法。如果表格行中的文本允许在分页符处拆分，则返回 true（在 C++ 中）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


如果允许表格行中的文本在分页符处拆分，则为 True。

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## 示例



展示如何为表格中的每一行禁用跨页断行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 将 "AllowBreakAcrossPages" 属性设置为 "false" 以保持该行
// 在表格跨越两页时保持完整，不在该行处断开。
// 如果该行太大而无法容纳在一页中，Microsoft Word 会将其推到下一页。
// 将 "AllowBreakAcrossPages" 属性设置为 "true" 以允许该行在两页之间断开。
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## 另见

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
