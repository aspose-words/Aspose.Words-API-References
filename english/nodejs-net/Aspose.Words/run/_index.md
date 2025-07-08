---
title: Run class
linktitle: Run class
articleTitle: Run class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Run class. Represents a run of characters with the same font formatting"
type: docs
weight: 1110
url: /nodejs-net/aspose.words/run/
---

## Run class

Represents a run of characters with the same font formatting.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Remarks

All text of the document is stored in runs of text.

[Run](./) can only be a child of [Paragraph](../paragraph/) or inline [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).




**Inheritance:** [Run](./) → [Inline](../inline/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Run(doc)](./constructor/#documentbase) | Initializes a new instance of the [Run](./) class. |
| [Run(doc, text)](./constructor/#documentbase_string) | Initializes a new instance of the **Run** class. |

### Properties

| Name | Description |
| --- | --- |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [font](../inline/font/) | Provides access to the font formatting of this object.<br>(Inherited from [Inline](../inline/)) |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [isDeleteRevision](../inline/isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [isFormatRevision](../inline/isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [isInsertRevision](../inline/isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [isMoveFromRevision](../inline/isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [isMoveToRevision](../inline/isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled.<br>(Inherited from [Inline](../inline/)) |
| [isPhoneticGuide](./isPhoneticGuide/) | Gets a boolean value indicating either the run is a phonetic guide. |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.Run](../nodetype/#Run). |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parentParagraph](../inline/parentParagraph/) | Retrieves the parent [Paragraph](../paragraph/) of this node.<br>(Inherited from [Inline](../inline/)) |
| [phoneticGuide](./phoneticGuide/) | Gets a [Run.phoneticGuide](./phoneticGuide/) object. |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [text](./text/) | Gets or sets the text of the run. |

### Methods

| Name | Description |
| --- | --- |
|[ asBody()](../node/asBody/#default) | Cast node to [Body](../body/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkEnd()](../node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../bookmarkend/).<br>(Inherited from [Node](../node/)) |
|[ asBookmarkStart()](../node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../bookmarkstart/).<br>(Inherited from [Node](../node/)) |
|[ asBuildingBlock()](../node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../buildingblock/).<br>(Inherited from [Node](../node/)) |
|[ asCell()](../node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../node/)) |
|[ asComment()](../node/asComment/#default) | Cast node to [Comment](../comment/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeEnd()](../node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../commentrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asCommentRangeStart()](../node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../commentrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asCompositeNode()](../node/asCompositeNode/#default) | Cast node to [CompositeNode](../compositenode/).<br>(Inherited from [Node](../node/)) |
|[ asDocument()](../node/asDocument/#default) | Cast node to [Node.document](../node/document/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeEnd()](../node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../editablerangeend/).<br>(Inherited from [Node](../node/)) |
|[ asEditableRangeStart()](../node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../editablerangestart/).<br>(Inherited from [Node](../node/)) |
|[ asFieldEnd()](../node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../node/)) |
|[ asFieldSeparator()](../node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../node/)) |
|[ asFieldStart()](../node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../node/)) |
|[ asFootnote()](../node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../node/)) |
|[ asFormField()](../node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../node/)) |
|[ asGlossaryDocument()](../node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../aspose.words.buildingblocks/glossarydocument/).<br>(Inherited from [Node](../node/)) |
|[ asGroupShape()](../node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../node/)) |
|[ asHeaderFooter()](../node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../headerfooter/).<br>(Inherited from [Node](../node/)) |
|[ asOfficeMath()](../node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../node/)) |
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](../paragraph/).<br>(Inherited from [Node](../node/)) |
|[ asRow()](../node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../node/)) |
|[ asRun()](../node/asRun/#default) | Cast node to [Run](./).<br>(Inherited from [Node](../node/)) |
|[ asSection()](../node/asSection/#default) | Cast node to [Section](../section/).<br>(Inherited from [Node](../node/)) |
|[ asShape()](../node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../node/)) |
|[ asSmartTag()](../node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../node/)) |
|[ asSpecialChar()](../node/asSpecialChar/#default) | Cast node to [SpecialChar](../specialchar/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTag()](../node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeEnd()](../node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../node/)) |
|[ asStructuredDocumentTagRangeStart()](../node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../node/)) |
|[ asSubDocument()](../node/asSubDocument/#default) | Cast node to [SubDocument](../subdocument/).<br>(Inherited from [Node](../node/)) |
|[ asTable()](../node/asTable/#default) | Cast node to [Table](../table/).<br>(Inherited from [Node](../node/)) |
|[ clone(isCloneChildren)](../node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../node/)) |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getText()](./getText/#default) | Gets the text of the run. |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to construct an Aspose.words document by hand.

```js
let doc = new aw.Document();

// A blank document contains one section, one body and one paragraph.
// Call the "RemoveAllChildren" method to remove all those nodes,
// and end up with a document node with no children.
doc.removeAllChildren();

// This document now has no composite child nodes that we can add content to.
// If we wish to edit it, we will need to repopulate its node collection.
// First, create a new section, and then append it as a child to the root document node.
let section = new aw.Section(doc);
doc.appendChild(section);

// Set some page setup properties for the section.
section.pageSetup.sectionStart = aw.SectionStart.NewPage;
section.pageSetup.paperSize = aw.PaperSize.Letter;

// A section needs a body, which will contain and display all its contents
// on the page between the section's header and footer.
let body = new aw.Body(doc);
section.appendChild(body);

// Create a paragraph, set some formatting properties, and then append it as a child to the body.
let para = new aw.Paragraph(doc);

para.paragraphFormat.styleName = "Heading 1";
para.paragraphFormat.alignment = aw.ParagraphAlignment.Center;

body.appendChild(para);

// Finally, add some content to do the document. Create a run,
// set its appearance and contents, and then append it as a child to the paragraph.
let run = new aw.Run(doc);
run.text = "Hello World!";
run.font.color = "#FF0000";
para.appendChild(run);

expect(doc.getText().trim()).toEqual("Hello World!");

doc.save(base.artifactsDir + "Section.CreateManually.docx");
```

Shows how to format a run of text using its font property.

```js
let doc = new aw.Document();
let run = new aw.Run(doc, "Hello world!");

let font = run.font;
font.name = "Courier New";
font.size = 36;
font.highlightColor = "#FFFF00";

doc.firstSection.body.firstParagraph.appendChild(run);
doc.save(base.artifactsDir + "Font.CreateFormattedRun.docx");
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```js
let doc = new aw.Document();

// An empty document, by default, has one paragraph.
expect(doc.firstSection.body.paragraphs.count).toEqual(1);

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
let paragraph = doc.firstSection.body.firstParagraph;
let paragraphText = new aw.Run(doc, "Initial text. ");
paragraph.appendChild(paragraphText);

// Create three more run nodes.
let run1 = new aw.Run(doc, "Run 1. ");
let run2 = new aw.Run(doc, "Run 2. ");
let run3 = new aw.Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
expect(paragraph.getText().trim()).toEqual("Initial text.");

// Insert the second run into the paragraph in front of the initial run.
paragraph.insertBefore(run2, paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 2. Initial text.");

// Insert the third run after the initial run.
paragraph.insertAfter(run3, paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 2. Initial text. Run 3.");

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.prependChild(run1);

expect(paragraph.getText().trim()).toEqual("Run 1. Run 2. Initial text. Run 3.");
expect(paragraph.getChildNodes(aw.NodeType.Any, true).count).toEqual(4);

// We can modify the contents of the run by editing and deleting existing child nodes.
//paragraph.getChildNodes(aw.NodeType.Run, true).toArray().at(1).text = "Updated run 2. ";
//paragraph.getChildNodes(aw.NodeType.Run, true).remove(paragraphText);
paragraph.getChildNodes(aw.NodeType.Run, true).toArray().at(1).asRun().text = "Updated run 2. ";
paragraph.getChildNodes(aw.NodeType.Run, true).remove(paragraphText);

expect(paragraph.getText().trim()).toEqual("Run 1. Updated run 2. Run 3.");
expect(paragraph.getChildNodes(aw.NodeType.Any, true).count).toEqual(3);
```

### See Also

* module [Aspose.Words](../)
* class [Inline](../inline/)

