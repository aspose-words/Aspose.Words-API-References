---
title: FieldSeparator
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 2190
url: /net/aspose.words.fields/fieldseparator/
---
## FieldSeparator class

Represents a Word field separator that separates the field code from the field result.

```csharp
public class FieldSeparator : FieldChar
```

## Properties

| Name | Description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [FieldType](../../aspose.words.fields/fieldchar/fieldtype) { get; } | Returns the type of the field. |
| [Font](../../aspose.words/inline/font) { get; } | Provides access to the font formatting of this object. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Returns true if this node can contain other nodes. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsDirty](../../aspose.words.fields/fieldchar/isdirty) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsLocked](../../aspose.words.fields/fieldchar/islocked) { get; set; } | Gets or sets whether the parent field is locked (should not recalculate its result). |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.fields/fieldseparator/nodetype) { get; } | Returns FieldSeparator. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Retrieves the parent [`Paragraph`](../../aspose.words/paragraph) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.fields/fieldseparator/accept)(DocumentVisitor) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| [GetField](../../aspose.words.fields/fieldchar/getfield)() | Returns a field for the field char. |
| override [GetText](../../aspose.words/specialchar/gettext)() | Gets the special character that this node represents. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove)() | Removes itself from the parent. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exports the content of the node into a string using the specified save options. |

### Remarks

[`FieldSeparator`](../fieldseparator) is an inline-level node and represented by the [`FieldSeparatorChar`](../../aspose.words/controlchar/fieldseparatorchar) control character in the document.

[`FieldSeparator`](../fieldseparator) can only be a child of [`Paragraph`](../../aspose.words/paragraph).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [`InsertField`](../../aspose.words/documentbuilder/insertfield) method.

### See Also

* class [FieldChar](../fieldchar)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
