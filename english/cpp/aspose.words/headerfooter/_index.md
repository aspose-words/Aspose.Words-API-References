---
title: HeaderFooter
second_title: Aspose.Words for C++ API Reference
description: Represents a container for the header or footer text of a section.
type: docs
weight: 391
url: /cpp/aspose.words/headerfooter/
---
## HeaderFooter class


Represents a container for the header or footer text of a section.

```cpp
class HeaderFooter : public Aspose::Words::Story
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AppendChild](../compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendParagraph](../story/appendparagraph/)(const System::String\&) | A shortcut method that creates a [Paragraph](../paragraph/) object with optional text and appends it to the end of this object. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [DeleteShapes](../story/deleteshapes/)() | Deletes all shapes from the text of this story. |
| [get_ChildNodes](../compositenode/get_childnodes/)() | Gets all immediate child nodes of this node. |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FirstParagraph](../story/get_firstparagraph/)() | Gets the first paragraph in the story. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns true if this node has any child nodes. |
| [get_HeaderFooterType](./get_headerfootertype/)() | Gets the type of this header/footer. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns true as this node can have child nodes. |
| [get_IsHeader](./get_isheader/)() | True if this **HeaderFooter** object is a header. |
| [get_IsLinkedToPrevious](./get_islinkedtoprevious/)() | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_LastParagraph](../story/get_lastparagraph/)() | Gets the last paragraph in the story. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns **NodeType.HeaderFooter**. |
| [get_Paragraphs](../story/get_paragraphs/)() | Gets a collection of paragraphs that are immediate children of the story. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentSection](./get_parentsection/)() | Gets the parent section of this story. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [get_StoryType](../story/get_storytype/)() const | Gets the type of this story. |
| [get_Tables](../story/get_tables/)() | Gets a collection of tables that are immediate children of the story. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [HeaderFooter](./headerfooter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::HeaderFooterType) | Creates a new header or footer of the specified type. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../compositenode/insertafter/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../compositenode/insertbefore/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../compositenode/prependchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../compositenode/removechild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the specified child node. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../node/) that matches the XPath expression. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_IsLinkedToPrevious](./set_islinkedtoprevious/)(bool) | Setter for [Aspose::Words::HeaderFooter::get_IsLinkedToPrevious](./get_islinkedtoprevious/). |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

**HeaderFooter** can contain **Paragraph** and **Table** child nodes.

**HeaderFooter** is a section-level node and can only be a child of **Section**. There can only be one **HeaderFooter** or each [HeaderFooterType](./get_headerfootertype/) in a **Section**.

If **Section** does not have a **HeaderFooter** of a specific type or the **HeaderFooter** has no child nodes, this header/footer is considered linked to the header/footer of the same type of the previous section in Microsoft Word.

When **HeaderFooter** contains at least one **Paragraph**, it is no longer considered linked to previous in Microsoft Word.

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


Shows how to replace text in a document's footer. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Footer.docx");

SharedPtr<HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
SharedPtr<HeaderFooter> footer = headersFooters->idx_get(HeaderFooterType::FooterPrimary);

auto options = MakeObject<FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(ArtifactsDir + u"HeaderFooter.ReplaceText.docx");
```

