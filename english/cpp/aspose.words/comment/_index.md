---
title: Aspose::Words::Comment class
linktitle: Comment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment class. Represents a container for text of a comment. To learn more, visit the  documentation article in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/comment/
---
## Comment class


Represents a container for text of a comment. To learn more, visit the [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) documentation article.

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the comment. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the comment. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Adds a reply to this comment. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Initializes a new instance of the [Comment](./) class. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Initializes a new instance of the [Comment](./) class. |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | If the last child is not a paragraph, creates and appends one empty paragraph. |
| [get_Ancestor](./get_ancestor/)() | Returns the parent [Comment](./) object. Returns **null** for top-level comments. |
| [get_Author](./get_author/)() const | Returns or sets the author name for a comment. |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_DateTime](./get_datetime/)() const | Gets the date and time that the comment was made. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Gets the UTC date and time that the comment was made. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_Done](./get_done/)() const | Gets or sets flag indicating that the comment has been marked done. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Gets the first paragraph in the story. |
| [get_Font](../inlinestory/get_font/)() | Provides access to the font formatting of the anchor character of this object. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_Id](./get_id/)() const | Gets or sets the comment identifier. |
| [get_Initial](./get_initial/)() const | Returns or sets the initials of the user associated with a specific comment. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Gets the last paragraph in the story. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Gets a collection of paragraphs that are immediate children of the story. |
| [get_ParentId](./get_parentid/)() const | Gets the parent comment ID. A value of **%-1** means the comment has no parent. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [get_Replies](./get_replies/)() | Returns a collection of [Comment](./) objects that are immediate children of the specified comment. |
| [get_StoryType](./get_storytype/)() override | Returns [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Gets a collection of tables that are immediate children of the story. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveAllReplies](./removeallreplies/)() | Removes all replies to this comment. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Removes the specified reply to this comment. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../node/) that matches the XPath expression. |
| [set_Author](./set_author/)(const System::String\&) | Setter for [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Gets the date and time that the comment was made. |
| [set_Done](./set_done/)(bool) | Setter for [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Setter for [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Setter for [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Sets the parent comment ID. A value of **%-1** means the comment has no parent. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | This is a convenience method that allows to easily set text of the comment. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


A comment is an annotation which is anchored to a region of text or to a position in text. A comment can contain an arbitrary amount of block-level content.

If a [Comment](./) object occurs on its own, the comment is anchored to the position of the [Comment](./) object.

To anchor a comment to a region of text three objects are required: [Comment](./), [CommentRangeStart](../commentrangestart/) and [CommentRangeEnd](../commentrangeend/). All three objects need to share the same [Id](./get_id/) value.

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Examples



Shows how to add a comment to a document, and then reply to it. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Place the comment at a node in the document's body.
// This comment will show up at the location of its paragraph,
// outside the right-side margin of the page, and with a dotted line connecting it to its paragraph.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Add a reply, which will show up under its parent comment.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Comments and replies are both Comment nodes.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Comments that do not reply to other comments are "top-level". They have no ancestor comments.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Replies have an ancestor top-level comment.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


Shows how to add a comment to a paragraph. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word, we can right-click this comment in the document body to edit it, or reply to it.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## See Also

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
