---
title: Aspose::Words::Markup::SmartTag class
linktitle: SmartTag
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SmartTag class. This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph. To learn more, visit the Structured Document Tags or Content Control documentation article in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.markup/smarttag/
---
## SmartTag class


This element specifies the presence of a smart tag around one or more inline structures (runs, images, fields,etc.) within a paragraph. 
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) documentation article.

```cpp
class SmartTag : public CompositeNode,
                 public IMarkupNode
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the SmartTag. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the SmartTag. |
| [SmartTag](./smarttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\> \&) | Initializes a new instance of the [SmartTag](./) class. |
| [get_Element](./get_element/)() const | Specifies the name of the smart tag within the document. |
| [get_NodeType](./get_nodetype/)() const override | Returns [SmartTag](../../aspose.words/nodetype/). |
| [get_Properties](./get_properties/)() const | A collection of the smart tag properties. |
| [get_Uri](./get_uri/)() const | Specifies the namespace URI of the smart tag. |
| [set_Element](./set_element/)(const System::String \&) | Specifies the name of the smart tag within the document. |
| [set_Uri](./set_uri/)(const System::String \&) | Specifies the namespace URI of the smart tag. |
| virtual [AcceptEnd](../../aspose.words/compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../../aspose.words/compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [SmartTag](./) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Gets the last child of the node. |
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


Smart tags is a kind of custom XML markup. Smart tags provide a facility for embedding customer-defined semantics into the document via the ability to provide a basic namespace/name for a run or set of runs within a document.

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or another [SmartTag](./) node.

The complete list of child nodes that can occur inside a smart tag consists of [BookmarkStart](../../aspose.words/bookmarkstart/), [BookmarkEnd](../../aspose.words/bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../../aspose.words/comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../../aspose.words/run/), [SpecialChar](../../aspose.words/specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [CommentRangeStart](../../aspose.words/commentrangestart/), [CommentRangeEnd](../../aspose.words/commentrangeend/), [SmartTag](./).
## See Also

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
