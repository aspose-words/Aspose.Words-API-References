---
title: SmartTag
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 3760
url: /net/aspose.words.markup/smarttag/
---
## SmartTag class

This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph.

```csharp
public class SmartTag : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [SmartTag](smarttag)(DocumentBase) | Initializes a new instance of the [`SmartTag`](../smarttag) class. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [Element](../../aspose.words.markup/smarttag/element) { get; set; } | Specifies the name of the smart tag within the document. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Gets the first child of the node. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returns true if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returns true as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Gets the last child of the node. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.markup/smarttag/nodetype) { get; } | Returns **NodeType.SmartTag**. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Properties](../../aspose.words.markup/smarttag/properties) { get; } | A collection of the smart tag properties. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [Uri](../../aspose.words.markup/smarttag/uri) { get; set; } | Specifies the namespace URI of the smart tag. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.markup/smarttag/accept)(DocumentVisitor) | Accepts a visitor. |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Removes all [`SmartTag`](../smarttag) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Selects the first Node that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

### Remarks

Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding customer-defined semantics into the document via the ability to provide a basic namespace/name for a run or set of runs within a document.

[`SmartTag`](../smarttag) can be a child of a [`Paragraph`](../../aspose.words/paragraph) or another [`SmartTag`](../smarttag) node.

The complete list of child nodes that can occur inside a smart tag consists of [`BookmarkStart`](../../aspose.words/bookmarkstart), [`BookmarkEnd`](../../aspose.words/bookmarkend), [`FieldStart`](../../aspose.words.fields/fieldstart), [`FieldSeparator`](../../aspose.words.fields/fieldseparator), [`FieldEnd`](../../aspose.words.fields/fieldend), [`FormField`](../../aspose.words.fields/formfield), [`Comment`](../../aspose.words/comment), [`Footnote`](../../aspose.words.notes/footnote), [`Run`](../../aspose.words/run), [`SpecialChar`](../../aspose.words/specialchar), [`Shape`](../../aspose.words.drawing/shape), [`GroupShape`](../../aspose.words.drawing/groupshape), [`CommentRangeStart`](../../aspose.words/commentrangestart), [`CommentRangeEnd`](../../aspose.words/commentrangeend), [`SmartTag`](../smarttag).

### See Also

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Markup](../../aspose.words.markup)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
