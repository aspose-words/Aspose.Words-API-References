---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore 方法"
linktitle: "get_PageBreakBefore"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore 方法。如果在 C++ 中强制在段落前插入分页，则返回 true。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


如果在段落前强制换页，则为 True。

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## 示例



展示如何在段落开头创建带分页的段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将此标志设置为 "true" 以在每个段落的开头应用分页
// 文档生成器将在此 ParagraphFormat 配置下创建的段落。
// 第一个段落不会收到分页。
// 将此标志保持为 "false" 以在同一页上开始每个新段落
// 与前一个段落一样，只要有足够的空间。
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## 另见

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
