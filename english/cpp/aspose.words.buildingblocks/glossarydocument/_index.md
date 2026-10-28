---
title: Aspose::Words::BuildingBlocks::GlossaryDocument class
linktitle: GlossaryDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BuildingBlocks::GlossaryDocument class. Represents the root element for a glossary document within a Word document. A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks. To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class


Represents the root element for a glossary document within a Word document. A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks. 
To learn more, visit the Aspose.Words Document Object Model (DOM) (https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```cpp
class GlossaryDocument : public DocumentBase
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the Glossary document. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the Glossary document. |
| [GetBuildingBlock](./getbuildingblock/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery, const System::String \&, const System::String \&) | Finds a building block using the specified gallery, category and name. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_BuildingBlocks](./get_buildingblocks/)() | Returns a typed collection that represents all building blocks in the glossary document. |
| [get_FirstBuildingBlock](./get_firstbuildingblock/)() | Gets the first building block in the glossary document. |
| [get_LastBuildingBlock](./get_lastbuildingblock/)() | Gets the last building block in the glossary document. |
| [get_NodeType](./get_nodetype/)() const override | Returns the [GlossaryDocument](../../aspose.words/nodetype/) value. |
| [GetType](../../aspose.words/documentbase/gettype/)() const override |  |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&, bool) | Imports a node from another document to the current document. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&, bool, Aspose::Words::ImportFormatMode) | Imports a node from another document to the current document with an option to control formatting. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\> \&) | Imports a node from another document to the current document with an option to control formatting. |
| [Is](../../aspose.words/documentbase/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../../aspose.words/documentbase/type/)() |  |
| [get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/)() const | Gets or sets the background shape of the document. Can be **null**. |
| [get_Document](../../aspose.words/documentbase/get_document/)() const override | Gets this instance. |
| [get_FontInfos](../../aspose.words/documentbase/get_fontinfos/)() const | Provides access to properties of fonts used in this document. |
| [get_FootnoteSeparators](../../aspose.words/documentbase/get_footnoteseparators/)() const | Provides access to the footnote/endnote separators defined in the document. |
| [get_Lists](../../aspose.words/documentbase/get_lists/)() const | Provides access to the list formatting used in the document. |
| [get_NodeChangingCallback](../../aspose.words/documentbase/get_nodechangingcallback/)() | Called when a node is inserted or removed in the document. |
| [get_PageColor](../../aspose.words/documentbase/get_pagecolor/)() | Gets or sets the page color of the document. This property is a simpler version of [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [get_ResourceLoadingCallback](../../aspose.words/documentbase/get_resourceloadingcallback/)() const | Allows to control how external resources are loaded. |
| [get_Styles](../../aspose.words/documentbase/get_styles/)() const | Returns a collection of styles defined in the document. |
| [get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/)() const | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [set_BackgroundShape](../../aspose.words/documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\> \&) | Sets the background shape of the document. Can be **null**. |
| [set_NodeChangingCallback](../../aspose.words/documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\> \&) | Called when a node is inserted or removed in the document. |
| [set_PageColor](../../aspose.words/documentbase/set_pagecolor/)(System::Drawing::Color) | Sets the page color of the document. This property is a simpler version of [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [set_ResourceLoadingCallback](../../aspose.words/documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\> \&) | Allows to control how external resources are loaded. |
| [set_WarningCallback](../../aspose.words/documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
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


Some documents, usually templates, can contain AutoText, AutoCorrect entries and/or Building Blocks (also known as glossary document entries, document parts or building blocks).

To access building blocks, you need to load a document into a [Document](../../aspose.words/document/) object. Building blocks will be available via the [GlossaryDocument](../../aspose.words/document/get_glossarydocument/) property.

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects. Each [BuildingBlock](../buildingblock/) represents one document part.

Corresponds to the glossaryDocument and docParts elements in OOXML.
## See Also

* Class [DocumentBase](../../aspose.words/documentbase/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
