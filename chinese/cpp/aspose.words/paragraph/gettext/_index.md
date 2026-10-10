---
title: "Aspose::Words::Paragraph::GetText 方法"
linktitle: "GetText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::GetText 方法。获取此段落的文本，包括段落结束字符（C++）。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


获取此段落的文本，包括段落结束字符。

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## 备注


所有子节点的文本会被连接，并在其后附加段落结束字符，如下所示：

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



返回的字符串包含所有控制字符和特殊字符，如 [ControlChar](../../controlchar/) 中所述。

## 示例



展示如何在 [CompositeNode](../../compositenode/) 的子节点集合中添加、更新和删除子节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 默认情况下，空文档只有一个段落。
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// 复合节点（例如我们的段落）可以包含其他复合节点和内联节点作为子节点。
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// 创建另外三个运行节点。
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// 文档主体在我们将这些运行插入到复合节点之前不会显示它们
// 该复合节点本身是文档节点树的一部分，就像我们对第一个运行所做的那样。
// 我们可以确定插入的节点的文本内容位于何处
// 通过相对于段落中另一个节点指定插入位置，来决定它在文档中的出现位置。
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// 将第二个运行插入到段落中，位于初始运行之前。
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// 在初始运行之后插入第三个运行。
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// 将第一个运行插入到段落子节点集合的开头。
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 我们可以通过编辑和删除现有子节点来修改运行的内容。
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## 另见

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
