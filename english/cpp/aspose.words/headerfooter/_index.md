---
title: Aspose::Words::HeaderFooter class
linktitle: HeaderFooter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::HeaderFooter class. Represents a container for the header or footer text of a section. To learn more, visit the Working with Headers and Footers documentation article in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words/headerfooter/
---
## HeaderFooter class


Represents a container for the header or footer text of a section. 
To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/) documentation article.

```cpp
class HeaderFooter : public Story
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the header. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the header. |
| [HeaderFooter](./headerfooter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&, Aspose::Words::HeaderFooterType) | Creates a new header or footer of the specified type. |
| [get_HeaderFooterType](./get_headerfootertype/)() | Gets the type of this header/footer. |
| [get_IsHeader](./get_isheader/)() | True if this [HeaderFooter](./) object is a header. |
| [get_IsLinkedToPrevious](./get_islinkedtoprevious/)() | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [get_NodeType](./get_nodetype/)() const override | Returns [HeaderFooter](../nodetype/). |
| [get_ParentSection](./get_parentsection/)() | Gets the parent section of this story. |
| [set_IsLinkedToPrevious](./set_islinkedtoprevious/)(bool) | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [AppendParagraph](../story/appendparagraph/)(const System::String \&) | A shortcut method that creates a [Paragraph](../paragraph/) object with optional text and appends it to the end of this object. |
| [DeleteShapes](../story/deleteshapes/)() | Deletes all shapes from the text of this story. |
| [get_FirstParagraph](../story/get_firstparagraph/)() override | Gets the first paragraph in the story. |
| [get_LastParagraph](../story/get_lastparagraph/)() override | Gets the last paragraph in the story. |
| [get_Paragraphs](../story/get_paragraphs/)() override | Gets a collection of paragraphs that are immediate children of the story. |
| [get_StoryType](../story/get_storytype/)() override | Gets the type of this story. |
| [get_Tables](../story/get_tables/)() override | Gets a collection of tables that are immediate children of the story. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [PrependChild](../compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../node/) that matches the XPath expression. |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
## Remarks


[HeaderFooter](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

[HeaderFooter](./) is a section-level node and can only be a child of [Section](../section/). There can only be one [HeaderFooter](./) of each [HeaderFooterType](./get_headerfootertype/) in a [Section](../section/).

If [Section](../section/) does not have a [HeaderFooter](./) of a specific type or the [HeaderFooter](./) has no child nodes, this header/footer is considered linked to the header/footer of the same type of the previous section in Microsoft Word.

When [HeaderFooter](./) contains at least one [Paragraph](../paragraph/), it is no longer considered linked to previous in Microsoft Word.
## Examples


Shows how to create a header and a footer.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```

Shows how to delete all footers from a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Header and footer types.docx"));

// Iterate through each section and remove footers of every kind.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section>>()))
{
    // There are three kinds of footer and header types.
    // 1 -  The "First" header/footer, which only appears on the first page of a section.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  The "Even" header/footer, which appears on even pages.
    footer = section->get_HeadersFooters()->idx_get(HeaderFooterType::FooterEven);
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

Shows how to replace text in a document's footer.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Footer.docx"));

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```
## See Also

* Class [Story](../story/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
