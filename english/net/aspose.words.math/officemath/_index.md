---
title: OfficeMath
second_title: Aspose.Words for .NET API Reference
description: Represents an Office Math object such as function equation matrix or alike. Can contain child elements including runs of mathematical text bookmarks comments other OfficeMath./officemath instances and some other nodes.
type: docs
weight: 3880
url: /net/aspose.words.math/officemath/
---
## OfficeMath class

Represents an Office Math object such as function, equation, matrix or alike. Can contain child elements including runs of mathematical text, bookmarks, comments, other [`OfficeMath`](../officemath) instances and some other nodes.

```csharp
public class OfficeMath : CompositeNode
```

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| [DisplayType](../../aspose.words.math/officemath/displaytype) { get; set; } | Gets/sets Office Math display format type which represents whether an equation is displayed inline with the text or displayed on its own line. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [EquationXmlEncoding](../../aspose.words.math/officemath/equationxmlencoding) { get; set; } | Gets/sets an encoding that was used to encode equation XML, if this office math object is read from equation XML. We use the encoding on saving a document to write in same encoding that it was read. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Gets the first child of the node. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returns true if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returns true as this node can have child nodes. |
| [Justification](../../aspose.words.math/officemath/justification) { get; set; } | Gets/sets Office Math justification. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Gets the last child of the node. |
| [MathObjectType](../../aspose.words.math/officemath/mathobjecttype) { get; } | Gets type [`MathObjectType`](./mathobjecttype) of this Office Math object. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.math/officemath/nodetype) { get; } | Returns **NodeType.OfficeMath**. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words.math/officemath/parentparagraph) { get; } | Retrieves the parent [`Paragraph`](../../aspose.words/paragraph) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.math/officemath/accept)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserved for system use. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Provides support for the for each style iteration over the child nodes of this node. |
| [GetMathRenderer](../../aspose.words.math/officemath/getmathrenderer)() | Creates and returns an object that can be used to render this equation into an image. |
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

## Remarks

In this version of Aspose.Words, [`OfficeMath`](../officemath) nodes do not provide public methods and properties to create or modify a OfficeMath object. In this version you are not able to instantiate Math nodes or modify existing except deleting them.

[`OfficeMath`](../officemath) can only be a child of [`Paragraph`](../../aspose.words/paragraph).

## Examples

Shows how to set office math display formatting.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OOXML and WML formats use the "EquationXmlEncoding" property.
Assert.IsNull(officeMath.EquationXmlEncoding);

// Change the location and display type of the OfficeMath node.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Math](../../aspose.words.math)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
