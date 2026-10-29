---
title: Aspose::Words::Section class
linktitle: Section
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Section class. Represents a single section in a document. To learn more, visit the Working with Sections documentation article in C++.'
type: docs
weight: 58000
url: /cpp/aspose.words/section/
---
## Section class


Represents a single section in a document. 
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/) documentation article.

```cpp
class Section : public CompositeNode,
                public ISectionAttrSource
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendContent](./appendcontent/)(const System::SharedPtr\<Aspose::Words::Section\> \&) | Inserts a copy of content of the source section at the end of this section. |
| [ClearContent](./clearcontent/)() | Clears the section. |
| [ClearHeadersFooters](./clearheadersfooters/)() | Clears the headers and footers of this section. |
| [ClearHeadersFooters](./clearheadersfooters/)(bool) | Clears the headers and footers of this section. |
| [Clone](./clone/)() | Creates a duplicate of this section. |
| [DeleteHeaderFooterShapes](./deleteheaderfootershapes/)() | Deletes all shapes (drawing objects) from the headers and footers of this section. |
| [EnsureMinimum](./ensureminimum/)() | Ensures that the section has [Body](./get_body/) with one [Paragraph](../paragraph/). |
| [PrependContent](./prependcontent/)(const System::SharedPtr\<Aspose::Words::Section\> \&) | Inserts a copy of content of the source section at the beginning of this section. |
| [Section](./section/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&) | Initializes a new instance of the Section class. |
| [get_Body](./get_body/)() | Returns the [Body](../body/) child node of the section. |
| [get_HeadersFooters](./get_headersfooters/)() | Provides access to the headers and footers nodes of the section. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Section](../nodetype/). |
| [get_PageSetup](./get_pagesetup/)() | Returns an object that represents page setup and section properties. |
| [get_ProtectedForForms](./get_protectedforforms/)() | True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word. |
| [set_ProtectedForForms](./set_protectedforforms/)(bool) | True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word. |
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


[Section](./) can have one [Body](../body/) and maximum one [HeaderFooter](../headerfooter/) of each [HeaderFooterType](../headerfootertype/). [Body](../body/) and [HeaderFooter](../headerfooter/) nodes can be in any order inside [Section](./).

A minimal valid section needs to have [Body](../body/) with one [Paragraph](../paragraph/).

Each section has its own set of properties that specify page size, orientation, margins etc.

You can create a copy of a section using [Clone()](../node/clone/). The copy can be inserted into the same or different document.

To add, insert or remove a whole section including section break and section properties use methods of the [Sections](../document/get_sections/) object.

To copy and insert just content of the section excluding the section break and section properties use [AppendContent()](./appendcontent/) and [PrependContent()](./prependcontent/) methods.
## Examples


Shows how to construct an Aspose.Words document by hand.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```
## See Also

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
