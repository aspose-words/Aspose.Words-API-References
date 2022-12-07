---
title: GetText
second_title: Aspose.Words for C++ API Reference
description: Gets the text of this paragraph including the end of paragraph character.
type: docs
weight: 339
url: /cpp/aspose.words/paragraph/gettext/
---
## Paragraph::GetText method


Gets the text of this paragraph including the end of paragraph character.

```cpp
System::String Aspose::Words::Paragraph::GetText() override
```

## Remarks


The text of all child nodes is concatenated and the end of paragraph character is appended as follows:

* If the paragraph is the last paragraph of [Body](../../body/), then [SectionBreak](../../controlchar/sectionbreak/) (\x000c) is appended.
* If the paragraph is the last paragraph of [Cell](../../../aspose.words.tables/cell/), then [Cell](../../controlchar/cell/) (\x0007) is appended.
* For all other paragraphs [ParagraphBreak](../../controlchar/paragraphbreak/) (\r) is appended.



The returned string includes all control and special characters as described in [ControlChar](../../controlchar/).

## Examples



Shows how to add, update and delete child nodes in a [CompositeNode](../../compositenode/)'s collection of children. 
```cpp
auto doc = MakeObject<Document>();

// An empty document, by default, has one paragraph.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
SharedPtr<Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = MakeObject<Run>(doc, u"Initial text. ");
paragraph->AppendChild(paragraphText);

// Create three more run nodes.
auto run1 = MakeObject<Run>(doc, u"Run 1. ");
auto run2 = MakeObject<Run>(doc, u"Run 2. ");
auto run3 = MakeObject<Run>(doc, u"Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Insert the second run into the paragraph in front of the initial run.
paragraph->InsertBefore(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Insert the third run after the initial run.
paragraph->InsertAfter(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph->PrependChild(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(NodeType::Any, true)->get_Count());

// We can modify the contents of the run by editing and deleting existing child nodes.
(System::DynamicCast<Run>(paragraph->GetChildNodes(NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(NodeType::Any, true)->get_Count());
```

## See Also

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
