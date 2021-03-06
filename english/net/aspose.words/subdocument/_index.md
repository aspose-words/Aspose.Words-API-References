---
title: SubDocument
second_title: Aspose.Words for .NET API Reference
description: Represents a SubDocument - which is a reference to an externally stored document.
type: docs
weight: 5870
url: /net/aspose.words/subdocument/
---
## SubDocument class

Represents a **SubDocument** - which is a reference to an externally stored document.

```csharp
public class SubDocument : Node
```

## Properties

| Name | Description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Returns true if this node can contain other nodes. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/subdocument/nodetype) { get; } | Returns **NodeType.SubDocument** |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept)(DocumentVisitor) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| virtual [GetText](../../aspose.words/node/gettext)() | Gets the text of this node and of all its children. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove)() | Removes itself from the parent. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

## Remarks

In this version of Aspose.Words, [`SubDocument`](../subdocument) nodes do not provide public methods and properties to create or modify a subdocument. In this version you are not able to instantiate SubDocument nodes or modify existing except deleting them.

[`SubDocument`](../subdocument) can only be a child of [`Paragraph`](../paragraph).

## Examples

Shows how to access a master document's subdocument.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// This node serves as a reference to an external document, and its contents cannot be accessed.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### See Also

* class [Node](../node)
* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
