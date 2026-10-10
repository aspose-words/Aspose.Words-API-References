---
title: "Aspose::Words::TabStop 类"
linktitle: "TabStop"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TabStop 类。表示单个自定义制表位。TabStop 对象是 TabStopCollection 集合的成员。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 68000
url: /zh/cpp/aspose.words/tabstop/
---
## TabStop class


表示单个自定义制表位。 [TabStop](./) 对象是 [TabStopCollection](../tabstopcollection/) 集合的成员。欲了解更多，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class TabStop : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | 与指定的 [TabStop](./) 进行比较。 |
| [get_Alignment](./get_alignment/)() const | 获取或设置此制表位处文本的对齐方式。 |
| [get_IsClear](./get_isclear/)() | 如果此制表位在该位置清除任何已有的制表位，则返回 **true**。 |
| [get_Leader](./get_leader/)() const | 获取或设置制表符下方显示的前导线类型。 |
| [get_Position](./get_position/)() | 获取制表位的点数位置。 |
| [GetHashCode](./gethashcode/)() const override | 计算此对象的哈希码。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::TabAlignment) | [Aspose::Words::TabStop::get_Alignment](./get_alignment/) 的设置器。 |
| [set_Leader](./set_leader/)(Aspose::Words::TabLeader) | [Aspose::Words::TabStop::get_Leader](./get_leader/) 的设置器。 |
| [TabStop](./tabstop/)(double) | 初始化此类的新实例。 |
| [TabStop](./tabstop/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | 初始化此类的新实例。 |
| static [Type](./type/)() |  |
## 备注


通常，制表位指定制表位存在的位置。但由于制表位可以从父样式继承，子对象可能需要显式定义在给定位置没有制表位。要清除给定位置继承的制表位，请创建一个 [TabStop](./) 对象并将 [Alignment](./get_alignment/) 设置为 [Clear](../tabalignment/)。

欲了解更多信息，请参阅 [TabStopCollection](../tabstopcollection/)。

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
