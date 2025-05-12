---
title: Document class
linktitle: Document class
articleTitle: Document class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Document class. Represents a Word document"
type: docs
weight: 310
url: /nodejs-net/aspose.words/document/
---

## Document class

Represents a Word document.
To learn more, visit the [Working with Document](https://docs.aspose.com/words/nodejs-net/working-with-document/) documentation article.




### Remarks

The **Document** is a central object in the Aspose.Words library.

To load an existing document in any of the [LoadFormat](../loadformat/) formats, pass a file name
or a stream into one of the **Document** constructors. To create a blank document, call the
constructor without parameters.

Use one of the Save method overloads to save the document in any of the
[SaveFormat](../saveformat/) formats.

Aspose.Words.Document.MailMerge is the Aspose.Words's reporting engine that allows to populate
reports designed in Microsoft Word with data from various data sources quickly and easily.

**Document** stores document-wide information such as [DocumentBase.styles](../documentbase/styles/),
[Document.builtInDocumentProperties](./builtInDocumentProperties/), [Document.customDocumentProperties](./customDocumentProperties/), lists and macros.
Most of these objects are accessible via the corresponding properties of the **Document**.

The **Document** is a root node of a tree that contains all other nodes of the document.
The tree is a Composite design pattern and in many ways similar to XmlDocument.
The content of the document can be manipulated freely programmatically:


* The nodes of the document can be accessed via typed collections, for example [Document.sections](./sections/),
  [ParagraphCollection](../paragraphcollection/) etc.
  
* The nodes of the document can be selected by their node type using
  [CompositeNode.getChildNodes()](../compositenode/getChildNodes/#nodetype_boolean)
  or using an XPath query with [CompositeNode.selectNodes()](../compositenode/selectNodes/#string) or [CompositeNode.selectSingleNode()](../compositenode/selectSingleNode/#string).
  
* Content nodes can be added or removed from anywhere in the document using
  [CompositeNode.insertBefore()](../compositenode/insertBefore/#node_node), [CompositeNode.insertAfter()](../compositenode/insertAfter/#node_node),
  [CompositeNode.removeChild()](../compositenode/removeChild/#node) and other
  methods provided by the base class [CompositeNode](../compositenode/).
  
* The formatting attributes of each node can be changed via the properties of that node.
  
Consider using [DocumentBuilder](../documentbuilder/) that simplifies the task of programmatically creating
or populating the document tree.

The **Document** can contain only [Section](../section/) objects.

In Microsoft Word, a valid document needs to have at least one section.




**Inheritance:** [Document](./) → [DocumentBase](../documentbase/) → [CompositeNode](../compositenode/) → [Node](../node/)

### Constructors
| Name | Description |
| --- | --- |
| [Document()](./constructor/#default) | Creates a blank Word document. |
| [Document(fileName)](./constructor/#string) | Opens an existing document from a file. Automatically detects the file format. |
| [Document(fileName, loadOptions)](./constructor/#string_loadoptions) | Opens an existing document from a file. Allows to specify additional options such as an encryption password. |
| [Document(stream)](./constructor/#buffer) | Opens an existing document from a stream. Automatically detects the file format. |
| [Document(stream, loadOptions)](./constructor/#buffer_loadoptions) | Opens an existing document from a stream. Allows to specify additional options such as an encryption password. |

### Properties

| Name | Description |
| --- | --- |
| [attachedTemplate](./attachedTemplate/) | Gets or sets the full path of the template attached to the document. |
| [automaticallyUpdateStyles](./automaticallyUpdateStyles/) | Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [backgroundShape](../documentbase/backgroundShape/) | Gets or sets the background shape of the document. Can be ``null``.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [bibliography](./bibliography/) | Gets the [Document.bibliography](./bibliography/) object that represents the list of sources available in the document. |
| [builtInDocumentProperties](./builtInDocumentProperties/) | Returns a collection that represents all the built-in document properties of the document. |
| [compatibilityOptions](./compatibilityOptions/) | Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word). |
| [compliance](./compliance/) | Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents. |
| [count](../compositenode/count/) | Gets the number of immediate children of this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [customDocumentProperties](./customDocumentProperties/) | Returns a collection that represents all the custom document properties of the document. |
| [customNodeId](../node/customNodeId/) | Specifies custom node identifier.<br>(Inherited from [Node](../node/)) |
| [customXmlParts](./customXmlParts/) | Gets or sets the collection of Custom XML Data Storage Parts. |
| [defaultTabStop](./defaultTabStop/) | Gets or sets the interval (in points) between the default tab stops. |
| [digitalSignatures](./digitalSignatures/) | Gets the collection of digital signatures for this document and their validation results. |
| [document](../node/document/) | Gets the document to which this node belongs.<br>(Inherited from [Node](../node/)) |
| [endnoteOptions](./endnoteOptions/) | Provides options that control numbering and positioning of endnotes in this document. |
| [fieldOptions](./fieldOptions/) | Gets a [FieldOptions](../../aspose.words.fields/fieldoptions/) object that represents options to control field handling in the document. |
| [firstChild](../compositenode/firstChild/) | Gets the first child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [firstSection](./firstSection/) | Gets the first section in the document. |
| [fontInfos](../documentbase/fontInfos/) | Provides access to properties of fonts used in this document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [fontSettings](./fontSettings/) | Gets or sets document font settings. |
| [footnoteOptions](./footnoteOptions/) | Provides options that control numbering and positioning of footnotes in this document. |
| [footnoteSeparators](../documentbase/footnoteSeparators/) | Provides access to the footnote/endnote separators defined in the document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [frameset](./frameset/) | Returns a [Document.frameset](./frameset/) instance if this document represents a frames page. |
| [glossaryDocument](./glossaryDocument/) | Gets or sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document. |
| [grammarChecked](./grammarChecked/) | Returns ``true`` if the document has been checked for grammar. |
| [hasChildNodes](../compositenode/hasChildNodes/) | Returns ``true`` if this node has any child nodes.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [hasMacros](./hasMacros/) | Returns ``true`` if the document has a VBA project (macros). |
| [hasRevisions](./hasRevisions/) | Returns ``true`` if the document has any tracked changes. |
| [hyphenationOptions](./hyphenationOptions/) | Provides access to document hyphenation options. |
| [includeTextboxesFootnotesEndnotesInStat](./includeTextboxesFootnotesEndnotesInStat/) | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| [isComposite](../node/isComposite/) | Returns ``true`` if this node can contain other nodes.<br>(Inherited from [Node](../node/)) |
| [justificationMode](./justificationMode/) | Gets or sets the character spacing adjustment of a document. |
| [lastChild](../compositenode/lastChild/) | Gets the last child of the node.<br>(Inherited from [CompositeNode](../compositenode/)) |
| [lastSection](./lastSection/) | Gets the last section in the document. |
| [layoutOptions](./layoutOptions/) | Gets a [LayoutOptions](../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document. |
| [lists](../documentbase/lists/) | Provides access to the list formatting used in the document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [mailMergeSettings](./mailMergeSettings/) | Gets or sets the object that contains all of the mail merge information for a document. |
| [nextSibling](../node/nextSibling/) | Gets the node immediately following this node.<br>(Inherited from [Node](../node/)) |
| [nodeChangingCallback](../documentbase/nodeChangingCallback/) | Called when a node is inserted or removed in the document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [nodeType](./nodeType/) | Returns [NodeType.Document](../nodetype/#Document). |
| [originalFileName](./originalFileName/) | Gets the original file name of the document. |
| [originalLoadFormat](./originalLoadFormat/) | Gets the format of the original document that was loaded into this object. |
| [packageCustomParts](./packageCustomParts/) | Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [pageColor](../documentbase/pageColor/) | Gets or sets the page color of the document. This property is a simpler version of [DocumentBase.backgroundShape](../documentbase/backgroundShape/).<br>(Inherited from [DocumentBase](../documentbase/)) |
| [pageCount](./pageCount/) | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [parentNode](../node/parentNode/) | Gets the immediate parent of this node.<br>(Inherited from [Node](../node/)) |
| [previousSibling](../node/previousSibling/) | Gets the node immediately preceding this node.<br>(Inherited from [Node](../node/)) |
| [protectionType](./protectionType/) | Gets the currently active document protection type. |
| [punctuationKerning](./punctuationKerning/) | Specifies whether kerning applies to both Latin text and punctuation. |
| [range](../node/range/) | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node.<br>(Inherited from [Node](../node/)) |
| [removePersonalInformation](./removePersonalInformation/) | Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [resourceLoadingCallback](../documentbase/resourceLoadingCallback/) | Allows to control how external resources are loaded.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [revisions](./revisions/) | Gets a collection of revisions (tracked changes) that exist in this document. |
| [revisionsView](./revisionsView/) | Gets or sets a value indicating whether to work with the original or revised version of a document. |
| [sections](./sections/) | Returns a collection that represents all sections in the document. |
| [shadeFormData](./shadeFormData/) | Specifies whether to turn on the gray shading on form fields. |
| [showGrammaticalErrors](./showGrammaticalErrors/) | Specifies whether to display grammar errors in this document. |
| [showSpellingErrors](./showSpellingErrors/) | Specifies whether to display spelling errors in this document. |
| [spellingChecked](./spellingChecked/) | Returns ``true`` if the document has been checked for spelling. |
| [styles](../documentbase/styles/) | Returns a collection of styles defined in the document.<br>(Inherited from [DocumentBase](../documentbase/)) |
| [theme](./theme/) | Gets the [Document.theme](./theme/) object for this document. |
| [trackRevisions](./trackRevisions/) | True if changes are tracked when this document is edited in Microsoft Word. |
| [variables](./variables/) | Returns the collection of variables added to a document or template. |
| [vbaProject](./vbaProject/) | Gets or sets a [Document.vbaProject](./vbaProject/). |
| [versionsCount](./versionsCount/) | Gets the number of document versions that was stored in the DOC document. |
| [viewOptions](./viewOptions/) | Provides options to control how the document is displayed in Microsoft Word. |
| [watermark](./watermark/) | Provides access to the document watermark. |
| [webExtensionTaskPanes](./webExtensionTaskPanes/) | Returns a collection that represents a list of task pane add-ins. |
| [writeProtection](./writeProtection/) | Provides access to the document write protection options. |

### Methods

| Name | Description |
| --- | --- |
|[ acceptAllRevisions()](./acceptAllRevisions/#default) | Accepts all tracked changes in the document. |
|[ appendChild(newChild)](../compositenode/appendChild/#node) | Adds the specified node to the end of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ appendDocument(srcDoc, importFormatMode)](./appendDocument/#document_importformatmode) | Appends the specified document to the end of this document. |
|[ appendDocument(srcDoc, importFormatMode, importFormatOptions)](./appendDocument/#document_importformatmode_importformatoptions) | Appends the specified document to the end of this document. |
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
|[ cleanup()](./cleanup/#default) | Cleans unused styles and lists from the document. |
|[ cleanup(options)](./cleanup/#cleanupoptions) | Cleans unused styles and lists from the document depending on given [CleanupOptions](../cleanupoptions/). |
|[ clone()](./clone/#default) | Performs a deep copy of the [Document](./). |
|[ compare(document, author, dateTime)](./compare/#document_string_date) | Compares this document with another document producing changes as number of edit and format revisions [Revision](../revision/). |
|[ compare(document, author, dateTime, options)](./compare/#document_string_date_compareoptions) | Compares this document with another document producing changes as a number of edit and format revisions [Revision](../revision/). Allows to specify comparison options using [CompareOptions](../../aspose.words.comparing/compareoptions/). |
|[ copyStylesFromTemplate(template)](./copyStylesFromTemplate/#string) | Copies styles from the specified template to a document. |
|[ copyStylesFromTemplate(template)](./copyStylesFromTemplate/#document) | Copies styles from the specified template to a document. |
|[ ensureMinimum()](./ensureMinimum/#default) | If the document contains no sections, creates one section with one paragraph. |
|[ expandTableStylesToDirectFormatting()](./expandTableStylesToDirectFormatting/#default) | Converts formatting specified in table styles into direct formatting on tables in the document. |
|[ extractPages(index, count)](./extractPages/#number_number) | Returns the [Document](./) object representing specified range of pages. |
|[ getAncestor(ancestorType)](../node/getAncestor/#nodetype) | Gets the first ancestor of the specified [NodeType](../nodetype/).<br>(Inherited from [Node](../node/)) |
|[ getBuildingBlock(index, isDeep)](../compositenode/getBuildingBlock/#number_boolean) | Returns an Nth child [BuildingBlock](../buildingblock/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChild(nodeType, index, isDeep)](../compositenode/getChild/#nodetype_number_boolean) | Returns an Nth child node that matches the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getChildNodes(nodeType, isDeep)](../compositenode/getChildNodes/#nodetype_boolean) | Returns a live collection of child nodes that match the specified type.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getComment(index, isDeep)](../compositenode/getComment/#number_boolean) | Returns an Nth child [Comment](../comment/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getEditableRangeStart(index, isDeep)](../compositenode/getEditableRangeStart/#number_boolean) | Returns an Nth child [EditableRangeStart](../editablerangestart/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getFootnote(index, isDeep)](../compositenode/getFootnote/#number_boolean) | Returns an Nth child [Footnote](../../aspose.words.notes/footnote/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getGroupShape(index, isDeep)](../compositenode/getGroupShape/#number_boolean) | Returns an Nth child [GroupShape](../../aspose.words.drawing/groupshape/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getOfficeMath(index, isDeep)](../compositenode/getOfficeMath/#number_boolean) | Returns an Nth child [OfficeMath](../../aspose.words.math/officemath/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getPageInfo(pageIndex)](./getPageInfo/#number) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
|[ getParagraph(index, isDeep)](../compositenode/getParagraph/#number_boolean) | Returns an Nth child [Paragraph](../paragraph/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getRun(index, isDeep)](../compositenode/getRun/#number_boolean) | Returns an Nth child [Run](../run/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdt(index, isDeep)](../compositenode/getSdt/#number_boolean) | Returns an Nth child [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeEnd(index, isDeep)](../compositenode/getSdtRangeEnd/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeEnd](../../aspose.words.markup/structureddocumenttagrangeend/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSdtRangeStart(index, isDeep)](../compositenode/getSdtRangeStart/#number_boolean) | Returns an Nth child [StructuredDocumentTagRangeStart](../../aspose.words.markup/structureddocumenttagrangestart/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getShape(index, isDeep)](../compositenode/getShape/#number_boolean) | Returns an Nth child [Shape](../../aspose.words.drawing/shape/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getSmartTag(index, isDeep)](../compositenode/getSmartTag/#number_boolean) | Returns an Nth child [SmartTag](../../aspose.words.markup/smarttag/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getTable(index, isDeep)](../compositenode/getTable/#number_boolean) | Returns an Nth child [Table](../table/) node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ getText()](../node/getText/#default) | Gets the text of this node and of all its children.<br>(Inherited from [Node](../node/)) |
|[ importNode(srcNode, isImportChildren)](../documentbase/importNode/#node_boolean) | Imports a node from another document to the current document.<br>(Inherited from [DocumentBase](../documentbase/)) |
|[ importNode(srcNode, isImportChildren, importFormatMode)](../documentbase/importNode/#node_boolean_importformatmode) | Imports a node from another document to the current document with an option to control formatting.<br>(Inherited from [DocumentBase](../documentbase/)) |
|[ indexOf(child)](../compositenode/indexOf/#node) | Returns the index of the specified child node in the child node array.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertAfter(newChild, refChild)](../compositenode/insertAfter/#node_node) | Inserts the specified node immediately after the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ insertBefore(newChild, refChild)](../compositenode/insertBefore/#node_node) | Inserts the specified node immediately before the specified reference node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ joinRunsWithSameFormatting()](./joinRunsWithSameFormatting/#default) | Joins runs with same formatting in all paragraphs of the document. |
|[ nextPreOrder(rootNode)](../node/nextPreOrder/#node) | Gets next node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ nodeTypeToString(nodeType)](../node/nodeTypeToString/#nodetype) | A utility method that converts a node type enum value into a user friendly string.<br>(Inherited from [Node](../node/)) |
|[ normalizeFieldTypes()](./normalizeFieldTypes/#default) | Changes field type values [FieldChar.fieldType](../../aspose.words.fields/fieldchar/fieldType/) of [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes. |
|[ prependChild(newChild)](../compositenode/prependChild/#node) | Adds the specified node to the beginning of the list of child nodes for this node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ previousPreOrder(rootNode)](../node/previousPreOrder/#node) | Gets the previous node according to the pre-order tree traversal algorithm.<br>(Inherited from [Node](../node/)) |
|[ protect(type)](./protect/#protectiontype) | Protects the document from changes without changing the existing password or assigns a random password. |
|[ protect(type, password)](./protect/#protectiontype_string) | Protects the document from changes and optionally sets a protection password. |
|[ referenceEquals(other)](../node/referenceEquals/#node) | <br>(Inherited from [Node](../node/)) |
|[ remove()](../node/remove/#default) | Removes itself from the parent.<br>(Inherited from [Node](../node/)) |
|[ removeAllChildren()](../compositenode/removeAllChildren/#default) | Removes all the child nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeBlankPages()](./removeBlankPages/#default) | Removes blank pages from the document. |
|[ removeChild(oldChild)](../compositenode/removeChild/#node) | Removes the specified child node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ removeExternalSchemaReferences()](./removeExternalSchemaReferences/#default) | Removes external XML schema references from this document. |
|[ removeMacros()](./removeMacros/#default) | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
|[ removeSmartTags()](../compositenode/removeSmartTags/#default) | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ save(stream, saveFormat)](./save/#unknown_saveformat) | Saves the document to a stream using the specified format. |
|[ save(stream, saveOptions)](./save/#unknown_saveoptions) | Saves the document to a stream using the specified save options. |
|[ save(fileName)](./save/#string) | Saves the document to a file. Automatically determines the save format from the extension. |
|[ save(fileName, saveFormat)](./save/#string_saveformat) | Saves the document to a file in the specified format. |
|[ save(fileName, saveOptions)](./save/#string_saveoptions) | Saves the document to a file using the specified save options. |
|[ selectNodes(xpath)](../compositenode/selectNodes/#string) | Selects a list of nodes matching the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ selectSingleNode(xpath)](../compositenode/selectSingleNode/#string) | Selects the first [Node](../node/) that matches the XPath expression.<br>(Inherited from [CompositeNode](../compositenode/)) |
|[ startTrackRevisions(author, dateTime)](./startTrackRevisions/#string_date) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
|[ startTrackRevisions(author)](./startTrackRevisions/#string) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
|[ stopTrackRevisions()](./stopTrackRevisions/#default) | Stops automatic marking of document changes as revisions. |
|[ toString(saveFormat)](../node/toString/#saveformat) | Exports the content of the node into a string in the specified format.<br>(Inherited from [Node](../node/)) |
|[ toString(saveOptions)](../node/toString/#saveoptions) | Exports the content of the node into a string using the specified save options.<br>(Inherited from [Node](../node/)) |
|[ unlinkFields()](./unlinkFields/#default) | Unlinks fields in the whole document. |
|[ unprotect()](./unprotect/#default) | Removes protection from the document regardless of the password. |
|[ unprotect(password)](./unprotect/#string) | Removes protection from the document if a correct password is specified. |
|[ updateActualReferenceMarks()](./updateActualReferenceMarks/#default) | Updates the [Footnote.actualReferenceMark](../../aspose.words.notes/footnote/actualReferenceMark/) property of all footnotes and endnotes in the document. |
|[ updateFields()](./updateFields/#default) | Updates the values of fields in the whole document. |
|[ updateListLabels()](./updateListLabels/#default) | Updates list labels for all list items in the document. |
|[ updatePageLayout()](./updatePageLayout/#default) | Rebuilds the page layout of the document. |
|[ updateThumbnail(options)](./updateThumbnail/#thumbnailgeneratingoptions) | Updates [BuiltInDocumentProperties.thumbnail](../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document according to the specified options. |
|[ updateThumbnail()](./updateThumbnail/#default) | Updates [BuiltInDocumentProperties.thumbnail](../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document using default options. |
|[ updateWordCount()](./updateWordCount/#default) | Updates word count properties of the document. |
|[ updateWordCount(updateLinesCount)](./updateWordCount/#boolean) | Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.lines](../../aspose.words.properties/builtindocumentproperties/lines/) property. |

### Examples

Shows how to execute a mail merge with data from a DataTable.

```js
test('ExecuteDataTable', () => {
  let table = new DataTable("Test");
  table.columns.add("CustomerName");
  table.columns.add("Address");
  table.rows.add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
  table.rows.add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

  // Below are two ways of using a DataTable as the data source for a mail merge.
  // 1 -  Use the entire table for the mail merge to create one output mail merge document for every row in the table:
  let doc = CreateSourceDocExecuteDataTable();

  doc.mailMerge.execute(table);

  doc.save(base.artifactsDir + "MailMerge.ExecuteDataTable.wholeTable.docx");

  // 2 -  Use one row of the table to create one output mail merge document:
  doc = CreateSourceDocExecuteDataTable();

  doc.mailMerge.execute(table.rows.at(1));

  doc.save(base.artifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
});


  /// <summary>
  /// Creates a mail merge source document.
  /// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
  let doc = new aw.Document();
  let builder = new aw.DocumentBuilder(doc);

  builder.insertField(" MERGEFIELD CustomerName ");
  builder.insertParagraph();
  builder.insertField(" MERGEFIELD Address ");

  return doc;
}
```

### See Also

* module [Aspose.Words](../)
* class [DocumentBase](../documentbase/)

