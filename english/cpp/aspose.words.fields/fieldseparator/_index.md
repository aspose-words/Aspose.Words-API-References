---
title: Aspose::Words::Fields::FieldSeparator class
linktitle: FieldSeparator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldSeparator class. Represents a Word field separator that separates the field code from the field result. To learn more, visit the Working with Fields documentation article in C++.'
type: docs
weight: 90000
url: /cpp/aspose.words.fields/fieldseparator/
---
## FieldSeparator class


Represents a Word field separator that separates the field code from the field result. 
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldSeparator : public FieldChar
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [get_NodeType](./get_nodetype/)() const override | Returns [FieldSeparator](../../aspose.words/nodetype/). |
| [GetField](../fieldchar/getfield/)() | Returns a field for the field char. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Returns the type of the field. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Gets or sets whether the parent field is locked (should not recalculate its result). |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Sets whether the parent field is locked (should not recalculate its result). |
| [Accept](../../aspose.words/specialchar/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Gets the special character that this node represents. |
| [get_NodeType](../../aspose.words/specialchar/get_nodetype/)() const override | Returns [SpecialChar](../../aspose.words/nodetype/). |
| [get_Font](../../aspose.words/inline/get_font/)() | Provides access to the font formatting of this object. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Retrieves the parent [Paragraph](../../aspose.words/paragraph/) of this node. |
| virtual [Accept](../../aspose.words/node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/). |
| virtual [GetText](../../aspose.words/node/gettext/)() | Gets the text of this node and of all its children. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../../aspose.words/node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../../aspose.words/node/get_range/)() | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
## Remarks


[FieldSeparator](./) is an inline-level node and represented by the [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) control character in the document.

[FieldSeparator](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

A complete field in a Microsoft Word document is a complex structure consisting of a field start character, field code, field separator character, field result and field end character. Some fields only have field start, field code and field end.

To easily insert a new field into a document, use the [InsertField()](../../aspose.words/documentbuilder/insertfield/) method.
## See Also

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
