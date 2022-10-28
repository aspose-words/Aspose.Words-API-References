---
title: Story
second_title: Aspose.Words for C++ API Reference
description: Base class for elements that contain block-level nodes Paragraph and Table.
type: docs
weight: 807
url: /cpp/aspose.words/story/
---
## Story class


Base class for elements that contain block-level nodes [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/).

```cpp
class Story : public Aspose::Words::CompositeNode
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [AppendChild](../compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendParagraph](./appendparagraph/)(const System::String\&) | A shortcut method that creates a [Paragraph](../paragraph/) object with optional text and appends it to the end of this object. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [DeleteShapes](./deleteshapes/)() | Deletes all shapes from the text of this story. |
| [get_ChildNodes](../compositenode/get_childnodes/)() | Gets all immediate child nodes of this node. |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FirstParagraph](./get_firstparagraph/)() | Gets the first paragraph in the story. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns true if this node has any child nodes. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns true as this node can have child nodes. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_LastParagraph](./get_lastparagraph/)() | Gets the last paragraph in the story. |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Gets the type of this node. |
| [get_Paragraphs](./get_paragraphs/)() | Gets a collection of paragraphs that are immediate children of the story. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [get_StoryType](./get_storytype/)() const | Gets the type of this story. |
| [get_Tables](./get_tables/)() | Gets a collection of tables that are immediate children of the story. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../compositenode/gettext/)() override | Gets the text of this node and of all its children. |
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
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

Text of a Word document is said to consist of several stories. The main text is stored in the main text story represented by [Body](../body/), each header and footer is stored in a separate story represented by [HeaderFooter](../headerfooter/).

## Examples




Shows how to remove all shapes from a node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Use a DocumentBuilder to insert a shape. This is an inline shape,
// which has a parent Paragraph, which is a child node of the first section's Body.
builder->InsertShape(ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(NodeType::Shape, true)->get_Count());

// We can delete all shapes from the child paragraphs of this Body.
ASSERT_EQ(StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(NodeType::Shape, true)->get_Count());
```

