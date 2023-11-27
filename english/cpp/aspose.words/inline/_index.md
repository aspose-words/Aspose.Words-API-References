---
title: Aspose::Words::Inline class
linktitle: Inline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Inline class. Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own. To learn more, visit the  documentation article in C++.'
type: docs
weight: 36000
url: /cpp/aspose.words/inline/
---
## Inline class


Base class for inline-level nodes that can have character formatting associated with them, but cannot have child nodes of their own. To learn more, visit the [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) documentation article.

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_Font](./get_font/)() | Provides access to the font formatting of this object. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](./get_parentparagraph/)() | Retrieves the parent [Paragraph](../paragraph/) of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


A class derived from [Inline](./) can be a child of [Paragraph](../paragraph/).

## Examples



Shows how to determine the revision type of an inline node. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Revision runs.docx");

// When we edit the document while the "Track Changes" option, found in via Review -> Tracking,
// is turned on in Microsoft Word, the changes we apply count as revisions.
// When editing a document using Aspose.Words, we can begin tracking revisions by
// invoking the document's "StartTrackRevisions" method and stop tracking by using the "StopTrackRevisions" method.
// We can either accept revisions to assimilate them into the document
// or reject them to change the proposed change effectively.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// The parent node of a revision is the run that the revision concerns. A Run is an Inline node.
auto run = System::ExplicitCast<Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

SharedPtr<Paragraph> firstParagraph = run->get_ParentParagraph();
SharedPtr<RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Below are five types of revisions that can flag an Inline node.
// 1 -  An "insert" revision:
// This revision occurs when we insert text while tracking changes.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  A "format" revision:
// This revision occurs when we change the formatting of text while tracking changes.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  A "move from" revision:
// When we highlight text in Microsoft Word, and then drag it to a different place in the document
// while tracking changes, two revisions appear.
// The "move from" revision is a copy of the text originally before we moved it.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  A "move to" revision:
// The "move to" revision is the text that we moved in its new position in the document.
// "Move from" and "move to" revisions appear in pairs for every move revision we carry out.
// Accepting a move revision deletes the "move from" revision and its text,
// and keeps the text from the "move to" revision.
// Rejecting a move revision conversely keeps the "move from" revision and deletes the "move to" revision.
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  A "delete" revision:
// This revision occurs when we delete text while tracking changes. When we delete text like this,
// it will stay in the document as a revision until we either accept the revision,
// which will delete the text for good, or reject the revision, which will keep the text we deleted where it was.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## See Also

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
