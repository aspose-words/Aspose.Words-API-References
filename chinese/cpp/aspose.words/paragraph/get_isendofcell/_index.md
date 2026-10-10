---
title: "Aspose::Words::Paragraph::get_IsEndOfCell 方法"
linktitle: "get_IsEndOfCell"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_IsEndOfCell 方法。若此段落是单元格中的最后一个段落则为 true；否则为 false（在 C++ 中）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/paragraph/get_isendofcell/
---
## Paragraph::get_IsEndOfCell method


如果此段落是 [Cell](../../../aspose.words.tables/cell/) 中的最后一个段落，则为 true；否则为 false。

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfCell()
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
