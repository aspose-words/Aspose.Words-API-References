---
title: Aspose::Words::CommentRangeEnd class
linktitle: CommentRangeEnd
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CommentRangeEnd class. Denotes the end of a region of text that has a comment associated with it. To learn more, visit the Working with Comments documentation article in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/commentrangeend/
---
## CommentRangeEnd class


Denotes the end of a region of text that has a comment associated with it. 
To learn more, visit the [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) documentation article.

```cpp
class CommentRangeEnd : public Node,
                        public IDisplaceableByCustomXml,
                        public INodeWithAnnotationId
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [CommentRangeEnd](./commentrangeend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&, int32_t) | Initializes a new instance of this class. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_Id](./get_id/)() const | Specifies the identifier of the comment to which this region is linked to. |
| [get_NodeType](./get_nodetype/)() const override | Returns [CommentRangeEnd](../nodetype/). |
| [set_Id](./set_id/)(int32_t) | Specifies the identifier of the comment to which this region is linked to. |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](../node/gettype/)() const override |  |
| [Is](../node/is/)(const System::TypeInfo \&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| static [Type](../node/type/)() |  |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
## Remarks


To create a comment anchored to a region of text, you need to create a [Comment](../comment/) and then create [CommentRangeStart](../commentrangestart/) and [CommentRangeEnd](./) and set their identifiers to the same [Id](../comment/get_id/) value.

[CommentRangeEnd](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).
## See Also

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
