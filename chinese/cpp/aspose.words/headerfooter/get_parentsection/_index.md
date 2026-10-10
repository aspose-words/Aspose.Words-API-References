---
title: "Aspose::Words::HeaderFooter::get_ParentSection 方法"
linktitle: "get_ParentSection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::HeaderFooter::get_ParentSection 方法。获取此故事在 C++ 中的父节。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/headerfooter/get_parentsection/
---
## HeaderFooter::get_ParentSection method


获取此故事的父节。

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::HeaderFooter::get_ParentSection()
```

## 备注


[ParentSection](./) is equivalent to [ParentNode](../../node/get_parentnode/) casted to [Section](../../section/).

## 示例



展示如何在节之间链接页眉和页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 3");

// 移动到第一节并创建页眉和页脚。默认情况下，
// 页眉和页脚仅会出现在包含它们的节的页面上。
builder->MoveToSection(0);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->Write(u"This is the header, which will be displayed in sections 1 and 2.");

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->Write(u"This is the footer, which will be displayed in sections 1, 2 and 3.");

// 我们可以将节的页眉/页脚链接到前一节的页眉/页脚
// 以便链接的节显示被链接节的页眉/页脚。
doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LinkToPrevious(true);

// 每个节仍然拥有自己的页眉/页脚对象。当我们链接节时，
// 链接的节将在保留自身的同时显示被链接节的页眉/页脚。
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0));
ASPOSE_ASSERT_NE(doc->get_Sections()->idx_get(0)->get_HeadersFooters()->idx_get(0)->get_ParentSection(), doc->get_Sections()->idx_get(1)->get_HeadersFooters()->idx_get(0)->get_ParentSection());

// 将第三节的页眉/页脚链接到第二节的页眉/页脚。
// 第二节已经链接到第一节的页眉/页脚，
// 因此链接到第二节将形成一个链接链。
// 第一、第二以及现在的第三节都将显示第一节的页眉。
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(true);

// 我们可以在调用 LinkToPrevious 方法时传入 "false" 来取消链接前一节的页眉/页脚。
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(false);

// 我们还可以使用此方法仅选择特定类型的页眉/页脚进行链接。
// 现在第三节将拥有与第二节和第一节相同的页脚，但不包括页眉。
doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LinkToPrevious(Aspose::Words::HeaderFooterType::FooterPrimary, true);

// 第一节的页眉/页脚无法自行链接到任何内容，因为没有前一节。
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->get_Count());
ASSERT_EQ(2, doc->get_Sections()->idx_get(0)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// 第二节的所有页眉/页脚都已链接到第一节的页眉/页脚。
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->get_Count());
ASSERT_EQ(6, doc->get_Sections()->idx_get(1)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return (System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));

// 在第三节中，只有页脚通过第二节链接到第一节的页脚。
ASSERT_EQ(6, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->get_Count());
ASSERT_EQ(5, doc->get_Sections()->idx_get(2)->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
{
    return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsLinkedToPrevious();
}))));
ASSERT_TRUE(doc->get_Sections()->idx_get(2)->get_HeadersFooters()->idx_get(3)->get_IsLinkedToPrevious());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Link.docx");
```

## 另见

* Class [Section](../../section/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
