---
title: HeaderFooter class
linktitle: HeaderFooter class
articleTitle: HeaderFooter class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.HeaderFooter class. Represents a container for the header or footer text of a section"
type: docs
weight: 480
url: /nodejs-net/aspose.words/headerfooter/
---

## HeaderFooter class

Represents a container for the header or footer text of a section.
To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/nodejs-net/working-with-headers-and-footers/) documentation article.




### Remarks

[HeaderFooter](./) can contain [Paragraph](../paragraph/) and [Table](../table/) child nodes.

[HeaderFooter](./) is a section-level node and can only be a child of [Section](../section/).
There can only be one [HeaderFooter](./) of each [HeaderFooter.headerFooterType](./headerFooterType/) in a [Section](../section/).

If [Section](../section/) does not have a [HeaderFooter](./) of a specific type or
the [HeaderFooter](./) has no child nodes, this header/footer is considered linked to
the header/footer of the same type of the previous section in Microsoft Word.

When [HeaderFooter](./) contains at least one [Paragraph](../paragraph/), it is no longer
considered linked to previous in Microsoft Word.




**Inheritance:** [HeaderFooter](./) → [Story](../story/) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [HeaderFooter(doc, headerFooterType)](./constructor/#documentbase_headerfootertype) | Creates a new header or footer of the specified type. |

### Properties

| Name | Description |
| --- | --- |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [firstChild](../compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [firstParagraph](../story/firstParagraph/) | Gets the first paragraph in the story.<br>(Inherited from [Story](../story/)) |
| [hasChildNodes](../compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [headerFooterType](./headerFooterType/) | Gets the type of this header/footer. |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [isHeader](./isHeader/) | True if this [HeaderFooter](./) object is a header. |
| [isLinkedToPrevious](./isLinkedToPrevious/) | True if this header or footer is linked to the corresponding header or footer in the previous section. |
| [lastChild](../compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [lastParagraph](../story/lastParagraph/) | Gets the last paragraph in the story.<br>(Inherited from [Story](../story/)) |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.HeaderFooter](../nodetype/#HeaderFooter). |
| [paragraphs](../story/paragraphs/) | Gets a collection of paragraphs that are immediate children of the story.<br>(Inherited from [Story](../story/)) |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parentSection](./parentSection/) | Gets the parent section of this story. |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [storyType](../story/storyType/) | Gets the type of this story.<br>(Inherited from [Story](../story/)) |
| [tables](../story/tables/) | Gets a collection of tables that are immediate children of the story.<br>(Inherited from [Story](../story/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the header. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the header. |
|[ appendChild(newChild)](../compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ appendParagraph(text)](../story/appendParagraph/#string) | A shortcut method that creates a [Paragraph](../paragraph/) object with optional text and appends it to the end of this object.<br>(Inherited from [Story](../story/)) |
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
|[ asHeaderFooter()](../node/asHeaderFooter/#default) | Cast node to [HeaderFooter](./).<br>(Inherited from [Node](../node/)) |
|[ asOfficeMath()](../node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../node/)) |
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](../paragraph/).<br>(Inherited from [Node](../node/)) |
|[ asRow()](../node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../node/)) |
|[ asRun()](../node/asRun/#default) | Cast node to [Run](../run/).<br>(Inherited from [Node](../node/)) |
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
|[ deleteShapes()](../story/deleteShapes/#default) | Deletes all shapes from the text of this story.<br>(Inherited from [Story](../story/)) |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getBuildingBlock(index, isDeep)](../compositenode/getBuildingBlock/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getComment(index, isDeep)](../compositenode/getComment/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../compositenode/getEditableRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getFootnote(index, isDeep)](../compositenode/getFootnote/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getGroupShape(index, isDeep)](../compositenode/getGroupShape/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getOfficeMath(index, isDeep)](../compositenode/getOfficeMath/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getParagraph(index, isDeep)](../compositenode/getParagraph/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getRun(index, isDeep)](../compositenode/getRun/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdt(index, isDeep)](../compositenode/getSdt/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../compositenode/getSdtRangeEnd/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../compositenode/getSdtRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getShape(index, isDeep)](../compositenode/getShape/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSmartTag(index, isDeep)](../compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getTable(index, isDeep)](../compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getText()](../node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ indexOf(child)](../compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertAfter(newChild, refChild)](../compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertBefore(newChild, refChild)](../compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ prependChild(newChild)](../compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ removeAllChildren()](../compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeChild(oldChild)](../compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeSmartTags()](../compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectNodes(xpath)](../compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectSingleNode(xpath)](../compositenode/selectSingleNode/#string) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |

### Examples

Shows how to create a header and a footer.

```js
let doc = new aw.Document();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
let header = new aw.HeaderFooter(doc, aw.HeaderFooterType.HeaderPrimary);
doc.firstSection.headersFooters.add(header);

let para = header.appendParagraph("My header.");

expect(header.isHeader).toEqual(true);
expect(para.isEndOfHeaderFooter).toEqual(true);

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
let footer = new aw.HeaderFooter(doc, aw.HeaderFooterType.FooterPrimary);
doc.firstSection.headersFooters.add(footer);

para = footer.appendParagraph("My footer.");

expect(footer.isHeader).toEqual(false);
expect(para.isEndOfHeaderFooter).toEqual(true);

expect(para.parentStory.referenceEquals(footer)).toEqual(true);
expect(para.parentSection.referenceEquals(footer.parentSection)).toEqual(true);
expect(header.parentSection.referenceEquals(footer.parentSection)).toEqual(true);

doc.save(base.artifactsDir + "HeaderFooter.create.docx");
```

Shows how to delete all footers from a document.

```js
let doc = new aw.Document(base.myDir + "Header and footer types.docx");

// Iterate through each section and remove footers of every kind.
for (let section of doc.sections.toArray())
{
  // There are three kinds of footer and header types.
  // 1 -  The "First" header/footer, which only appears on the first page of a section.
  let footer = section.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterFirst);
  footer.remove();

  // 2 -  The "Primary" header/footer, which appears on odd pages.
  footer = section.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary);
  footer.remove();

  // 3 -  The "Even" header/footer, which appears on even pages. 
  footer = section.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterEven);
  footer.remove();

  let count = section.headersFooters.toArray().filter((hf) => !hf.isHeader).length;
  expect(count).toEqual(0);
}

doc.save(base.artifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Shows how to replace text in a document's footer.

```js
let doc = new aw.Document(base.myDir + "Footer.docx");

let headersFooters = doc.firstSection.headersFooters;
let footer = headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary);

let options = new aw.Replacing.FindReplaceOptions();
options.matchCase = false;
options.findWholeWordsOnly = false;

let currentYear = new Date().getYear();
footer.range.replace("(C) 2006 Aspose Pty Ltd.", `Copyright (C) ${currentYear} by Aspose Pty Ltd.`, options);

doc.save(base.artifactsDir + "HeaderFooter.ReplaceText.docx");
```

### See Also

* module [Aspose.Words](../)
* class [Story](../story/)

