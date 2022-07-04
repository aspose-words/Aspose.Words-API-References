---
title: Footnote
second_title: Aspose.Words for .NET API Reference
description: Represents a container for text of a footnote or endnote.
type: docs
weight: 4020
url: /net/aspose.words.notes/footnote/
---
## Footnote class

Represents a container for text of a footnote or endnote.

```csharp
public class Footnote : InlineStory
```

## Constructors

| Name | Description |
| --- | --- |
| [Footnote](footnote)(DocumentBase, FootnoteType) | Initializes an instance of the **Footnote** class. |

## Properties

| Name | Description |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Gets the first child of the node. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Gets the first paragraph in the story. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Provides access to the font formatting of the anchor character of this object. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype) { get; } | Returns a value that specifies whether this is a footnote or endnote. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returns true if this node has any child nodes. |
| [IsAuto](../../aspose.words.notes/footnote/isauto) { get; set; } | Holds a value that specifies whether this is a auto-numbered footnote or footnote with user defined custom reference mark. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returns true as this node can have child nodes. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Gets the last child of the node. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Gets the last paragraph in the story. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype) { get; } | Returns **NodeType.Footnote**. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Gets a collection of paragraphs that are immediate children of the story. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Retrieves the parent [`Paragraph`](../../aspose.words/paragraph) of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark) { get; set; } | Gets/sets custom reference mark to be used for this footnote. Default value is **empty string** (Empty), meaning auto-numbered footnotes are used. |
| override [StoryType](../../aspose.words.notes/footnote/storytype) { get; } | Returns **StoryType.Footnotes** or **StoryType.Endnotes**. |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Gets a collection of tables that are immediate children of the story. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserved for system use. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | If the last child is not a paragraph, creates and appends one empty paragraph. |
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

## Remarks

The **Footnote** class is used to represent both footnotes and endnotes in a Word document.

**Footnote** is an inline-level node and can only be a child of **Paragraph**.

**Footnote** can contain **Paragraph** and **Table** child nodes.

## Examples

Shows how to insert and customize footnotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
Assert.True(footnote.IsAuto);

// We can move the document builder inside the footnote to edit its reference text. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### See Also

* class [InlineStory](../../aspose.words/inlinestory)
* namespace [Aspose.Words.Notes](../../aspose.words.notes)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
