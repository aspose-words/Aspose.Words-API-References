---
title: Class DocumentBase
second_title: Aspose.Words for .NET API Reference
description: Provides the abstract base class for a main document and a glossary document of a Word document in C#
type: docs
weight: 430
url: /net/aspose.words/documentbase/
---
## DocumentBase class

Provides the abstract base class for a main document and a glossary document of a Word document.

To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) documentation article.

```csharp
public abstract class DocumentBase : CompositeNode
```

## Properties

| Name | Description |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Gets or sets the background shape of the document. Can be `null`. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| override [Document](../../aspose.words/documentbase/document/) { get; } |  |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Provides access to properties of fonts used in this document. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Provides access to the list formatting used in the document. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Called when a node is inserted or removed in the document. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Gets the type of this node. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Gets or sets the page color of the document. This property is a simpler version of [`BackgroundShape`](./backgroundshape/). |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Allows to control how external resources are loaded. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Returns a collection of styles defined in the document. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserved for system use. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode)(Node, bool) | Imports a node from another document to the current document. |
| [ImportNode](../../aspose.words/documentbase/importnode/#importnode_1)(Node, bool, ImportFormatMode) | Imports a node from another document to the current document with an option to control formatting. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserts the specified node immediately before the specified reference node. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selects the first [`Node`](../node/) that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

Aspose.Words represents a Word document as a tree of nodes. `DocumentBase` is a root node of the tree that contains all other nodes of the document.

`DocumentBase` also stores document-wide information such as [`Styles`](./styles/) and [`Lists`](./lists/) that the tree nodes might refer to.

## Examples

Shows how to initialize the subclasses of DocumentBase.

```csharp
Document doc = new Document();

Assert.AreEqual(typeof(DocumentBase), doc.GetType().BaseType);

GlossaryDocument glossaryDoc = new GlossaryDocument();
doc.GlossaryDocument = glossaryDoc;

Assert.AreEqual(typeof(DocumentBase), glossaryDoc.GetType().BaseType);
```

### See Also

* class [CompositeNode](../compositenode/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
