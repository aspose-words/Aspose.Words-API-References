---
title: GlossaryDocument class
linktitle: GlossaryDocument class
articleTitle: GlossaryDocument class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.BuildingBlocks.GlossaryDocument class. Represents the root element for a glossary document within a Word document"
type: docs
weight: 50
url: /nodejs-net/aspose.words.buildingblocks/glossarydocument/
---

## GlossaryDocument class

Represents the root element for a glossary document within a Word document.
A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

Some documents, usually templates, can contain AutoText, AutoCorrect entries
and/or Building Blocks (also known as *glossary document entries*, *document parts*
or *building blocks*).

To access building blocks, you need to load a document into a [Document](../../aspose.words/document/)
object. Building blocks will be available via the [Document.glossaryDocument](../../aspose.words/document/glossaryDocument/) property.

[GlossaryDocument](./) can contain any number of [BuildingBlock](../../aspose.words/buildingblock/) objects.
Each [BuildingBlock](../../aspose.words/buildingblock/) represents one document part.

Corresponds to the **glossaryDocument** and **docParts** elements in OOXML.




**Inheritance:** [GlossaryDocument](./) → [DocumentBase](../../aspose.words/documentbase/) → [CompositeNode](../../aspose.words/compositenode/) → [Node](../../aspose.words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [GlossaryDocument()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [backgroundShape](../../aspose.words/documentbase/backgroundShape/) | Gets or sets the background shape of the document. Can be ``null``.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [buildingBlocks](./buildingBlocks/) | Returns a typed collection that represents all building blocks in the glossary document. |
| [count](../../aspose.words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [customNodeId](../../aspose.words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [document](../../aspose.words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [firstBuildingBlock](./firstBuildingBlock/) | Gets the first building block in the glossary document. |
| [firstChild](../../aspose.words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [fontInfos](../../aspose.words/documentbase/fontInfos/) | Provides access to properties of fonts used in this document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [footnoteSeparators](../../aspose.words/documentbase/footnoteSeparators/) | Provides access to the footnote/endnote separators defined in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [hasChildNodes](../../aspose.words/compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [isComposite](../../aspose.words/node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [lastBuildingBlock](./lastBuildingBlock/) | Gets the last building block in the glossary document. |
| [lastChild](../../aspose.words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
| [lists](../../aspose.words/documentbase/lists/) | Provides access to the list formatting used in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [nextSibling](../../aspose.words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [nodeChangingCallback](../../aspose.words/documentbase/nodeChangingCallback/) | Called when a node is inserted or removed in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [nodeType](./nodeType/) | Returns the [NodeType.GlossaryDocument](../../aspose.words/nodetype/#GlossaryDocument) value. |
| [pageColor](../../aspose.words/documentbase/pageColor/) | Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.backgroundShape](../../aspose.words/documentbase/backgroundShape/).<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [parentNode](../../aspose.words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [previousSibling](../../aspose.words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [range](../../aspose.words/node/range/) | Returns a [Range](../../aspose.words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../aspose.words/node/)) |
| [resourceLoadingCallback](../../aspose.words/documentbase/resourceLoadingCallback/) | Allows to control how external resources are loaded.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
| [styles](../../aspose.words/documentbase/styles/) | Returns a collection of styles defined in the document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ appendChild(newChild)](../../aspose.words/compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ asBody()](../../aspose.words/node/asBody/#default) | Cast node to [Body](../../aspose.words/body/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkEnd()](../../aspose.words/node/asBookmarkEnd/#default) | Cast node to [BookmarkEnd](../../aspose.words/bookmarkend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBookmarkStart()](../../aspose.words/node/asBookmarkStart/#default) | Cast node to [BookmarkStart](../../aspose.words/bookmarkstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asBuildingBlock()](../../aspose.words/node/asBuildingBlock/#default) | Cast node to [BuildingBlock](../../aspose.words/buildingblock/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCell()](../../aspose.words/node/asCell/#default) | Cast node to [Cell](../../aspose.words.tables/cell/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asComment()](../../aspose.words/node/asComment/#default) | Cast node to [Comment](../../aspose.words/comment/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeEnd()](../../aspose.words/node/asCommentRangeEnd/#default) | Cast node to [CommentRangeEnd](../../aspose.words/commentrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCommentRangeStart()](../../aspose.words/node/asCommentRangeStart/#default) | Cast node to [CommentRangeStart](../../aspose.words/commentrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asCompositeNode()](../../aspose.words/node/asCompositeNode/#default) | Cast node to [CompositeNode](../../aspose.words/compositenode/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asDocument()](../../aspose.words/node/asDocument/#default) | Cast node to [Node.document](../../aspose.words/node/document/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeEnd()](../../aspose.words/node/asEditableRangeEnd/#default) | Cast node to [EditableRangeEnd](../../aspose.words/editablerangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asEditableRangeStart()](../../aspose.words/node/asEditableRangeStart/#default) | Cast node to [EditableRangeStart](../../aspose.words/editablerangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldEnd()](../../aspose.words/node/asFieldEnd/#default) | Cast node to [FieldEnd](../../aspose.words.fields/fieldend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldSeparator()](../../aspose.words/node/asFieldSeparator/#default) | Cast node to [FieldSeparator](../../aspose.words.fields/fieldseparator/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFieldStart()](../../aspose.words/node/asFieldStart/#default) | Cast node to [FieldStart](../../aspose.words.fields/fieldstart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFootnote()](../../aspose.words/node/asFootnote/#default) | Cast node to [Footnote](../../aspose.words.notes/footnote/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asFormField()](../../aspose.words/node/asFormField/#default) | Cast node to [FormField](../../aspose.words.fields/formfield/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGlossaryDocument()](../../aspose.words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](./).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asGroupShape()](../../aspose.words/node/asGroupShape/#default) | Cast node to [GroupShape](../../aspose.words.drawing/groupshape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asHeaderFooter()](../../aspose.words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../aspose.words/headerfooter/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asOfficeMath()](../../aspose.words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../aspose.words.math/officemath/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asParagraph()](../../aspose.words/node/asParagraph/#default) | Cast node to [Paragraph](../../aspose.words/paragraph/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRow()](../../aspose.words/node/asRow/#default) | Cast node to [Row](../../aspose.words.tables/row/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asRun()](../../aspose.words/node/asRun/#default) | Cast node to [Run](../../aspose.words/run/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSection()](../../aspose.words/node/asSection/#default) | Cast node to [Section](../../aspose.words/section/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asShape()](../../aspose.words/node/asShape/#default) | Cast node to [Shape](../../aspose.words.drawing/shape/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSmartTag()](../../aspose.words/node/asSmartTag/#default) | Cast node to [SmartTag](../../aspose.words.markup/smarttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSpecialChar()](../../aspose.words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../aspose.words/specialchar/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTag()](../../aspose.words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../aspose.words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../aspose.words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asSubDocument()](../../aspose.words/node/asSubDocument/#default) | Cast node to [SubDocument](../../aspose.words/subdocument/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ asTable()](../../aspose.words/node/asTable/#default) | Cast node to [Table](../../aspose.words/table/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ clone(isCloneChildren)](../../aspose.words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getAncestor(ancestorType)](../../aspose.words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../aspose.words/nodetype/).<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ getBuildingBlock(gallery, category, name)](./getBuildingBlock/#buildingblockgallery_string_string) | Finds a building block using the specified gallery, category and name. |
|[ getChild(nodeType, index, isDeep)](../../aspose.words/compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../../aspose.words/compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getComment(index, isDeep)](../../aspose.words/compositenode/getComment/#number_boolean) | Returns an Nth child [Comment](../../aspose.words/comment/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../../aspose.words/compositenode/getEditableRangeStart/#number_boolean) | Returns an Nth child [EditableRangeStart](../../aspose.words/editablerangestart/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getFootnote(index, isDeep)](../../aspose.words/compositenode/getFootnote/#number_boolean) | Returns an Nth child [Footnote](../../aspose.words.notes/footnote/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getGroupShape(index, isDeep)](../../aspose.words/compositenode/getGroupShape/#number_boolean) | Returns an Nth child [GroupShape](../../aspose.words.drawing/groupshape/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getOfficeMath(index, isDeep)](../../aspose.words/compositenode/getOfficeMath/#number_boolean) | Returns an Nth child [OfficeMath](../../aspose.words.math/officemath/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getParagraph(index, isDeep)](../../aspose.words/compositenode/getParagraph/#number_boolean) | Returns an Nth child [Paragraph](../../aspose.words/paragraph/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getRun(index, isDeep)](../../aspose.words/compositenode/getRun/#number_boolean) | Returns an Nth child [Run](../../aspose.words/run/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSdt(index, isDeep)](../../aspose.words/compositenode/getSdt/#number_boolean) | Returns an Nth child [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../../aspose.words/compositenode/getSdtRangeEnd/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../../aspose.words/compositenode/getSdtRangeStart/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getShape(index, isDeep)](../../aspose.words/compositenode/getShape/#number_boolean) | Returns an Nth child [Shape](../../aspose.words.drawing/shape/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getSmartTag(index, isDeep)](../../aspose.words/compositenode/getSmartTag/#number_boolean) | Returns an Nth child [SmartTag](../../aspose.words.markup/smarttag/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getTable(index, isDeep)](../../aspose.words/compositenode/getTable/#number_boolean) | Returns an Nth child [Table](../../aspose.words/table/) node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ getText()](../../aspose.words/node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ importNode(srcNode, isImportChildren)](../../aspose.words/documentbase/importNode/#node_boolean) | Imports a node from another document to the current document.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
|[ importNode(srcNode, isImportChildren, importFormatMode)](../../aspose.words/documentbase/importNode/#node_boolean_importformatmode) | Imports a node from another document to the current document with an option to control formatting.<br>(Inherited from [DocumentBase](../../aspose.words/documentbase/)) |
|[ indexOf(child)](../../aspose.words/compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertAfter(newChild, refChild)](../../aspose.words/compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ insertBefore(newChild, refChild)](../../aspose.words/compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ nextPreOrder(rootNode)](../../aspose.words/node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ nodeTypeToString(nodeType)](../../aspose.words/node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ prependChild(newChild)](../../aspose.words/compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ previousPreOrder(rootNode)](../../aspose.words/node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ referenceEquals(other)](../../aspose.words/node/referenceEquals/#node) | <br>(Inherited from [Node](../../aspose.words/node/)) |
|[ remove()](../../aspose.words/node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ removeAllChildren()](../../aspose.words/compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ removeChild(oldChild)](../../aspose.words/compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ removeSmartTags()](../../aspose.words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ selectNodes(xpath)](../../aspose.words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ selectSingleNode(xpath)](../../aspose.words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../aspose.words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../aspose.words/compositenode/)) |
|[ toString(saveFormat)](../../aspose.words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../aspose.words/node/)) |
|[ toString(saveOptions)](../../aspose.words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../aspose.words/node/)) |

### See Also

* module [Aspose.Words.BuildingBlocks](../)
* class [DocumentBase](../../aspose.words/documentbase/)
* class [Document](../../aspose.words/document/)
* property [Document.glossaryDocument](../../aspose.words/document/glossaryDocument/)
* class [BuildingBlock](../../aspose.words/buildingblock/)

