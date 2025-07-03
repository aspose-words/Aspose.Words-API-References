---
title: Aspose::Words::Layout::LayoutCollector::Clear method
linktitle: Clear
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutCollector::Clear method. Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.layout/layoutcollector/clear/
---
## LayoutCollector::Clear method


Clears all collected layout data. Call this method after document was manually updated, or layout was rebuilt.

```cpp
void Aspose::Words::Layout::LayoutCollector::Clear()
```


## Examples



Shows how to see the the ranges of pages that a node spans. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);

// Call the "GetNumPagesSpanned" method to count how many pages the content of our document spans.
// Since the document is empty, that number of pages is currently zero.
ASPOSE_ASSERT_EQ(doc, layoutCollector->get_Document());
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

// Populate the document with 5 pages of content.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->Write(u"Section 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Before the layout collector, we need to call the "UpdatePageLayout" method to give us
// an accurate figure for any layout-related metric, such as the page count.
ASSERT_EQ(0, layoutCollector->GetNumPagesSpanned(doc));

layoutCollector->Clear();
doc->UpdatePageLayout();

ASSERT_EQ(5, layoutCollector->GetNumPagesSpanned(doc));

// We can see the numbers of the start and end pages of any node and their overall page spans.
System::SharedPtr<Aspose::Words::NodeCollection> nodes = doc->GetChildNodes(Aspose::Words::NodeType::Any, true);
for (auto&& node : System::IterateOver(nodes))
{
    std::cout << System::String::Format(u"->  NodeType.{0}: ", node->get_NodeType()) << std::endl;
    std::cout << (System::String::Format(u"\tStarts on page {0}, ends on page {1},", layoutCollector->GetStartPageIndex(node), layoutCollector->GetEndPageIndex(node)) + System::String::Format(u" spanning {0} pages.", layoutCollector->GetNumPagesSpanned(node))) << std::endl;
}

// We can iterate over the layout entities using a LayoutEnumerator.
auto layoutEnumerator = System::MakeObject<Aspose::Words::Layout::LayoutEnumerator>(doc);

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Page, layoutEnumerator->get_Type());

// The LayoutEnumerator can traverse the collection of layout entities like a tree.
// We can also apply it to any node's corresponding layout entity.
layoutEnumerator->set_Current(layoutCollector->GetEntity(doc->GetChild(Aspose::Words::NodeType::Paragraph, 1, true)));

ASSERT_EQ(Aspose::Words::Layout::LayoutEntityType::Span, layoutEnumerator->get_Type());
ASSERT_EQ(u"¶", layoutEnumerator->get_Text());
```

## See Also

* Class [LayoutCollector](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
