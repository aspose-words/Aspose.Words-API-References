---
title: Aspose::Words::Layout::LayoutCollector class
linktitle: LayoutCollector
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutCollector class. This class allows to compute page numbers of document nodes. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.layout/layoutcollector/
---
## LayoutCollector class


This class allows to compute page numbers of document nodes. To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) documentation article.

```cpp
class LayoutCollector : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt. |
| [get_Document](./get_document/)() const | Gets or sets the document this collector instance is attached to. |
| [GetEndPageIndex](./getendpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets 1-based index of the page where node ends. Returns 0 if node cannot be mapped to a page. |
| [GetEntity](./getentity/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns an opaque position of the [LayoutEnumerator](../layoutenumerator/) which corresponds to the specified node. You can use returned value as an argument to [Current](../layoutenumerator/get_current/) given the document being enumerated and the document of the node are the same. |
| [GetNumPagesSpanned](./getnumpagesspanned/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets number of pages the specified node spans. 0 if node is within a single page. This is the same as [GetEndPageIndex()](../) - [GetStartPageIndex()](../). |
| [GetStartPageIndex](./getstartpageindex/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets 1-based index of the page where node begins. Returns 0 if node cannot be mapped to a page. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutCollector](./layoutcollector/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initializes an instance of this class. |
| [set_Document](./set_document/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Setter for [Aspose::Words::Layout::LayoutCollector::get_Document](./get_document/). |
| static [Type](./type/)() |  |
## Remarks


When you create a [LayoutCollector](./) and specify a [Document](../../aspose.words/document/) document object to attach to, the collector will record mapping of document nodes to layout objects when the document is formatted into pages.

You will be able to find out on which page a particular document node (e.g. run, paragraph or table cell) is located by using the [GetStartPageIndex()](../), [GetEndPageIndex()](../) and [GetNumPagesSpanned()](../) methods. These methods automatically build page layout model of the document and update fields if required.

When you no longer need to collect layout information, it is best to set the [Document](./get_document/) property to **null** to avoid unnecessary collection of more layout mappings.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
