---
title: Aspose::Words::CompositeNode::get_Count method
linktitle: get_Count
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::get_Count method. Gets the number of immediate children of this node in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/compositenode/get_count/
---
## CompositeNode::get_Count method


Gets the number of immediate children of this node.

```cpp
int32_t Aspose::Words::CompositeNode::get_Count()
```


## Examples



Shows how to add, update and delete child nodes in a [CompositeNode](../)'s collection of children. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// An empty document, by default, has one paragraph.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Create three more run nodes.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Insert the second run into the paragraph in front of the initial run.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Insert the third run after the initial run.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// We can modify the contents of the run by editing and deleting existing child nodes.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## See Also

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
