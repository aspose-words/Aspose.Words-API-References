---
title: Aspose::Words::Layout::LayoutCollector::GetEntity method
linktitle: GetEntity
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutCollector::GetEntity method. Returns an opaque position of the LayoutEnumerator which corresponds to the specified node. You can use returned value as an argument to Current given the document being enumerated and the document of the node are the same in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector::GetEntity method


Returns an opaque position of the [LayoutEnumerator](../../layoutenumerator/) which corresponds to the specified node. You can use returned value as an argument to [Current](../../layoutenumerator/get_current/) given the document being enumerated and the document of the node are the same.

```cpp
System::SharedPtr<System::Object> Aspose::Words::Layout::LayoutCollector::GetEntity(const System::SharedPtr<Aspose::Words::Node> &node)
```

## Remarks


This method works for only [Paragraph](../../../aspose.words/paragraph/) nodes, as well as indivisible inline nodes, e.g. [BookmarkStart](../../../aspose.words/bookmarkstart/) or [Shape](../../../aspose.words.drawing/shape/). It doesn't work for [Run](../../../aspose.words/run/), [Cell](../../../aspose.words.tables/cell/)[Row](../../../aspose.words.tables/row/) or [Table](../../../aspose.words.tables/table/) nodes, and nodes within header/footer.

Note that the entity returned for a [Paragraph](../../../aspose.words/paragraph/) node is a paragraph break span. Use the appropriate method to ascend to the parent line

If you need to navigate to a [Run](../../../aspose.words/run/) of text then you can insert bookmark right before it and then navigate to the bookmark instead.

If you need to navigate to a [Cell](../../../aspose.words.tables/cell/) node then you can move to a [Paragraph](../../../aspose.words/paragraph/) node in this cell and then ascend to a parent entity. The same approach can be used for [Row](../../../aspose.words.tables/row/) and [Table](../../../aspose.words.tables/table/) nodes.

## Examples



Shows how to see the the ranges of pages that a node spans. 
```cpp
auto doc = MakeObject<Document>();
auto layoutCollector = MakeObject<LayoutCollector>(doc);

// Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
// Since the document is empty, that number of pages is currently zero.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Populate the document with 5 pages of content.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(BreakType::PageBreak);
builder->InsertBreak(BreakType::PageBreak);
builder->InsertBreak(BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(BreakType::PageBreak);
builder->InsertBreak(BreakType::PageBreak);

// Before the layout collector, we need to call the "UpdatePageLayout" method to give us
// an accurate figure for any layout-related metric, such as the page count.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// We can see the numbers of the start and end pages of any node and their overall page spans.
SharedPtr<NodeCollection> nodes = doc->GetChildNodes(NodeType::Any, true);
for (const auto& node : System::IterateOver(nodes))
{
    std::cout << String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node),
                                 layoutCollector->GetEndPageIndex(node)) +
                  String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node)))
              << std::endl;
}

// We can iterate over the layout entities using a LayoutEnumerator.
auto layoutEnumerator = MakeObject<LayoutEnumerator>(doc);

ASSERT_EQ(LayoutEntityType::Page, layoutEnumerator->get_Type());

// The LayoutEnumerator can traverse the collection of layout entities like a tree.
// We can also apply it to any node's corresponding layout entity.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(NodeType::Paragraph, 1, true)));

ASSERT_EQ(LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## See Also

* Class [Node](../../../aspose.words/node/)
* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
