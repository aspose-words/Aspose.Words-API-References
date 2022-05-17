---
title: BuildingBlock
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 120
url: /net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Represents a glossary document entry such as a Building Block, AutoText or an AutoCorrect entry.

```csharp
public class BuildingBlock : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [BuildingBlock](buildingblock)(GlossaryDocument) | Initializes a new instance of this class. |

## Properties

| Name | Description |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior) { get; set; } | Specifies the behavior that shall be applied when the contents of the building block is inserted into the main document. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category) { get; set; } | Specifies the second-level categorization for the building block. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description) { get; set; } | Gets or sets the description associated with this building block. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Gets the first child of the node. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection) { get; } | Gets the first section in the building block. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery) { get; set; } | Specifies the first-level categorization for the building block for the purposes of classification or user interface sorting. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid) { get; set; } | Gets or sets an identifier (a 128-bit GUID) that uniquely identifies this building block. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returns true if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returns true as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Gets the last child of the node. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection) { get; } | Gets the last section in the building block. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name) { get; set; } | Gets or sets the name of this building block. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype) { get; } | Returns the BuildingBlock value. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections) { get; } | Returns a collection that represents all sections in the building block. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type) { get; set; } | Specifies the building block type. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserved for system use. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Selects the first Node that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

### Remarks

[`BuildingBlock`](../buildingblock) can contain only [`Section`](../../aspose.words/section) nodes.

[`BuildingBlock`](../buildingblock) can only be a child of [`GlossaryDocument`](../glossarydocument).

You can create new building blocks and insert them into a glossary document. You can modify or delete existing building blocks. You can copy or move building blocks between documents. You can insert content of a building block into a document.

Corresponds to the **docPart**, **docPartPr** and **docPartBody** elements in OOXML.

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
