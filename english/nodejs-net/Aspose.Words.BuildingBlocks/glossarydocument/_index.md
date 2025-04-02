---
title: GlossaryDocument class
linktitle: GlossaryDocument class
articleTitle: GlossaryDocument class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.BuildingBlocks.GlossaryDocument class. Represents the root element for a glossary document within a Word document"
type: docs
weight: 50
url: /nodejs-net/Aspose.Words.BuildingBlocks/glossarydocument/
---

## GlossaryDocument class

Represents the root element for a glossary document within a Word document.
A glossary document is a storage for AutoText, AutoCorrect entries and Building Blocks.
To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/nodejs-net/aspose-words-document-object-model/) documentation article.




### Remarks

Some documents, usually templates, can contain AutoText, AutoCorrect entries
and/or Building Blocks (also known as *glossary document entries*, *document parts*
or *building blocks*).

To access building blocks, you need to load a document into a [Document](../../Aspose.Words/document/)
object. Building blocks will be available via the [Document.glossaryDocument](../../Aspose.Words/document/glossaryDocument/) property.

[GlossaryDocument](./) can contain any number of [BuildingBlock](../../Aspose.Words/buildingblock/) objects.
Each [BuildingBlock](../../Aspose.Words/buildingblock/) represents one document part.

Corresponds to the **glossaryDocument** and **docParts** elements in OOXML.




**Inheritance:** [GlossaryDocument](./) → [DocumentBase](../../Aspose.Words/documentbase/) → [CompositeNode](../../Aspose.Words/compositenode/) → [Node](../../Aspose.Words/node/)

### Constructors
| Name | Description |
| --- | --- |
| [GlossaryDocument()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [backgroundShape](../../Aspose.Words/documentbase/backgroundShape/) | Gets or sets the background shape of the document. Can be ``None``.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [buildingBlocks](./buildingBlocks/) | Returns a typed collection that represents all building blocks in the glossary document. |
| [count](../../Aspose.Words/compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [customNodeId](../../Aspose.Words/node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [document](../../Aspose.Words/node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [firstBuildingBlock](./firstBuildingBlock/) | Gets the first building block in the glossary document. |
| [firstChild](../../Aspose.Words/compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [fontInfos](../../Aspose.Words/documentbase/fontInfos/) | Provides access to properties of fonts used in this document.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [footnoteSeparators](../../Aspose.Words/documentbase/footnoteSeparators/) | Provides access to the footnote/endnote separators defined in the document.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [hasChildNodes](../../Aspose.Words/compositenode/hasChildNodes/) | Returns ``True`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [isComposite](../../Aspose.Words/node/isComposite/) | Returns ``True`` if this node can contain other nodes.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [lastBuildingBlock](./lastBuildingBlock/) | Gets the last building block in the glossary document. |
| [lastChild](../../Aspose.Words/compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
| [lists](../../Aspose.Words/documentbase/lists/) | Provides access to the list formatting used in the document.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [nextSibling](../../Aspose.Words/node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [nodeChangingCallback](../../Aspose.Words/documentbase/nodeChangingCallback/) | Called when a node is inserted or removed in the document.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [nodeType](./nodeType/) | Returns the [NodeType.GlossaryDocument](../../Aspose.Words/nodetype/#GlossaryDocument) value. |
| [pageColor](../../Aspose.Words/documentbase/pageColor/) | Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.backgroundShape](../../Aspose.Words/documentbase/backgroundShape/).<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [parentNode](../../Aspose.Words/node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [previousSibling](../../Aspose.Words/node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [range](../../Aspose.Words/node/range/) | Returns a [Range](../../Aspose.Words/range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
| [resourceLoadingCallback](../../Aspose.Words/documentbase/resourceLoadingCallback/) | Allows to control how external resources are loaded.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [styles](../../Aspose.Words/documentbase/styles/) | Returns a collection of styles defined in the document.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
| [warningCallback](../../Aspose.Words/documentbase/warningCallback/) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ accept(visitor)](./accept/#documentvisitor) | Accepts a visitor. |
|[ acceptEnd(visitor)](./acceptEnd/#documentvisitor) | Accepts a visitor for visiting the end of the Glossary document. |
|[ acceptStart(visitor)](./acceptStart/#documentvisitor) | Accepts a visitor for visiting the start of the Glossary document. |
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
|[ asGlossaryDocument()](../../Aspose.Words/node/asGlossaryDocument/#default) | Cast node to [GlossaryDocument](./).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asGroupShape()](../../Aspose.Words/node/asGroupShape/#default) | Cast node to [GroupShape](../../Aspose.Words.Drawing/groupshape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asHeaderFooter()](../../Aspose.Words/node/asHeaderFooter/#default) | Cast node to [HeaderFooter](../../Aspose.Words/headerfooter/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asOfficeMath()](../../Aspose.Words/node/asOfficeMath/#default) | Cast node to [OfficeMath](../../Aspose.Words.Math/officemath/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asParagraph()](../../Aspose.Words/node/asParagraph/#default) | Cast node to [Paragraph](../../Aspose.Words/paragraph/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRow()](../../Aspose.Words/node/asRow/#default) | Cast node to [Row](../../Aspose.Words.Tables/row/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asRun()](../../Aspose.Words/node/asRun/#default) | Cast node to [Run](../../Aspose.Words/run/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSection()](../../Aspose.Words/node/asSection/#default) | Cast node to [Section](../../Aspose.Words/section/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asShape()](../../Aspose.Words/node/asShape/#default) | Cast node to [Shape](../../Aspose.Words.Drawing/shape/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSmartTag()](../../Aspose.Words/node/asSmartTag/#default) | Cast node to [SmartTag](../../Aspose.Words.Markup/smarttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSpecialChar()](../../Aspose.Words/node/asSpecialChar/#default) | Cast node to [SpecialChar](../../Aspose.Words/specialchar/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTag()](../../Aspose.Words/node/asStructuredDocumentTag/#default) | Cast node to [StructuredDocumentTag](../../Aspose.Words.Markup/structureddocumenttag/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeEnd()](../../Aspose.Words/node/asStructuredDocumentTagRangeEnd/#default) | Cast node to [StructuredDocumentTagRangeEnd](../../Aspose.Words.Markup/structureddocumenttagrangeend/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asStructuredDocumentTagRangeStart()](../../Aspose.Words/node/asStructuredDocumentTagRangeStart/#default) | Cast node to [StructuredDocumentTagRangeStart](../../Aspose.Words.Markup/structureddocumenttagrangestart/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asSubDocument()](../../Aspose.Words/node/asSubDocument/#default) | Cast node to [SubDocument](../../Aspose.Words/subdocument/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ asTable()](../../Aspose.Words/node/asTable/#default) | Cast node to [Table](../../Aspose.Words/table/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ clone(isCloneChildren)](../../Aspose.Words/node/clone/#boolean) | Creates a duplicate of the node.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getAncestor(ancestorType)](../../Aspose.Words/node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../../Aspose.Words/nodetype/).<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ getBuildingBlock(gallery, category, name)](./getBuildingBlock/#buildingblockgallery_string_string) | Finds a building block using the specified gallery, category and name. |
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
|[ importNode(srcNode, isImportChildren)](../../Aspose.Words/documentbase/importNode/#node_boolean) | Imports a node from another document to the current document.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
|[ importNode(srcNode, isImportChildren, importFormatMode)](../../Aspose.Words/documentbase/importNode/#node_boolean_importformatmode) | Imports a node from another document to the current document with an option to control formatting.<br>(Inherited from [DocumentBase](../../Aspose.Words/documentbase/)) |
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
|[ removeSmartTags()](../../Aspose.Words/compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../Aspose.Words.Markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectNodes(xpath)](../../Aspose.Words/compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ selectSingleNode(xpath)](../../Aspose.Words/compositenode/selectSingleNode/#string) | Selects the first [Node](../../Aspose.Words/node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../../Aspose.Words/compositenode/)) |
|[ toString(saveFormat)](../../Aspose.Words/node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../../Aspose.Words/node/)) |
|[ toString(saveOptions)](../../Aspose.Words/node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../../Aspose.Words/node/)) |

### See Also

* module [Aspose.Words.BuildingBlocks](../)
* class [DocumentBase](../../Aspose.Words/documentbase/)
* class [Document](../../Aspose.Words/document/)
* property [Document.glossaryDocument](../../Aspose.Words/document/glossaryDocument/)
* class [BuildingBlock](../../Aspose.Words/buildingblock/)

