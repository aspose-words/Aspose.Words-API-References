---
title: "Aspose::Words::TabStop::GetType 方法"
linktitle: "get_Alignment"
second_title: "Aspose.Words for C++ API 参考"
description: "如何在 C++ 中使用 Aspose::Words::TabStop 类的 GetType 方法。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/tabstop/get_alignment/
---
## TabStop::get_Alignment method


获取或设置此制表位处文本的对齐方式。

```cpp
Aspose::Words::TabAlignment Aspose::Words::TabStop::get_Alignment() const
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

* Enum [TabAlignment](../../tabalignment/)
* Class [TabStop](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
