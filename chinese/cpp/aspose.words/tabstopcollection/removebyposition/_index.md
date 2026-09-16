---
title: "Aspose::Words::TabStopCollection::RemoveByPosition 方法"
linktitle: "RemoveByPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStopCollection::RemoveByPosition 方法。移除集合中指定位置的制表位（C++）。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection::RemoveByPosition method


从集合中移除指定位置的制表位。

```cpp
void Aspose::Words::TabStopCollection::RemoveByPosition(double position)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 位置 | double | 要移除的制表位的位置（以点为单位）。 |

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

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
