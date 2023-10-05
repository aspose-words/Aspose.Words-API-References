---
title: Section Class
linktitle: Section
articleTitle: Section
second_title: Aspose.Words for .NET
description: Aspose.Words.Section class. Represents a single section in a document in C#.
type: docs
weight: 5730
url: /net/aspose.words/section/
---
## Section class

Represents a single section in a document.

To learn more, visit the [Working with Sections](https://docs.aspose.com/words/net/working-with-sections/) documentation article.

```csharp
public sealed class Section : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [Section](section/)(*[DocumentBase](../documentbase/)*) | Initializes a new instance of the Section class. |

## Properties

| Name | Description |
| --- | --- |
| [Body](../../aspose.words/section/body/) { get; } | Returns the [`Body`](../body/) child node of the section. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [HeadersFooters](../../aspose.words/section/headersfooters/) { get; } | Provides access to the headers and footers nodes of the section. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/section/nodetype/) { get; } | Returns Section. |
| [PageSetup](../../aspose.words/section/pagesetup/) { get; } | Returns an object that represents page setup and section properties. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [ProtectedForForms](../../aspose.words/section/protectedforforms/) { get; set; } | True if the section is protected for forms. When a section is protected for forms, users can select and modify text only in form fields in Microsoft Word. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/section/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor. |
| override [AcceptEnd](../../aspose.words/section/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| override [AcceptStart](../../aspose.words/section/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) |  |
| [AppendContent](../../aspose.words/section/appendcontent/)(*Section*) | Inserts a copy of content of the source section at the end of this section. |
| [ClearContent](../../aspose.words/section/clearcontent/)() | Clears the section. |
| [ClearHeadersFooters](../../aspose.words/section/clearheadersfooters/)() | Clears the headers and footers of this section. |
| [Clone](../../aspose.words/section/clone/#clone_1)() | Creates a duplicate of this section. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Creates navigator which can be used to traverse and read nodes. |
| [DeleteHeaderFooterShapes](../../aspose.words/section/deleteheaderfootershapes/)() | Deletes all shapes (drawing objects) from the headers and footers of this section. |
| [EnsureMinimum](../../aspose.words/section/ensureminimum/)() | Ensures that the section has [`Body`](./body/) with one [`Paragraph`](../paragraph/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returns the index of the specified child node in the child node array. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) |  |
| [PrependContent](../../aspose.words/section/prependcontent/)(*Section*) | Inserts a copy of content of the source section at the beginning of this section. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../node/) that matches the XPath expression. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

`Section` can have one [`Body`](../body/) and maximum one [`HeaderFooter`](../headerfooter/) of each [`HeaderFooterType`](../headerfootertype/). [`Body`](../body/) and [`HeaderFooter`](../headerfooter/) nodes can be in any order inside `Section`.

A minimal valid section needs to have [`Body`](../body/) with one [`Paragraph`](../paragraph/).

Each section has its own set of properties that specify page size, orientation, margins etc.

You can create a copy of a section using [`Clone`](../node/clone/). The copy can be inserted into the same or different document.

To add, insert or remove a whole section including section break and section properties use methods of the [`Sections`](../document/sections/) object.

To copy and insert just content of the section excluding the section break and section properties use [`AppendContent`](./appendcontent/) and [`PrependContent`](./prependcontent/) methods.

### See Also

* class [CompositeNode](../compositenode/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
