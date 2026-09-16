---
title: "Aspose::Words::Paragraph::get_IsInCell 方法"
linktitle: "get_IsInCell"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_IsInCell 方法。如果此段落是 Cell 的直接子项，则返回 true；否则在 C++ 中返回 false。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/paragraph/get_isincell/
---
## Paragraph::get_IsInCell method


如果此段落是 [Cell](../../../aspose.words.tables/cell/) 的直接子项，则返回 true；否则返回 false。

```cpp
bool Aspose::Words::Paragraph::get_IsInCell()
```


## 示例



展示如何设置表格在同一页上保持在一起。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 为表格中的每个段落启用 KeepWithNext，除了
// 最后一行的最后几个段落将防止表格跨多页拆分。
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(Aspose::Words::NodeType::Cell, true)))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(get_ArtifactsDir() + u"Table.KeepTableTogether.docx");
```

## 另见

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
