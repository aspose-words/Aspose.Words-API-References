---
title: Paragraph
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4100
url: /net/aspose.words/paragraph/
---
## Paragraph class

Represents a paragraph of text.

```csharp
public class Paragraph : CompositeNode
```

## Constructors

| Name | Description |
| --- | --- |
| [Paragraph](paragraph)(DocumentBase) | Initializes a new instance of the **Paragraph** class. |

## Properties

| Name | Description |
| --- | --- |
| [BreakIsStyleSeparator](../../aspose.words/paragraph/breakisstyleseparator) { get; } | True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Gets all immediate child nodes of this node. |
| [Count](../../aspose.words/compositenode/count) { get; } | Gets the number of immediate children of this node. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Specifies custom node identifier. |
| virtual [Document](../../aspose.words/node/document) { get; } | Gets the document to which this node belongs. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Gets the first child of the node. |
| [FrameFormat](../../aspose.words/paragraph/frameformat) { get; } | Provides access to the paragraph formatting properties. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Returns true if this node has any child nodes. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Returns true as this node can have child nodes. |
| [IsDeleteRevision](../../aspose.words/paragraph/isdeleterevision) { get; } | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [IsEndOfCell](../../aspose.words/paragraph/isendofcell) { get; } | True if this paragraph is the last paragraph in a [`Cell`](../../aspose.words.tables/cell); false otherwise. |
| [IsEndOfDocument](../../aspose.words/paragraph/isendofdocument) { get; } | True if this paragraph is the last paragraph in the last section of the document. |
| [IsEndOfHeaderFooter](../../aspose.words/paragraph/isendofheaderfooter) { get; } | True if this paragraph is the last paragraph in the **HeaderFooter** (main text story) of a **Section**; false otherwise. |
| [IsEndOfSection](../../aspose.words/paragraph/isendofsection) { get; } | True if this paragraph is the last paragraph in the **Body** (main text story) of a **Section**; false otherwise. |
| [IsFormatRevision](../../aspose.words/paragraph/isformatrevision) { get; } | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [IsInCell](../../aspose.words/paragraph/isincell) { get; } | True if this paragraph is an immediate child of [`Cell`](../../aspose.words.tables/cell); false otherwise. |
| [IsInsertRevision](../../aspose.words/paragraph/isinsertrevision) { get; } | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [IsListItem](../../aspose.words/paragraph/islistitem) { get; } | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [IsMoveFromRevision](../../aspose.words/paragraph/ismovefromrevision) { get; } | Returns **true** if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [IsMoveToRevision](../../aspose.words/paragraph/ismovetorevision) { get; } | Returns **true** if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Gets the last child of the node. |
| [ListFormat](../../aspose.words/paragraph/listformat) { get; } | Provides access to the list formatting properties of the paragraph. |
| [ListLabel](../../aspose.words/paragraph/listlabel) { get; } | Gets a [`ListLabel`](./listlabel) object that provides access to list numbering value and formatting for this paragraph. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Gets the node immediately following this node. |
| override [NodeType](../../aspose.words/paragraph/nodetype) { get; } | Returns **NodeType.Paragraph**. |
| [ParagraphBreakFont](../../aspose.words/paragraph/paragraphbreakfont) { get; } | Provides access to the font formatting of the paragraph break character. |
| [ParagraphFormat](../../aspose.words/paragraph/paragraphformat) { get; } | Provides access to the paragraph formatting properties. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Gets the immediate parent of this node. |
| [ParentSection](../../aspose.words/paragraph/parentsection) { get; } | Retrieves the parent [`Section`](../section) of the paragraph. |
| [ParentStory](../../aspose.words/paragraph/parentstory) { get; } | Retrieves the parent section-level story that can be [`Body`](../body) or [`HeaderFooter`](../headerfooter). |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Gets the node immediately preceding this node. |
| [Range](../../aspose.words/node/range) { get; } | Returns a **Range** object that represents the portion of a document that is contained in this node. |
| [Runs](../../aspose.words/paragraph/runs) { get; } | Provides access to the typed collection of pieces of text inside the paragraph. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/paragraph/accept)(DocumentVisitor) | Accepts a visitor. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_1)(string) | Appends a field to this paragraph. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield)(FieldType, bool) | Appends a field to this paragraph. |
| [AppendField](../../aspose.words/paragraph/appendfield#appendfield_2)(string, string) | Appends a field to this paragraph. |
| [Clone](../../aspose.words/node/clone)(bool) | Creates a duplicate of the node. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserved for system use. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Gets the first ancestor of the specified [`NodeType`](../nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEffectiveTabStops](../../aspose.words/paragraph/geteffectivetabstops)() | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Provides support for the for each style iteration over the child nodes of this node. |
| override [GetText](../../aspose.words/paragraph/gettext)() | Gets the text of this paragraph including the end of paragraph character. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Inserts the specified node immediately before the specified reference node. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_1)(string, Node, bool) | Inserts a field into this paragraph. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield)(FieldType, bool, Node, bool) | Inserts a field into this paragraph. |
| [InsertField](../../aspose.words/paragraph/insertfield#insertfield_2)(string, string, Node, bool) | Inserts a field into this paragraph. |
| [JoinRunsWithSameFormatting](../../aspose.words/paragraph/joinrunswithsameformatting)() | Joins runs with the same formatting in the paragraph. |
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

### Remarks

[`Paragraph`](../paragraph) is a block-level node and can be a child of classes derived from [`Story`](../story) or [`InlineStory`](../inlinestory).

[`Paragraph`](../paragraph) can contain any number of inline-level nodes and bookmarks.

The complete list of child nodes that can occur inside a paragraph consists of [`BookmarkStart`](../bookmarkstart), [`BookmarkEnd`](../bookmarkend), [`FieldStart`](../../aspose.words.fields/fieldstart), [`FieldSeparator`](../../aspose.words.fields/fieldseparator), [`FieldEnd`](../../aspose.words.fields/fieldend), [`FormField`](../../aspose.words.fields/formfield), [`Comment`](../comment), [`Footnote`](../../aspose.words.notes/footnote), [`Run`](../run), [`SpecialChar`](../specialchar), [`Shape`](../../aspose.words.drawing/shape), [`GroupShape`](../../aspose.words.drawing/groupshape), [`SmartTag`](../../aspose.words.markup/smarttag).

A valid paragraph in Microsoft Word always ends with a paragraph break character and a minimal valid paragraph consists just of a paragraph break. The **Paragraph** class automatically appends the appropriate paragraph break character at the end and this character is not part of the child nodes of the **Paragraph**, therefore a **Paragraph** can be empty.

Do not include the end of paragraph [`ControlChar.ParagraphBreak`](../controlchar/paragraphbreak) or end of cell [`ControlChar.Cell`](../controlchar/cell) characters inside the text of the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.

### Examples

Shows how to construct an Aspose.Words document by hand.

```csharp
Document doc = new Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.RemoveAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
Section section = new Section(doc);
doc.AppendChild(section);

// Set some page setup properties for the section.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
Body body = new Body(doc);
section.AppendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### See Also

* class [CompositeNode](../compositenode)
* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
