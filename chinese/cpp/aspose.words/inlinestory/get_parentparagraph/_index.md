---
title: "Aspose::Words::InlineStory::get_ParentParagraph 方法"
linktitle: "get_ParentParagraph"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::InlineStory::get_ParentParagraph 方法。检索此节点在 C++ 中的父段落。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/inlinestory/get_parentparagraph/
---
## InlineStory::get_ParentParagraph method


检索此节点的父 [Paragraph](../../paragraph/)。

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::InlineStory::get_ParentParagraph()
```


## 示例



展示如何插入 [InlineStory](../) 节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// 表格节点具有 "EnsureMinimum()" 方法，确保表格至少有一个单元格。
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// 我们可以在脚注中放置表格，这将使其出现在引用页面的页脚。
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// InlineStory 也有一个 "EnsureMinimum()" 方法，但在这种情况下，
// 它确保节点的最后一个子节点是段落，
// 以便我们能够在 Microsoft Word 中轻松点击并输入文本。
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// 编辑锚点的外观，即小的上标数字
// 在指向脚注的正文中。
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// 所有内联故事节点都有各自的故事类型。
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// 注释是另一种内联故事类型。
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// 内联故事节点的父段落将是来自主文档正文的段落。
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// 然而，最后一个段落是来自注释文本内容的段落，
// 它将以气泡的形式位于主文档正文之外。
// 默认情况下，注释不会有任何子节点，
// 因此我们可以使用 EnsureMinimum() 方法在此处同样放置一个段落。
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// 一旦我们有了段落，就可以移动构建器来执行此操作并编写我们的注释。
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## 另见

* Class [Paragraph](../../paragraph/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
