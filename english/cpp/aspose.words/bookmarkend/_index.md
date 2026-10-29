---
title: Aspose::Words::BookmarkEnd class
linktitle: BookmarkEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BookmarkEnd class. Represents an end of a bookmark in a Word document. To learn more, visit the Working with Bookmarks documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/bookmarkend/
---
## BookmarkEnd class


Represents an end of a bookmark in a Word document. 
To learn more, visit the [Working with Bookmarks](https://docs.aspose.com/words/cpp/working-with-bookmarks/) documentation article.

```cpp
class BookmarkEnd : public Node,
                    public IBookmarkNode,
                    public IDisplaceableByCustomXml
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [BookmarkEnd](./bookmarkend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&, const System::String \&) | Initializes a new instance of the [BookmarkEnd](./) class. |
| [get_Name](./get_name/)() override | Gets or sets the bookmark name. |
| [get_NodeType](./get_nodetype/)() const override | Returns [BookmarkEnd](../nodetype/). |
| [set_Name](./set_name/)(System::String) override | Sets the bookmark name. |
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


A complete bookmark in a Word document consists of a [BookmarkStart](../bookmarkstart/) and a matching [BookmarkEnd](./) with the same bookmark name.

[BookmarkStart](../bookmarkstart/) and [BookmarkEnd](./) are just markers inside a document that specify where the bookmark starts and ends.

Use the [Bookmark](../bookmark/) class as a "facade" to work with a bookmark as a single object.
## See Also

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
