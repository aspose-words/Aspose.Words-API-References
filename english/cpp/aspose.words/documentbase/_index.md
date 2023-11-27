---
title: Aspose::Words::DocumentBase class
linktitle: DocumentBase
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBase class. Provides the abstract base class for a main document and a glossary document of a Word document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words/documentbase/
---
## DocumentBase class


Provides the abstract base class for a main document and a glossary document of a Word document. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) |  |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) |  |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [get_BackgroundShape](./get_backgroundshape/)() const | Gets or sets the background shape of the document. Can be **null**. |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| [get_Document](./get_document/)() const override | Gets this instance. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_FontInfos](./get_fontinfos/)() const | Provides access to properties of fonts used in this document. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| [get_Lists](./get_lists/)() const | Provides access to the list formatting used in the document. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | Called when a node is inserted or removed in the document. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Gets the type of this node. |
| [get_PageColor](./get_pagecolor/)() | Gets or sets the page color of the document. This property is a simpler version of [BackgroundShape](./get_backgroundshape/). |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Allows to control how external resources are loaded. |
| [get_Styles](./get_styles/)() const | Returns a collection of styles defined in the document. |
| [get_WarningCallback](./get_warningcallback/)() const | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Imports a node from another document to the current document. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Imports a node from another document to the current document with an option to control formatting. |
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
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Selects the first [Node](../node/) that matches the XPath expression. |
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Setter for [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Setter for [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Setter for [Aspose::Words::DocumentBase::get_NodeChangingCallback](./get_nodechangingcallback/). |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | Setter for [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Setter for [Aspose::Words::DocumentBase::get_ResourceLoadingCallback](./get_resourceloadingcallback/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exports the content of the node into a string using the specified save options. |
| static [Type](./type/)() |  |
## Remarks


Aspose.Words represents a Word document as a tree of nodes. [DocumentBase](./) is a root node of the tree that contains all other nodes of the document.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## Examples



Shows how to initialize the subclasses of [DocumentBase](./). 
```cpp
auto doc = MakeObject<Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = MakeObject<GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## See Also

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
