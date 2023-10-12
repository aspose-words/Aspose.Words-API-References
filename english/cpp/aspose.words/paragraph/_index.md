---
title: Aspose::Words::Paragraph class
linktitle: Paragraph
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph class. Represents a paragraph of text. To learn more, visit the  documentation article in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words/paragraph/
---
## Paragraph class


Represents a paragraph of text. To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/) documentation article.

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AppendChild](../compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | Appends a field to this paragraph. |
| [AppendField](./appendfield/)(const System::String\&) | Appends a field to this paragraph. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | Appends a field to this paragraph. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | True if this paragraph break is a [Style](../style/) Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles. |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FrameFormat](./get_frameformat/)() | Provides access to the frame formatting properties. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsEndOfCell](./get_isendofcell/)() | True if this paragraph is the last paragraph in a [Cell](../../aspose.words.tables/cell/); false otherwise. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | True if this paragraph is the last paragraph in the last section of the document. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | True if this paragraph is the last paragraph in the [HeaderFooter](../headerfooter/) (main text story) of a [Section](../section/); false otherwise. |
| [get_IsEndOfSection](./get_isendofsection/)() | True if this paragraph is the last paragraph in the [Body](../body/) (main text story) of a [Section](../section/); false otherwise. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [get_IsInCell](./get_isincell/)() | True if this paragraph is an immediate child of [Cell](../../aspose.words.tables/cell/); false otherwise. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsListItem](./get_islistitem/)() | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_ListFormat](./get_listformat/)() | Provides access to the list formatting properties of the paragraph. |
| [get_ListLabel](./get_listlabel/)() | Gets a [ListLabel](./get_listlabel/) object that provides access to list numbering value and formatting for this paragraph. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Paragraph](../nodetype/). |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | Provides access to the font formatting of the paragraph break character. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Provides access to the paragraph formatting properties. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentSection](./get_parentsection/)() | Retrieves the parent [Section](../section/) of the paragraph. |
| [get_ParentStory](./get_parentstory/)() | Retrieves the parent section-level story that can be [Body](../body/) or [HeaderFooter](../headerfooter/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [get_Runs](./get_runs/)() | Provides access to the typed collection of pieces of text inside the paragraph. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](./gettext/)() override | Gets the text of this paragraph including the end of paragraph character. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../compositenode/insertafter/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../compositenode/insertbefore/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately before the specified reference node. |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserts a field into this paragraph. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserts a field into this paragraph. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserts a field into this paragraph. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Joins runs with the same formatting in the paragraph. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initializes a new instance of the [Paragraph](./) class. |
| [PrependChild](../compositenode/prependchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../compositenode/removechild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the specified child node. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../node/) that matches the XPath expression. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

The complete list of child nodes that can occur inside a paragraph consists of [BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../run/), [SpecialChar](../specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [SmartTag](../../aspose.words.markup/smarttag/).

A valid paragraph in Microsoft Word always ends with a paragraph break character and a minimal valid paragraph consists just of a paragraph break. The [Paragraph](./) class automatically appends the appropriate paragraph break character at the end and this character is not part of the child nodes of the [Paragraph](./), therefore a [Paragraph](./) can be empty.

Do not include the end of paragraph [ParagraphBreak](../controlchar/paragraphbreak/) or end of cell [Cell](../controlchar/cell/) characters inside the text of the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.

## Examples



Shows how to construct an Aspose.Words document by hand. 
```cpp
auto doc = MakeObject<Document>();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc->RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
auto section = MakeObject<Section>(doc);
doc->AppendChild(section);

// Set some page setup properties for the section.
section->get_PageSetup()->set_SectionStart(SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(PaperSize::Letter);

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
auto body = MakeObject<Body>(doc);
section->AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
auto para = MakeObject<Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(ParagraphAlignment::Center);

body->AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
auto run = MakeObject<Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(ArtifactsDir + u"Section.CreateManually.docx");
```

## See Also

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
