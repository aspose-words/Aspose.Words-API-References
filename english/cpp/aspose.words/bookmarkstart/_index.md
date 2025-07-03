---
title: Aspose::Words::BookmarkStart class
linktitle: BookmarkStart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BookmarkStart class. Represents a start of a bookmark in a Word document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/bookmarkstart/
---
## BookmarkStart class


Represents a start of a bookmark in a Word document. To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class BookmarkStart : public Aspose::Words::Node,
                      public Aspose::Words::IBookmarkNode,
                      public Aspose::Words::IDisplaceableByCustomXml
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [BookmarkStart](./bookmarkstart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | Initializes a new instance of the [BookmarkStart](./) class. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_Bookmark](./get_bookmark/)() | Gets the facade object that encapsulates this bookmark start and end. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_Name](./get_name/)() override | Gets the bookmark name. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns [BookmarkStart](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](./gettext/)() override | Returns an empty string. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Name](./set_name/)(System::String) override | Sets the bookmark name. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


A complete bookmark in a Word document consists of a [BookmarkStart](./) and a matching [BookmarkEnd](../bookmarkend/) with the same bookmark name.

[BookmarkStart](./) and [BookmarkEnd](../bookmarkend/) are just markers inside a document that specify where the bookmark starts and ends.

Use the [Bookmark](./get_bookmark/) class as a "facade" to work with a bookmark as a single object. 
## See Also

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
