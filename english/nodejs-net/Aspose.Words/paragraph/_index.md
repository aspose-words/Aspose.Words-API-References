---
title: Paragraph class
linktitle: Paragraph class
articleTitle: Paragraph class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Paragraph class. Represents a paragraph of text"
type: docs
weight: 1020
url: /nodejs-net/aspose.words/paragraph/
---

## Paragraph class

Represents a paragraph of text.
To learn more, visit the [Working with Paragraphs](https://docs.aspose.com/words/nodejs-net/working-with-paragraphs/) documentation article.




### Remarks

[Paragraph](./) is a block-level node and can be a child of classes derived from
[Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

The complete list of child nodes that can occur inside a paragraph consists of
[BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/),
[FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/),
[FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/),
[Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/),
[Run](../run/), [SpecialChar](../specialchar/),
[Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/),
[SmartTag](../../aspose.words.markup/smarttag/).

A valid paragraph in Microsoft Word always ends with a paragraph break character and
a minimal valid paragraph consists just of a paragraph break. The [Paragraph](./)
class automatically appends the appropriate paragraph break character at the end
and this character is not part of the child nodes of the [Paragraph](./), therefore
a [Paragraph](./) can be empty.

Do not include the end of paragraph Aspose.Words.ControlChar.ParagraphBreak
or end of cell Aspose.Words.ControlChar.Cell characters inside the text of
the paragraph as it might make the paragraph invalid when the document is opened in Microsoft Word.




**Inheritance:** [Paragraph](./) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Paragraph(doc)](./constructor/#documentbase) | Initializes a new instance of the [Paragraph](./) class. |

### Properties

| Name | Description |
| --- | --- |
| [breakIsStyleSeparator](./breakIsStyleSeparator/) | True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [firstChild](../compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [frameFormat](./frameFormat/) | Provides access to the frame formatting properties. |
| [hasChildNodes](../compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [isDeleteRevision](./isDeleteRevision/) | Returns true if this object was deleted in Microsoft Word while change tracking was enabled. |
| [isEndOfCell](./isEndOfCell/) | True if this paragraph is the last paragraph in a [Cell](../../aspose.words.tables/cell/); false otherwise. |
| [isEndOfDocument](./isEndOfDocument/) | True if this paragraph is the last paragraph in the last section of the document. |
| [isEndOfHeaderFooter](./isEndOfHeaderFooter/) | True if this paragraph is the last paragraph in the [HeaderFooter](../headerfooter/) (main text story) of a [Section](../section/); false otherwise. |
| [isEndOfSection](./isEndOfSection/) | True if this paragraph is the last paragraph in the [Body](../body/) (main text story) of a [Section](../section/); false otherwise. |
| [isFormatRevision](./isFormatRevision/) | Returns true if formatting of the object was changed in Microsoft Word while change tracking was enabled. |
| [isInCell](./isInCell/) | True if this paragraph is an immediate child of [Cell](../../aspose.words.tables/cell/); false otherwise. |
| [isInsertRevision](./isInsertRevision/) | Returns true if this object was inserted in Microsoft Word while change tracking was enabled. |
| [isListItem](./isListItem/) | True when the paragraph is an item in a bulleted or numbered list in original revision. |
| [isMoveFromRevision](./isMoveFromRevision/) | Returns ``true`` if this object was moved (deleted) in Microsoft Word while change tracking was enabled. |
| [isMoveToRevision](./isMoveToRevision/) | Returns ``true`` if this object was moved (inserted) in Microsoft Word while change tracking was enabled. |
| [lastChild](../compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [listFormat](./listFormat/) | Provides access to the list formatting properties of the paragraph. |
| [listLabel](./listLabel/) | Gets a [Paragraph.listLabel](./listLabel/) object that provides access to list numbering value and formatting for this paragraph. |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.Paragraph](../nodetype/#Paragraph). |
| [paragraphBreakFont](./paragraphBreakFont/) | Provides access to the font formatting of the paragraph break character. |
| [paragraphFormat](./paragraphFormat/) | Provides access to the paragraph formatting properties. |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [parentSection](./parentSection/) | Retrieves the parent [Section](../section/) of the paragraph. |
| [parentStory](./parentStory/) | Retrieves the parent section-level story that can be [Body](../body/) or [HeaderFooter](../headerfooter/). |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [runs](./runs/) | Provides access to the typed collection of pieces of text inside the paragraph. |

### Methods

| Name | Description |
| --- | --- |
|[ appendChild(newChild)](../compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ appendField(fieldType, updateField)](./appendField/#fieldtype_boolean) | Appends a field to this paragraph. |
|[ appendField(fieldCode)](./appendField/#string) | Appends a field to this paragraph. |
|[ appendField(fieldCode, fieldValue)](./appendField/#string_string) | Appends a field to this paragraph. |
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
|[ asParagraph()](../node/asParagraph/#default) | Cast node to [Paragraph](./).<br>(Inherited from [Node](../node/)) |
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
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getBuildingBlock(index, isDeep)](../compositenode/getBuildingBlock/#number_boolean) | Returns an Nth child [BuildingBlock](../buildingblock/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getComment(index, isDeep)](../compositenode/getComment/#number_boolean) | Returns an Nth child [Comment](../comment/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../compositenode/getEditableRangeStart/#number_boolean) | Returns an Nth child [EditableRangeStart](../editablerangestart/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getEffectiveTabStops()](./getEffectiveTabStops/#default) | Returns array of all tab stops applied to this paragraph, including applied indirectly by styles or lists. |
|[ getFootnote(index, isDeep)](../compositenode/getFootnote/#number_boolean) | Returns an Nth child [Footnote](../../aspose.words.notes/footnote/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getGroupShape(index, isDeep)](../compositenode/getGroupShape/#number_boolean) | Returns an Nth child [GroupShape](../../aspose.words.drawing/groupshape/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getOfficeMath(index, isDeep)](../compositenode/getOfficeMath/#number_boolean) | Returns an Nth child [OfficeMath](../../aspose.words.math/officemath/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getParagraph(index, isDeep)](../compositenode/getParagraph/#number_boolean) | Returns an Nth child [Paragraph](./) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getRun(index, isDeep)](../compositenode/getRun/#number_boolean) | Returns an Nth child [Run](../run/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdt(index, isDeep)](../compositenode/getSdt/#number_boolean) | Returns an Nth child [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../compositenode/getSdtRangeEnd/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../compositenode/getSdtRangeStart/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getShape(index, isDeep)](../compositenode/getShape/#number_boolean) | Returns an Nth child [Shape](../../aspose.words.drawing/shape/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSmartTag(index, isDeep)](../compositenode/getSmartTag/#number_boolean) | Returns an Nth child [SmartTag](../../aspose.words.markup/smarttag/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getTable(index, isDeep)](../compositenode/getTable/#number_boolean) | Returns an Nth child [Table](../table/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getText()](./getText/#default) | Gets the text of this paragraph including the end of paragraph character. |
|[ indexOf(child)](../compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertAfter(newChild, refChild)](../compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertBefore(newChild, refChild)](../compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertField(fieldType, updateField, refNode, isAfter)](./insertField/#fieldtype_boolean_node_boolean) | Inserts a field into this paragraph. |
|[ insertField(fieldCode, refNode, isAfter)](./insertField/#string_node_boolean) | Inserts a field into this paragraph. |
|[ insertField(fieldCode, fieldValue, refNode, isAfter)](./insertField/#string_string_node_boolean) | Inserts a field into this paragraph. |
|[ joinRunsWithSameFormatting()](./joinRunsWithSameFormatting/#default) | Joins runs with the same formatting in the paragraph. |
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

### See Also

* module [Aspose.Words](../)
* class [CompositeNode](../compositenode/)

