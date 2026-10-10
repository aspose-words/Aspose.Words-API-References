---
title: "Aspose::Words::TabStop::get_Leader 方法"
linktitle: "get_Leader"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStop::get_Leader 方法。获取或设置在 C++ 中制表符下显示的前导线类型。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/tabstop/get_leader/
---
## TabStop::get_Leader method


获取或设置制表符下方显示的前导线类型。

```cpp
Aspose::Words::TabLeader Aspose::Words::TabStop::get_Leader() const
```


## 示例



展示如何修改目录相关段落中右侧制表位的位置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table of contents.docx");

// 遍历所有使用基于目录结果的样式的段落；这些样式介于 TOC 和 TOC9 之间。
for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)))
{
    if (para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() >= Aspose::Words::StyleIdentifier::Toc1 && para->get_ParagraphFormat()->get_Style()->get_StyleIdentifier() <= Aspose::Words::StyleIdentifier::Toc9)
    {
        // 获取此段落使用的第一个制表位，它应当用于对齐页码。
        System::SharedPtr<Aspose::Words::TabStop> tab = para->get_ParagraphFormat()->get_TabStops()->idx_get(0);

        // 将第一个默认制表位替换为自定义制表位。
        para->get_ParagraphFormat()->get_TabStops()->RemoveByPosition(tab->get_Position());
        para->get_ParagraphFormat()->get_TabStops()->Add(tab->get_Position() - 50, tab->get_Alignment(), tab->get_Leader());
    }
}

doc->Save(get_ArtifactsDir() + u"Styles.ChangeTocsTabStops.docx");
```

## 另见

* Enum [TabLeader](../../tableader/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
