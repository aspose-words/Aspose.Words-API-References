---
title: OfficeMath
second_title: Aspose.Words for C++ API Reference
description: Represents an Office Math object such as function, equation, matrix or alike. Can contain child elements including runs of mathematical text, bookmarks, comments, other OfficeMath instances and some other nodes.
type: docs
weight: 1
url: /cpp/aspose.words.math/officemath/
---
## OfficeMath class


Represents an Office [Math](../) object such as function, equation, matrix or alike. Can contain child elements including runs of mathematical text, bookmarks, comments, other [OfficeMath](./) instances and some other nodes.

```cpp
class OfficeMath : public Aspose::Words::CompositeNode, public Aspose::Words::IInline, public Aspose::Words::Revisions::ITrackableNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [get_ChildNodes](../../aspose.words/compositenode/get_childnodes/)() | Gets all immediate child nodes of this node. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_DisplayType](./get_displaytype/)() | Gets/sets Office [Math](../) display format type which represents whether an equation is displayed inline with the text or displayed on its own line. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| [get_EquationXmlEncoding](./get_equationxmlencoding/)() const | Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML. We use the encoding on saving a document to write in same encoding that it was read. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns true if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns true as this node can have child nodes. |
| [get_Justification](./get_justification/)() | Gets/sets Office [Math](../) justification. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_MathObjectType](./get_mathobjecttype/)() const | Gets type [MathObjectType](./get_mathobjecttype/) of this Office [Math](../) object. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeType](./get_nodetype/)() const override | Returns **NodeType.OfficeMath**. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_ParentParagraph](./get_parentparagraph/)() | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetMathRenderer](./getmathrenderer/)() | Creates and returns an object that can be used to render this equation into an image. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(const System::SharedPtr\<Aspose::Words::Node\>\&, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_DisplayType](./set_displaytype/)(Aspose::Words::Math::OfficeMathDisplayType) | Setter for [Aspose::Words::Math::OfficeMath::get_DisplayType](./get_displaytype/). |
| [set_EquationXmlEncoding](./set_equationxmlencoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter for [Aspose::Words::Math::OfficeMath::get_EquationXmlEncoding](./get_equationxmlencoding/). |
| [set_Justification](./set_justification/)(Aspose::Words::Math::OfficeMathJustification) | Setter for [Aspose::Words::Math::OfficeMath::get_Justification](./get_justification/). |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |

In this version of Aspose.Words, [OfficeMath](./) nodes do not provide public methods and properties to create or modify a [OfficeMath](./) object. In this version you are not able to instantiate [Math](../) nodes or modify existing except deleting them.

[OfficeMath](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

## Examples




Shows how to set office math display formatting. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Office math.docx");

auto officeMath = System::DynamicCast<OfficeMath>(doc->GetChild(NodeType::OfficeMath, 0, true));

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
ASSERT_EQ(MathObjectType::OMathPara, officeMath->get_MathObjectType());
ASSERT_EQ(NodeType::OfficeMath, officeMath->get_NodeType());
ASPOSE_ASSERT_EQ(officeMath->get_ParentNode(), officeMath->get_ParentParagraph());

// OOXML and WML formats use the "EquationXmlEncoding" property.
ASSERT_TRUE(officeMath->get_EquationXmlEncoding() == nullptr);

// Change the location and display type of the OfficeMath node.
officeMath->set_DisplayType(OfficeMathDisplayType::Display);
officeMath->set_Justification(OfficeMathJustification::Left);

doc->Save(ArtifactsDir + u"Shape.OfficeMath.docx");
```

