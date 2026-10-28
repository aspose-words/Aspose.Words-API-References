---
title: Aspose::Words::BuildingBlocks::BuildingBlock class
linktitle: BuildingBlock
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::BuildingBlock class. Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry. To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class


Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry. 
To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```cpp
class BuildingBlock : public CompositeNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the BuildingBlock. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the BuildingBlock. |
| [BuildingBlock](./buildingblock/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> \&) | Initializes a new instance of this class. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_Behavior](./get_behavior/)() const | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [get_Category](./get_category/)() const | Specifies the second-level categorization for the building block. |
| [get_Description](./get_description/)() const | Gets or sets the description associated with this building block. |
| [get_FirstSection](./get_firstsection/)() | Gets the first section in the building block. |
| [get_Gallery](./get_gallery/)() const | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [get_Guid](./get_guid/)() const | Gets or sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [get_LastSection](./get_lastsection/)() | Gets the last section in the building block. |
| [get_Name](./get_name/)() const | Gets or sets the name of this building block. |
| [get_NodeType](./get_nodetype/)() const override | Returns the [BuildingBlock](../../aspose.words/nodetype/) value. |
| [get_Sections](./get_sections/)() | Returns a collection that represents all sections in the building block. |
| [get_Type](./get_type/)() const | Specifies the building block type. |
| [set_Behavior](./set_behavior/)(Aspose::Words::BuildingBlocks::BuildingBlockBehavior) | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [set_Category](./set_category/)(const System::String \&) | Specifies the second-level categorization for the building block. |
| [set_Description](./set_description/)(const System::String \&) | Sets the description associated with this building block. |
| [set_Gallery](./set_gallery/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery) | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [set_Guid](./set_guid/)(System::Guid) | Sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [set_Name](./set_name/)(const System::String \&) | Sets the name of this building block. |
| [set_Type](./set_type/)(Aspose::Words::BuildingBlocks::BuildingBlockType) | Specifies the building block type. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/compositenode/gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [Is](../../aspose.words/compositenode/is/)(const System::TypeInfo \&) const override |  |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| static [Type](../../aspose.words/compositenode/type/)() |  |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| virtual [GetText](../../aspose.words/node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](../../aspose.words/node/gettype/)() const override |  |
| [Is](../../aspose.words/node/is/)(const System::TypeInfo \&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| static [Type](../../aspose.words/node/type/)() |  |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
## Remarks


[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

You can create new building blocks and insert them into a glossary document. You can modify or delete existing building blocks. You can copy or move building blocks between documents. You can insert content of a building block into a document.

Corresponds to the docPart, docPartPr and docPartBody elements in OOXML.
## See Also

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
