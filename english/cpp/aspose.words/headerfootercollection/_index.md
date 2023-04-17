---
title: Aspose::Words::HeaderFooterCollection class
linktitle: HeaderFooterCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeaderFooterCollection class. Provides typed access to HeaderFooter nodes of a Section. To learn more, visit the  documentation article in C++.'
type: docs
weight: 32000
url: /cpp/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class


Provides typed access to [HeaderFooter](../headerfooter/) nodes of a [Section](../section/). To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/) documentation article.

```cpp
class HeaderFooterCollection : public Aspose::Words::NodeCollection
```

## Methods

| Method | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](../nodecollection/clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](../nodecollection/get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a [HeaderFooter](../headerfooter/) at the given index. |
| [idx_get](./idx_get/)(Aspose::Words::HeaderFooterType) | Retrieves a [HeaderFooter](../headerfooter/) of the specified type. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LinkToPrevious](./linktoprevious/)(bool) | Links or unlinks all headers and footers to the corresponding headers and footers in the previous section. |
| [LinkToPrevious](./linktoprevious/)(Aspose::Words::HeaderFooterType, bool) | Links or unlinks the specified header or footer to the corresponding header or footer in the previous section. |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all **HeaderFoorter**s from the collection to a new array of **HeaderFoorter**s. |
| static [Type](./type/)() |  |
## Remarks


There can be maximum of one [HeaderFooter](../headerfooter/)

of each [HeaderFooterType](../headerfootertype/) per [Section](../section/).

[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.

## Examples



Shows how to create a header and a footer. 
```cpp
auto doc = MakeObject<Document>();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
auto header = MakeObject<HeaderFooter>(doc, HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

SharedPtr<Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
auto footer = MakeObject<HeaderFooter>(doc, HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(ArtifactsDir + u"HeaderFooter.Create.docx");
```


Shows how to delete all footers from a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Header and footer types.docx");

// Iterate through each section and remove footers of every kind.
for (const auto& section : System::IterateOver(doc->LINQ_OfType<SharedPtr<Section>>()))
{
    // There are three kinds of footer and header types.
    // 1 -  The "First" header/footer, which only appears on the first page of a section.
    SharedPtr<HeaderFooter> footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterFirst);
    if (footer != nullptr)
    {
        footer->Remove();
    }

    // 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary);
    if (footer != nullptr)
    {
        footer->Remove();
    }

    // 3 -  The "Even" header/footer, which appears on even pages.
    footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterEven);
    if (footer != nullptr)
    {
        footer->Remove();
    }

    ASSERT_EQ(0,
              section->get_HeadersFooters()->LINQ_Count([](SharedPtr<Node> hf) { return !(System::DynamicCast<HeaderFooter>(hf))->get_IsHeader(); }));
}

doc->Save(ArtifactsDir + u"HeaderFooter.RemoveFooters.docx");
```

## See Also

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
