---
title: Cell
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 5890
url: /net/aspose.words.tables/cell/
---
## Cell class

Represents a table cell.

```csharp
public class Cell : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [Cell](cell)(DocumentBase) | Initializes a new instance of the **Cell** class. |

## Properties

| Name | Description |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat) { get; } | Provides access to the formatting properties of the cell. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph) { get; } | Gets the first paragraph among the immediate children. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returns true if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returns true as this node can have child nodes. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell) { get; } | True if this is the first cell inside a row; false otherwise. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell) { get; } | True if this is the last cell inside a row; false otherwise. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Gets the last child of the node. |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph) { get; } | Gets the last paragraph among the immediate children. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.tables/cell/nodetype) { get; } | Returns **NodeType.Cell**. |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs) { get; } | Gets a collection of paragraphs that are immediate children of the cell. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [ParentRow](../../aspose.words.tables/cell/parentrow) { get; } | Returns the parent row of the cell. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [Tables](../../aspose.words.tables/cell/tables) { get; } | Gets a collection of tables that are immediate children of the cell. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserved for system use. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum)() | If the last child is not a paragraph, creates and appends one empty paragraph. |
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

**Cell** can only be a child of a **Row**.

**Cell** can contain block-level nodes **Paragraph** and **Table**.

A minimal valid cell needs to have at least one **Paragraph**.

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
