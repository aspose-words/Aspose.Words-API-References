---
title: "Aspose::Words::Tables::Cell::get_Paragraphs 方法"
linktitle: "get_Paragraphs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Cell::get_Paragraphs 方法。获取单元格的直接子段落集合（C++）。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.tables/cell/get_paragraphs/
---
## Cell::get_Paragraphs method


获取作为单元格直接子项的段落集合。

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::Tables::Cell::get_Paragraphs()
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

* Class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
