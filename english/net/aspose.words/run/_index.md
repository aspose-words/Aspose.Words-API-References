---
title: Run Class
linktitle: Run
articleTitle: Run
second_title: Aspose.Words for .NET
description: Aspose.Words.Run class. Represents a run of characters with the same font formatting in C#.
type: docs
weight: 4820
url: /net/aspose.words/run/
---
## Run class

Represents a run of characters with the same font formatting.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public class Run : Inline
```

## Constructors

| Name | Description |
| --- | --- |
| [Run](run/#constructor)(*[DocumentBase](../documentbase/)*) | Initializes a new instance of the `Run` class. |
| [Run](run/#constructor_1)(*[DocumentBase](../documentbase/), string*) | Initializes a new instance of the **Run** class. |

## Properties

| Name | Description |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Gets the document to which this node belongs. |
| [Font](../../aspose.words/inline/font/) { get; } | Provides access to the font formatting of this object. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returns `true` if this node can contain other nodes. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Returns `true` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Returns `true` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [IsPhoneticGuide](../../aspose.words/run/isphoneticguide/) { get; } | Gets a boolean value indicating either the run is a phonetic guide. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/run/nodetype/) { get; } | Returns Run. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Retrieves the parent [`Paragraph`](../paragraph/) of this node. |
| [PhoneticGuide](../../aspose.words/run/phoneticguide/) { get; } | Gets a [`PhoneticGuide`](./phoneticguide/) object. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |
| [Text](../../aspose.words/run/text/) { get; set; } | Gets or sets the text of the run. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/run/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| override [GetText](../../aspose.words/run/gettext/)() | Gets the text of the run. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |

## Remarks

All text of the document is stored in runs of text.

`Run` can only be a child of [`Paragraph`](../paragraph/) or inline [`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/).

## Examples

Shows how to format a run of text using its font property.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### See Also

* class [Inline](../inline/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
