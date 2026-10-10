---
title: "Aspose::Words::HeaderFooterCollection 类"
linktitle: "HeaderFooterCollection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::HeaderFooterCollection 类。提供对 Section 的 HeaderFooter 节点的类型化访问。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


提供对 [HeaderFooter](../headerfooter/) 节点的类型化访问，属于 [Section](../section/)。要了解更多，请访问 [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/) 文档文章。

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 在集合的末尾添加一个节点。 |
| [Clear](../nodecollection/clear/)() | 从此集合和文档中移除所有节点。 |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 确定节点是否在集合中。 |
| [get_Count](../nodecollection/get_count/)() | 获取集合中节点的数量。 |
| [GetEnumerator](../nodecollection/getenumerator/)() override | 提供对节点集合的简单 "foreach" 样式迭代。 |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | 在给定索引处检索一个 [HeaderFooter](../headerfooter/)。 |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | 检索指定类型的 [HeaderFooter](../headerfooter/)。 |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定节点的从零开始的索引。 |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | 在指定索引处向集合插入一个节点。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | 将所有页眉和页脚链接或取消链接到前一节中对应的页眉和页脚。 |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | 将指定的页眉或页脚链接或取消链接到前一节中对应的页眉或页脚。 |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 从集合和文档中移除该节点。 |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | 从集合和文档中移除指定索引处的节点。 |
| [ToArray](./toarray/)() | 将集合中所有 **HeaderFooter**s 复制到新的 **HeaderFooter**s 数组中。 |
| static [Type](./type/)() |  |
## 备注


每个 [HeaderFooter](../headerfooter/) 最多只能有一个。

每个 [Section](../section/) 中每种 [HeaderFooterType](../headerfootertype/) 最多只能有一个。

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

## 示例



展示如何创建页眉和页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 创建一个页眉并向其追加一个段落。该段落中的文本
// 将出现在此节每页的顶部，位于正文文本之上。
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// 创建一个页脚并向其追加一个段落。该段落中的文本
// 将出现在此节每页的底部，位于正文文本之下。
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


展示如何从文档中删除所有页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// 遍历每个节并删除所有类型的页脚。
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // 有三种页眉和页脚类型。
    // 1 -  "First"页眉/页脚，仅在章节的首页出现。
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  "Primary"页眉/页脚，出现在奇数页。
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  "Even"页眉/页脚，出现在偶数页。
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```

## 另见

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
