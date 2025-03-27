---
title: StructuredDocumentTag class
linktitle: StructuredDocumentTag class
articleTitle: StructuredDocumentTag class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.StructuredDocumentTag class. Represents a structured document tag (SDT or content control) in a document"
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Markup/structureddocumenttag/
---

## StructuredDocumentTag class

Represents a structured document tag (SDT or content control) in a document.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Remarks

Structured document tags (SDTs) allow to embed customer-defined semantics as well as its
behavior and appearance into a document.

In this version Aspose.Words provides a number of public methods and properties to
manipulate the behavior and content of [StructuredDocumentTag](./).
Mapping of SDT nodes to custom XML packages within a document can be performed with using
the [StructuredDocumentTag.xmlMapping](./xmlMapping/) property.

[StructuredDocumentTag](./) can occur in a document in the following places:


* Block-level - Among paragraphs and tables, as a child of a [Body](../../Aspose.Words/body/), [HeaderFooter](../../Aspose.Words/headerfooter/),
  [Comment](../../Aspose.Words/comment/), [Footnote](../../Aspose.Words.Notes/footnote/) or a [Shape](../../Aspose.Words.Drawing/shape/) node.
  
* Row-level - Among rows in a table, as a child of a [Table](../../Aspose.Words/table/) node.
  
* Cell-level - Among cells in a table row, as a child of a [Row](../../Aspose.Words.Tables/row/) node.
  
* Inline-level - Among inline content inside, as a child of a [Paragraph](../../Aspose.Words/paragraph/).
  
* Nested inside another [StructuredDocumentTag](./).
  



**Inheritance:** [StructuredDocumentTag](./) → [CompositeNode](../../Aspose.Words/compositenode/) → [Node](../../Aspose.Words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [StructuredDocumentTag(doc, type, level)](./StructuredDocumentTag/#documentbase_sdttype_markuplevel) | Initializes a new instance of the **Structured document tag** class. |

### Properties

| Name | Description |
| --- | --- |
| [appearance](./appearance/) | Gets/sets the appearance of a structured document tag. |
| [buildingBlockCategory](./buildingBlockCategory/) | Specifies category of building block for this **SDT** node. Can not be ``None``. |
| [buildingBlockGallery](./buildingBlockGallery/) | Specifies type of building block for this **SDT**. Can not be ``None``. |
| [calendarType](./calendarType/) | Specifies the type of calendar for this **SDT**. Default is [SdtCalendarType.Default](../sdtcalendartype/#Default) |
| [checked](./checked/) | Gets/Sets current state of the Checkbox **SDT**. Default value for this property is ``False``. |
| [color](./color/) | Gets or sets the color of the structured document tag. |
| [contentsFont](./contentsFont/) | Font formatting that will be applied to text entered into **SDT**. |
| [count](../../Aspose.Words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [dateDisplayFormat](./dateDisplayFormat/) | String that represents the format in which dates are displayed. |
| [dateDisplayLocale](./dateDisplayLocale/) | Allows to set/get the language format for the date displayed in this **SDT**. |
| [dateStorageFormat](./dateStorageFormat/) | Gets/sets format in which the date for a date SDT is stored when the **SDT** is bound to an XML node in the document's data store. Default value is [SdtDateStorageFormat.DateTime](../sdtdatestorageformat/#DateTime) |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [endCharacterFont](./endCharacterFont/) | Font formatting that will be applied to the last character of text entered into **SDT**. |
| [firstChild](../../Aspose.Words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [fullDate](./fullDate/) | Specifies the full date and time last entered into this **SDT**. |
| [hasChildNodes](../../Aspose.Words/compositenode/hasChildNodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [id](./id/) | Specifies a unique read-only persistent numerical Id for this **SDT**. |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [isShowingPlaceholderText](./isShowingPlaceholderText/) | Specifies whether the content of this **SDT** shall be interpreted to contain placeholder text (as opposed to regular text contents within the SDT). |
| [isTemporary](./isTemporary/) | Specifies whether this **SDT** shall be removed from the WordProcessingML document when its contents are modified. |
| [lastChild](../../Aspose.Words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [level](./level/) | Gets the level at which this **SDT** occurs in the document tree. |
| [listItems](./listItems/) | Gets [SdtListItemCollection](../sdtlistitemcollection/) associated with this **SDT**. |
| [lockContentControl](./lockContentControl/) | When set to ``True``, this property will prohibit a user from deleting this **SDT**. |
| [lockContents](./lockContents/) | When set to ``True``, this property will prohibit a user from editing the contents of this **SDT**. |
| [multiline](./multiline/) | Specifies whether this **SDT** allows multiple lines of text. |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeType](./nodeType/) | Returns [NodeType.StructuredDocumentTag](../../Aspose.Words/nodetype/#StructuredDocumentTag). |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [placeholder](./placeholder/) | Gets the [BuildingBlock](../../Aspose.Words/buildingblock/) containing placeholder text which should be displayed when this SDT run contents are empty, the associated mapped XML element is empty as specified via the [StructuredDocumentTag.xmlMapping](./xmlMapping/) element or the [StructuredDocumentTag.isShowingPlaceholderText](./isShowingPlaceholderText/) element is ``True``. |
| [placeholderName](./placeholderName/) | Gets or sets Name of the [BuildingBlock](../../Aspose.Words/buildingblock/) containing placeholder text. |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [sdtType](./sdtType/) | Gets type of this **Structured document tag**. |
| [style](./style/) | Gets or sets the Style of the structured document tag. |
| [styleName](./styleName/) | Gets or sets the name of the style applied to the structured document tag. |
| [tag](./tag/) | Specifies a tag associated with the current SDT node. Can not be ``None``. |
| [title](./title/) | Specifies the friendly name associated with this **SDT**. Can not be ``None``. |
| [wordOpenXML](./wordOpenXML/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../Aspose.Words/saveformat/#FlatOpc) format. |
| [wordOpenXMLMinimal](./wordOpenXMLMinimal/) | Gets a string that represents the XML contained within the node in the [SaveFormat.FlatOpc](../../Aspose.Words/saveformat/#FlatOpc) format. |
| [xmlMapping](./xmlMapping/) | Gets an object that represents the mapping of this structured document tag to XML data in a custom XML part of the current document. |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the StructuredDocumentTag. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the StructuredDocumentTag. |
|[ appendChild(newChild)](../../Aspose.Words/compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ asBody()](../../Aspose.Words/node/asBody/#default) | Cast node to [Body](../../Aspose.Words/body/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkEnd()](../../Aspose.Words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../Aspose.Words/bookmarkend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBookmarkStart()](../../Aspose.Words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../Aspose.Words/bookmarkstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asBuildingBlock()](../../Aspose.Words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../Aspose.Words/buildingblock/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCell()](../../Aspose.Words/node/asCell/#default) | Cast node to [Cell](../../Aspose.Words.Tables/cell/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asComment()](../../Aspose.Words/node/asComment/#default) | Cast node to [Comment](../../Aspose.Words/comment/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeEnd()](../../Aspose.Words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../Aspose.Words/commentrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCommentRangeStart()](../../Aspose.Words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../Aspose.Words/commentrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asCompositeNode()](../../Aspose.Words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../Aspose.Words/compositenode/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asDocument()](../../Aspose.Words/node/asDocument/#default) | Cast node to [Node.document](../../Aspose.Words/node/document/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeEnd()](../../Aspose.Words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../Aspose.Words/editablerangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asEditableRangeStart()](../../Aspose.Words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../Aspose.Words/editablerangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldEnd()](../../Aspose.Words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../../Aspose.Words.Fields/fieldend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldSeparator()](../../Aspose.Words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../Aspose.Words.Fields/fieldseparator/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFieldStart()](../../Aspose.Words/node/asFieldStart/#default) | Cast node to [FieldStart](../../Aspose.Words.Fields/fieldstart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFootnote()](../../Aspose.Words/node/asFootnote/#default) | Cast node to [Footnote](../../Aspose.Words.Notes/footnote/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asFormField()](../../Aspose.Words/node/asFormField/#default) | Cast node to [FormField](../../Aspose.Words.Fields/formfield/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGlossaryDocument()](../../Aspose.Words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](../../Aspose.Words.BuildingBlocks/glossarydocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](../smarttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](./).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSubDocument()](../../Aspose.Words/node/asSubDocument/#default) | Cast node to [SubDocument](../../Aspose.Words/subdocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asTable()](../../Aspose.Words/node/asTable/#default) | Cast node to [Table](../../Aspose.Words/table/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ clear()](./clear/#default) | Clears contents of this structured document tag and displays a placeholder if it is defined. |
|[ clone(isCloneChildren)](../../Aspose.Words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getAncestor(ancestorType)](../../Aspose.Words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../Aspose.Words/nodetype/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getBuildingBlock(index, isDeep)](../../Aspose.Words/compositenode/getBuildingBlock/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../../Aspose.Words/compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../../Aspose.Words/compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getComment(index, isDeep)](../../Aspose.Words/compositenode/getComment/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../../Aspose.Words/compositenode/getEditableRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getFootnote(index, isDeep)](../../Aspose.Words/compositenode/getFootnote/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getGroupShape(index, isDeep)](../../Aspose.Words/compositenode/getGroupShape/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getOfficeMath(index, isDeep)](../../Aspose.Words/compositenode/getOfficeMath/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getParagraph(index, isDeep)](../../Aspose.Words/compositenode/getParagraph/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getRun(index, isDeep)](../../Aspose.Words/compositenode/getRun/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSdt(index, isDeep)](../../Aspose.Words/compositenode/getSdt/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../../Aspose.Words/compositenode/getSdtRangeEnd/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../../Aspose.Words/compositenode/getSdtRangeStart/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getShape(index, isDeep)](../../Aspose.Words/compositenode/getShape/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getSmartTag(index, isDeep)](../../Aspose.Words/compositenode/getSmartTag/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getTable(index, isDeep)](../../Aspose.Words/compositenode/getTable/#number_boolean) | <br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ getText()](../../Aspose.Words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ indexOf(child)](../../Aspose.Words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../Aspose.Words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../Aspose.Words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ nextPreOrder(rootNode)](../../Aspose.Words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ nodeTypeToString(nodeType)](../../Aspose.Words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ prependChild(newChild)](../../Aspose.Words/compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ previousPreOrder(rootNode)](../../Aspose.Words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ referenceEquals(other)](../../Aspose.Words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ remove()](../../Aspose.Words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ removeAllChildren()](../../Aspose.Words/compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ removeChild(oldChild)](../../Aspose.Words/compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ removeSelfOnly()](./removeSelfOnly/#default) | Removes just this SDT node itself, but keeps the content of it inside the document tree. |
|[ removeSmartTags()](../../Aspose.Words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](../smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectNodes(xpath)](../../Aspose.Words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectSingleNode(xpath)](../../Aspose.Words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../Aspose.Words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ setCheckedSymbol(characterCode, fontName)](./setCheckedSymbol/#number_string) | Sets the symbol used to represent the checked state of a check box content control. |
|[ setUncheckedSymbol(characterCode, fontName)](./setUncheckedSymbol/#number_string) | Sets the symbol used to represent the unchecked state of a check box content control. |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

### Examples

Shows how to work with styles for content control elements.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two ways to apply a style from the document to a structured document tag.
// 1 -  Apply a style object from the document's style collection:
let quoteStyle = doc.styles.at(aw.StyleIdentifier.Quote);
let sdtPlainText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Inline);
sdtPlainText.style = quoteStyle;

// 2 -  Reference a style in the document by name:
let sdtRichText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.RichText, aw.Markup.MarkupLevel.Inline);
sdtRichText.styleName = "Quote";

builder.insertNode(sdtPlainText);
builder.insertNode(sdtRichText);

expect(sdtPlainText.nodeType).toEqual(aw.NodeType.StructuredDocumentTag);

let tags = doc.getChildNodes(aw.NodeType.StructuredDocumentTag, true);

for (let node of tags)
{
  let sdt = node.asStructuredDocumentTag();

  console.log(sdt.wordOpenXMLMinimal);

  expect(sdt.style.styleIdentifier).toEqual(aw.StyleIdentifier.Quote);
  expect(sdt.styleName).toEqual("Quote");
}
```

### See Also

* module [Aspose.Words.Markup](../)
* class [CompositeNode](../../Aspose.Words/compositenode/)

