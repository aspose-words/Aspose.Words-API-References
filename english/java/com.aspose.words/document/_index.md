---
title: Document
linktitle: Document
second_title: Aspose.Words for Java
description: Represents a Word document in Java.
type: docs
weight: 148
url: /java/com.aspose.words/document/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/), [com.aspose.words.DocumentBase](../../com.aspose.words/documentbase/)
```
public class Document extends DocumentBase
```

Represents a Word document.

To learn more, visit the [ Working with Document ][Working with Document] documentation article.

 **Remarks:** 

The [Document](../../com.aspose.words/document/) is a central object in the Aspose.Words library.

To load an existing document in any of the [LoadFormat](../../com.aspose.words/loadformat/) formats, pass a file name or a stream into one of the [Document](../../com.aspose.words/document/) constructors. To create a blank document, call the constructor without parameters.

Use one of the Save method overloads to save the document in any of the [SaveFormat](../../com.aspose.words/saveformat/) formats.

To draw document pages directly onto a **Graphics** object use [renderToScale(int, java.awt.Graphics2D, float, float, float)](../../com.aspose.words/document/\#renderToScale-int--java.awt.Graphics2D--float--float--float) or [renderToSize(int, java.awt.Graphics2D, float, float, float, float)](../../com.aspose.words/document/\#renderToSize-int--java.awt.Graphics2D--float--float--float--float) method.

To print the document, use one of the [print(java.lang.String)](../../com.aspose.words/document/\#print-java.lang.String) methods.

[getMailMerge()](../../com.aspose.words/document/\#getMailMerge) is the Aspose.Words's reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a java.sql.ResultSet or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](../../com.aspose.words/document/) stores document-wide information such as [DocumentBase.getStyles()](../../com.aspose.words/documentbase/\#getStyles), [getBuiltInDocumentProperties()](../../com.aspose.words/document/\#getBuiltInDocumentProperties), [getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](../../com.aspose.words/document/).

The [Document](../../com.aspose.words/document/) is a root node of a tree that contains all other nodes of the document. The tree is a Composite design pattern and in many ways similar to XmlDocument. The content of the document can be manipulated freely programmatically:

 *  The nodes of the document can be accessed via typed collections, for example [getSections()](../../com.aspose.words/document/\#getSections), [ParagraphCollection](../../com.aspose.words/paragraphcollection/) etc.
 *  The nodes of the document can be selected by their node type using **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** or using an XPath query with [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode/\#selectNodes-java.lang.String) or [CompositeNode.selectSingleNode(java.lang.String)](../../com.aspose.words/compositenode/\#selectSingleNode-java.lang.String).
 *  Content nodes can be added or removed from anywhere in the document using **M:Aspose.Words.CompositeNode.InsertBefore1(0,Aspose.Words.Node)**, **M:Aspose.Words.CompositeNode.InsertAfter1(0,Aspose.Words.Node)**, **M:Aspose.Words.CompositeNode.RemoveChild1(0)** and other methods provided by the base class [CompositeNode](../../com.aspose.words/compositenode/).
 *  The formatting attributes of each node can be changed via the properties of that node.

Consider using [DocumentBuilder](../../com.aspose.words/documentbuilder/) that simplifies the task of programmatically creating or populating the document tree.

The [Document](../../com.aspose.words/document/) can contain only [Section](../../com.aspose.words/section/) objects.

In Microsoft Word, a valid document needs to have at least one section.

 **Examples:** 

Shows how to execute a mail merge with data from a DataTable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // This example creates a table, but you would normally load table from a database
 DataTable table = new DataTable("Test");
 table.getColumns().add("CustomerName");
 table.getColumns().add("Address");
 table.getRows().add("Thomas Hardy", "120 Hanover Sq., London");
 table.getRows().add("Paolo Accorti", "Via Monte Bianco 34, Torino");

 // Field values from the table are inserted into the mail merge fields found in the document
 doc.getMailMerge().execute(table);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.docx");

 // Create a copy of our document to perform another mail merge
 doc = new Document();
 builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // We can also source values for a mail merge from a single row in the table
 doc.getMailMerge().execute(table.getRows().get(1));

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.OneRow.docx");
 
```


[Working with Document]: https://docs.aspose.com/words/java/working-with-document/
## Constructors

| Constructor | Description |
| --- | --- |
| [Document()](#Document) | Creates or loads a document. |
| [Document(String fileName)](#Document-java.lang.String) | Opens an existing document from a file. |
| [Document(String fileName, LoadOptions loadOptions)](#Document-java.lang.String-com.aspose.words.LoadOptions) | Opens an existing document from a file. |
| [Document(InputStream stream)](#Document-java.io.InputStream) | Initializes a new instance of this class. |
| [Document(InputStream stream, LoadOptions loadOptions)](#Document-java.io.InputStream-com.aspose.words.LoadOptions) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor) | Accepts a visitor. |
| [acceptAllRevisions()](#acceptAllRevisions) | Accepts all tracked changes in the document. |
| [acceptEnd(DocumentVisitor visitor)](#acceptEnd-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the end of the document. |
| [acceptStart(DocumentVisitor visitor)](#acceptStart-com.aspose.words.DocumentVisitor) | Accepts a visitor for visiting the start of the document. |
| [add(Shape watermark)](#add-com.aspose.words.Shape) |  |
| [appendDocument(Document srcDoc, int importFormatMode)](#appendDocument-com.aspose.words.Document-int) |  |
| [appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions) |  |
| [cleanup()](#cleanup) | Cleans unused styles and lists from the document. |
| [cleanup(CleanupOptions options)](#cleanup-com.aspose.words.CleanupOptions) | Cleans unused styles and lists from the document depending on given [CleanupOptions](../../com.aspose.words/cleanupoptions/). |
| [clearSectionAttrs()](#clearSectionAttrs) |  |
| [compare(Document document, String author, Date dateTime)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date) | Compares this document with another document producing changes as number of edit and format revisions [Revision](../../com.aspose.words/revision/). |
| [compare(Document document, String author, Date dateTime, CompareOptions options)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../com.aspose.words/revision/). |
| [copyStylesFromTemplate(Document template)](#copyStylesFromTemplate-com.aspose.words.Document) | Copies styles from the specified template to a document. |
| [copyStylesFromTemplate(String template)](#copyStylesFromTemplate-java.lang.String) | Copies styles from the specified template to a document. |
| [dd()](#dd) |  |
| [deepClone()](#deepClone) | Performs a deep copy of the [Document](../../com.aspose.words/document/). |
| [deepClone(boolean isCloneChildren)](#deepClone-boolean) | Creates a duplicate of the node. |
| [ensureMinimum()](#ensureMinimum) | If the document contains no sections, creates one section with one paragraph. |
| [expandTableStylesToDirectFormatting()](#expandTableStylesToDirectFormatting) | Converts formatting specified in table styles into direct formatting on tables in the document. |
| [extractPages(int index, int count)](#extractPages-int-int) | Returns the [Document](../../com.aspose.words/document/) object representing specified range of pages. |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int) |  |
| [get()](#get) |  |
| [getAncestor(int ancestorType)](#getAncestor-int) |  |
| [getAncestor(Class ancestorType)](#getAncestor-java.lang.Class) | Gets the first ancestor of the specified object type. |
| [getAttachedTemplate()](#getAttachedTemplate) | Gets the full path of the template attached to the document. |
| [getAutomaticallyUpdateStyles()](#getAutomaticallyUpdateStyles) | Gets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [getBackgroundShape()](#getBackgroundShape) | Gets the background shape of the document. |
| [getBibliography()](#getBibliography) | Gets the [getBibliography()](../../com.aspose.words/document/\#getBibliography) object that represents the list of sources available in the document. |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | Returns a collection that represents all the built-in document properties of the document. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getCompatibilityOptions()](#getCompatibilityOptions) | Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word). |
| [getCompliance()](#getCompliance) | Gets the OOXML compliance version determined from the loaded document content. |
| [getContainer()](#getContainer) |  |
| [getCount()](#getCount) | Gets the number of immediate children of this node. |
| [getCurrentNode()](#getCurrentNode) |  |
| [getCustomDocumentProperties()](#getCustomDocumentProperties) | Returns a collection that represents all the custom document properties of the document. |
| [getCustomNodeId()](#getCustomNodeId) | Specifies custom node identifier. |
| [getCustomXmlParts()](#getCustomXmlParts) | Gets the collection of Custom XML Data Storage Parts. |
| [getDefaultTabStop()](#getDefaultTabStop) | Gets the interval (in points) between the default tab stops. |
| [getDigitalSignatures()](#getDigitalSignatures) | Gets the collection of digital signatures for this document and their validation results. |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int) |  |
| [getDocument()](#getDocument) | Gets this instance. |
| [getEndnoteOptions()](#getEndnoteOptions) | Provides options that control numbering and positioning of endnotes in this document. |
| [getFieldOptions()](#getFieldOptions) | Gets a [FieldOptions](../../com.aspose.words/fieldoptions/) object that represents options to control field handling in the document. |
| [getFirstChild()](#getFirstChild) | Gets the first child of the node. |
| [getFirstSection()](#getFirstSection) | Gets the first section in the document. |
| [getFontInfos()](#getFontInfos) | Provides access to properties of fonts used in this document. |
| [getFontSettings()](#getFontSettings) | Gets document font settings. |
| [getFootnoteOptions()](#getFootnoteOptions) | Provides options that control numbering and positioning of footnotes in this document. |
| [getFrameset()](#getFrameset) | Returns a [getFrameset()](../../com.aspose.words/document/\#getFrameset) instance if this document represents a frames page. |
| [getGlossaryDocument()](#getGlossaryDocument) | Gets the glossary document within this document or template. |
| [getGrammarChecked()](#getGrammarChecked) | Returns  true  if the document has been checked for grammar. |
| [getHyphenationOptions()](#getHyphenationOptions) | Provides access to document hyphenation options. |
| [getIncludeTextboxesFootnotesEndnotesInStat()](#getIncludeTextboxesFootnotesEndnotesInStat) | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| [getJustificationMode()](#getJustificationMode) | Gets the character spacing adjustment of a document. |
| [getLastChild()](#getLastChild) | Gets the last child of the node. |
| [getLastSection()](#getLastSection) | Gets the last section in the document. |
| [getLayoutOptions()](#getLayoutOptions) | Gets a [LayoutOptions](../../com.aspose.words/layoutoptions/) object that represents options to control the layout process of this document. |
| [getLists()](#getLists) | Provides access to the list formatting used in the document. |
| [getMailMerge()](#getMailMerge) | Returns a [MailMerge](../../com.aspose.words/mailmerge/) object that represents the mail merge functionality for the document. |
| [getMailMergeSettings()](#getMailMergeSettings) | Gets the object that contains all of the mail merge information for a document. |
| [getNextMatchingNode(Node curNode)](#getNextMatchingNode-com.aspose.words.Node) |  |
| [getNextSibling()](#getNextSibling) | Gets the node immediately following this node. |
| [getNodeChangingCallback()](#getNodeChangingCallback) | Called when a node is inserted or removed in the document. |
| [getNodeType()](#getNodeType) | Returns [NodeType.DOCUMENT](../../com.aspose.words/nodetype/\#DOCUMENT). |
| [getOriginalFileName()](#getOriginalFileName) | Gets the original file name of the document. |
| [getOriginalLoadFormat()](#getOriginalLoadFormat) | Gets the format of the original document that was loaded into this object. |
| [getPackageCustomParts()](#getPackageCustomParts) | Gets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [getPageColor()](#getPageColor) | Gets the page color of the document. |
| [getPageCount()](#getPageCount) | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [getPageInfo(int pageIndex)](#getPageInfo-int) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
| [getParentNode()](#getParentNode) | Gets the immediate parent of this node. |
| [getPreviousSibling()](#getPreviousSibling) | Gets the node immediately preceding this node. |
| [getProtectionType()](#getProtectionType) | Gets the currently active document protection type. |
| [getPunctuationKerning()](#getPunctuationKerning) | Specifies whether kerning applies to both Latin text and punctuation. |
| [getRange()](#getRange) | Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node. |
| [getRemovePersonalInformation()](#getRemovePersonalInformation) | Gets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback) | Allows to control how external resources are loaded. |
| [getRevisions()](#getRevisions) | Gets a collection of revisions (tracked changes) that exist in this document. |
| [getRevisionsView()](#getRevisionsView) | Gets a value indicating whether to work with the original or revised version of a document. |
| [getSections()](#getSections) | Returns a collection that represents all sections in the document. |
| [getShadeFormData()](#getShadeFormData) | Specifies whether to turn on the gray shading on form fields. |
| [getShowGrammaticalErrors()](#getShowGrammaticalErrors) | Specifies whether to display grammar errors in this document. |
| [getShowSpellingErrors()](#getShowSpellingErrors) | Specifies whether to display spelling errors in this document. |
| [getSpellingChecked()](#getSpellingChecked) | Returns  true  if the document has been checked for spelling. |
| [getStyles()](#getStyles) | Returns a collection of styles defined in the document. |
| [getText()](#getText) | Gets the text of this node and of all its children. |
| [getTheme()](#getTheme) | Gets the [getTheme()](../../com.aspose.words/document/\#getTheme) object for this document. |
| [getTrackRevisions()](#getTrackRevisions) | True if changes are tracked when this document is edited in Microsoft Word. |
| [getVariables()](#getVariables) | Returns the collection of variables added to a document or template. |
| [getVbaProject()](#getVbaProject) | Gets a [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject). |
| [getVersionsCount()](#getVersionsCount) | Gets the number of document versions that was stored in the DOC document. |
| [getViewOptions()](#getViewOptions) | Provides options to control how the document is displayed in Microsoft Word. |
| [getWarningCallback()](#getWarningCallback) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [getWatermark()](#getWatermark) | Provides access to the document watermark. |
| [getWebExtensionTaskPanes()](#getWebExtensionTaskPanes) | Returns a collection that represents a list of task pane add-ins. |
| [getWriteProtection()](#getWriteProtection) | Provides access to the document write protection options. |
| [hasChildNodes()](#hasChildNodes) | Returns  true  if this node has any child nodes. |
| [hasMacros()](#hasMacros) | Returns  true  if the document has a VBA project (macros). |
| [hasRevisions()](#hasRevisions) | Returns  true  if the document has any tracked changes. |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Imports a node from another document to the current document. |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting) | Joins runs with same formatting in all paragraphs of the document. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes) | Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar/\#getFieldType) of [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/) in the whole document so that they correspond to the field types contained in the field codes. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [print()](#print) | Prints the document without bringing up any user interface forms. |
| [print(String printerName)](#print-java.lang.String) | Print the whole document to the specified printer, using the standard (no User Interface) print controller. |
| [print(AttributeSet printerSettings)](#print-javax.print.attribute.AttributeSet) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller. |
| [print(AttributeSet printerSettings, String documentName)](#print-javax.print.attribute.AttributeSet-java.lang.String) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name. |
| [protect(int type)](#protect-int) |  |
| [protect(int type, String password)](#protect-int-java.lang.String) |  |
| [remove()](#remove) |  |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeBlankPages()](#removeBlankPages) | Removes blank pages from the document. |
| [removeExternalSchemaReferences()](#removeExternalSchemaReferences) | Removes external XML schema references from this document. |
| [removeMacros()](#removeMacros) | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)](#renderToScale-int-java.awt.Graphics2D-float-float-float) | Renders a document page into a java.awt.Graphics2D object to a specified scale. |
| [renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-int-java.awt.Graphics2D-float-float-float-float) | Renders a document page into a java.awt.Graphics2D object to a specified size. |
| [save(OutputStream stream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [save(OutputStream stream, int saveFormat)](#save-java.io.OutputStream-int) |  |
| [save(String fileName)](#save-java.lang.String) | Saves the document. |
| [save(String fileName, SaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SaveOptions) | Saves the document to a file using the specified save options. |
| [save(String fileName, int saveFormat)](#save-java.lang.String-int) |  |
| [selectNodes(String xpath)](#selectNodes-java.lang.String) | Selects a list of nodes matching the XPath expression. |
| [selectSingleNode(String xpath)](#selectSingleNode-java.lang.String) | Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression. |
| [setAttachedTemplate(String value)](#setAttachedTemplate-java.lang.String) | Sets the full path of the template attached to the document. |
| [setAutomaticallyUpdateStyles(boolean value)](#setAutomaticallyUpdateStyles-boolean) | Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [setBackgroundShape(Shape value)](#setBackgroundShape-com.aspose.words.Shape) | Sets the background shape of the document. |
| [setCustomNodeId(int value)](#setCustomNodeId-int) | Specifies custom node identifier. |
| [setCustomXmlParts(CustomXmlPartCollection value)](#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection) | Sets the collection of Custom XML Data Storage Parts. |
| [setDefaultTabStop(double value)](#setDefaultTabStop-double) | Sets the interval (in points) between the default tab stops. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings) | Sets document font settings. |
| [setGlossaryDocument(GlossaryDocument value)](#setGlossaryDocument-com.aspose.words.GlossaryDocument) | Sets the glossary document within this document or template. |
| [setGrammarChecked(boolean value)](#setGrammarChecked-boolean) | Returns  true  if the document has been checked for grammar. |
| [setIncludeTextboxesFootnotesEndnotesInStat(boolean value)](#setIncludeTextboxesFootnotesEndnotesInStat-boolean) | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| [setJustificationMode(int value)](#setJustificationMode-int) | Sets the character spacing adjustment of a document. |
| [setMailMergeSettings(MailMergeSettings value)](#setMailMergeSettings-com.aspose.words.MailMergeSettings) | Sets the object that contains all of the mail merge information for a document. |
| [setNodeChangingCallback(INodeChangingCallback value)](#setNodeChangingCallback-com.aspose.words.INodeChangingCallback) | Called when a node is inserted or removed in the document. |
| [setPackageCustomParts(CustomPartCollection value)](#setPackageCustomParts-com.aspose.words.CustomPartCollection) | Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [setPageColor(Color value)](#setPageColor-java.awt.Color) | Sets the page color of the document. |
| [setPunctuationKerning(boolean value)](#setPunctuationKerning-boolean) | Specifies whether kerning applies to both Latin text and punctuation. |
| [setRemovePersonalInformation(boolean value)](#setRemovePersonalInformation-boolean) | Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback) | Allows to control how external resources are loaded. |
| [setRevisionsView(int value)](#setRevisionsView-int) | Sets a value indicating whether to work with the original or revised version of a document. |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object) |  |
| [setShadeFormData(boolean value)](#setShadeFormData-boolean) | Specifies whether to turn on the gray shading on form fields. |
| [setShowGrammaticalErrors(boolean value)](#setShowGrammaticalErrors-boolean) | Specifies whether to display grammar errors in this document. |
| [setShowSpellingErrors(boolean value)](#setShowSpellingErrors-boolean) | Specifies whether to display spelling errors in this document. |
| [setSpellingChecked(boolean value)](#setSpellingChecked-boolean) | Returns  true  if the document has been checked for spelling. |
| [setTrackRevisions(boolean value)](#setTrackRevisions-boolean) | True if changes are tracked when this document is edited in Microsoft Word. |
| [setVbaProject(VbaProject value)](#setVbaProject-com.aspose.words.VbaProject) | Sets a [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject). |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [startTrackRevisions(String author)](#startTrackRevisions-java.lang.String) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [startTrackRevisions(String author, Date dateTime)](#startTrackRevisions-java.lang.String-java.util.Date) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [stopTrackRevisions()](#stopTrackRevisions) | Stops automatic marking of document changes as revisions. |
| [toString()](#toString) |  |
| [toString(SaveOptions saveOptions)](#toString-com.aspose.words.SaveOptions) | Exports the content of the node into a string using the specified save options. |
| [toString(int saveFormat)](#toString-int) |  |
| [unlinkFields()](#unlinkFields) | Unlinks fields in the whole document. |
| [unprotect()](#unprotect) | Removes protection from the document. |
| [unprotect(String password)](#unprotect-java.lang.String) | Removes protection from the document if a correct password is specified. |
| [updateActualReferenceMarks()](#updateActualReferenceMarks) | Updates the [Footnote.getActualReferenceMark()](../../com.aspose.words/footnote/\#getActualReferenceMark) property of all footnotes and endnotes in the document. |
| [updateFields()](#updateFields) | Updates the values of fields in the whole document. |
| [updateListLabels()](#updateListLabels) | Updates list labels for all list items in the document. |
| [updatePageLayout()](#updatePageLayout) | Rebuilds the page layout of the document. |
| [updateTableLayout()](#updateTableLayout) | Implements an earlier approach to table column widths re-calculation that has known issues. |
| [updateThumbnail()](#updateThumbnail) | Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document using default options. |
| [updateThumbnail(ThumbnailGeneratingOptions options)](#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) | Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document according to the specified options. |
| [updateWordCount()](#updateWordCount) | Updates word count properties of the document. |
| [updateWordCount(boolean updateLinesCount)](#updateWordCount-boolean) | Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties/\#getLines) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties/\#setLines-int) property. |
### Document() {#Document}
```
public Document()
```


Creates or loads a document.  Creates a blank Word document.

 **Remarks:** 

A blank document is retrieved from resources, and by default, the resulting document looks more like created by [MsWordVersion.WORD\_2007](../../com.aspose.words/mswordversion/\#WORD-2007). This blank document contains a default fonts table, minimal default styles, and latent styles.

**M:Aspose.Words.Settings.CompatibilityOptions.OptimizeFor(Aspose.Words.Settings.MsWordVersion)** method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

The document paper size is Letter by default. If you want to change page setup, use [Section.getPageSetup()](../../com.aspose.words/section/\#getPageSetup).

After creation, you can use [DocumentBuilder](../../com.aspose.words/documentbuilder/) to add document content easily.

 **Examples:** 

Shows how to format a run of text using its font property.

```

 Document doc = new Document();
 Run run = new Run(doc, "Hello world!");

 Font font = run.getFont();
 font.setName("Courier New");
 font.setSize(36.0);
 font.setHighlightColor(Color.YELLOW);

 doc.getFirstSection().getBody().getFirstParagraph().appendChild(run);
 doc.save(getArtifactsDir() + "Font.CreateFormattedRun.docx");
 
```

Shows how to create simple document.

```

 Document doc = new Document();

 // New Document objects by default come with the minimal set of nodes
 // required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
 doc.appendChild(new Section(doc))
     .appendChild(new Body(doc))
     .appendChild(new Paragraph(doc))
     .appendChild(new Run(doc, "Hello world!"));
 
```

Shows how to create and load documents.

```

 // There are two ways of creating a Document object using Aspose.Words.
 // 1 -  Create a blank document:
 Document doc = new Document();

 // New Document objects by default come with the minimal set of nodes
 // required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
 doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, "Hello world!"));

 // 2 -  Load a document that exists in the local file system:
 doc = new Document(getMyDir() + "Document.docx");

 // Loaded documents will have contents that we can access and edit.
 Assert.assertEquals("Hello World!", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());

 // Some operations that need to occur during loading, such as using a password to decrypt a document,
 // can be done by passing a LoadOptions object when loading the document.
 doc = new Document(getMyDir() + "Encrypted.docx", new LoadOptions("docPassword"));

 Assert.assertEquals("Test encrypted document.", doc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

### Document(String fileName) {#Document-java.lang.String}
```
public Document(String fileName)
```


Opens an existing document from a file. Automatically detects the file format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | File name of the document to open. |

### Document(String fileName, LoadOptions loadOptions) {#Document-java.lang.String-com.aspose.words.LoadOptions}
```
public Document(String fileName, LoadOptions loadOptions)
```


Opens an existing document from a file. Allows to specify additional options such as an encryption password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | File name of the document to open. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Additional options to use when loading a document. Can be  null . |

### Document(InputStream stream) {#Document-java.io.InputStream}
```
public Document(InputStream stream)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### Document(InputStream stream, LoadOptions loadOptions) {#Document-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Document(InputStream stream, LoadOptions loadOptions)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |

### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

 **Remarks:** 

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

Calls [DocumentVisitor.visitDocumentStart(com.aspose.words.Document)](../../com.aspose.words/documentvisitor/\#visitDocumentStart-com.aspose.words.Document), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the document and calls [DocumentVisitor.visitDocumentEnd(com.aspose.words.Document)](../../com.aspose.words/documentvisitor/\#visitDocumentEnd-com.aspose.words.Document) at the end.

 **Examples:** 

Shows how to use a document visitor to print a document's node structure.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes.
### acceptAllRevisions() {#acceptAllRevisions}
```
public void acceptAllRevisions()
```


Accepts all tracked changes in the document.

 **Remarks:** 

This method is a shortcut for [RevisionCollection.acceptAll()](../../com.aspose.words/revisioncollection/\#acceptAll).

 **Examples:** 

Shows how to accept all tracking changes in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Edit the document while tracking changes to create a few revisions.
 doc.startTrackRevisions("John Doe");
 builder.write("Hello world! ");
 builder.write("Hello again! ");
 builder.write("This is another revision.");
 doc.stopTrackRevisions();

 Assert.assertEquals(3, doc.getRevisions().getCount());

 // We can iterate through every revision and accept/reject it as a part of our document.
 // If we know we wish to accept every revision, we can do it more straightforwardly so by calling this method.
 doc.acceptAllRevisions();

 Assert.assertEquals(0, doc.getRevisions().getCount());
 Assert.assertEquals("Hello world! Hello again! This is another revision.", doc.getText().trim());
 
```

### acceptEnd(DocumentVisitor visitor) {#acceptEnd-com.aspose.words.DocumentVisitor}
```
public int acceptEnd(DocumentVisitor visitor)
```


Accepts a visitor for visiting the end of the document.

 **Examples:** 

Shows how to use a document visitor to print a document's node structure.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### acceptStart(DocumentVisitor visitor) {#acceptStart-com.aspose.words.DocumentVisitor}
```
public int acceptStart(DocumentVisitor visitor)
```


Accepts a visitor for visiting the start of the document.

 **Examples:** 

Shows how to use a document visitor to print a document's node structure.

```

 public void docStructureToText() throws Exception {
     Document doc = new Document(getMyDir() + "DocumentVisitor-compatible features.docx");
     DocStructurePrinter visitor = new DocStructurePrinter();

     // When we get a composite node to accept a document visitor, the visitor visits the accepting node,
     // and then traverses all the node's children in a depth-first manner.
     // The visitor can read and modify each visited node.
     doc.accept(visitor);

     System.out.println(visitor.getText());
 }

 /// 
 /// Traverses a node's tree of child nodes.
 /// Creates a map of this tree in the form of a string.
 /// 
 public static class DocStructurePrinter extends DocumentVisitor {
     public DocStructurePrinter() {
         mAcceptingNodeChildTree = new StringBuilder();
     }

     public String getText() {
         return mAcceptingNodeChildTree.toString();
     }

     /// 
     /// Called when a Document node is encountered.
     /// 
     public int visitDocumentStart(Document doc) {
         int childNodeCount = doc.getChildNodes(NodeType.ANY, true).getCount();

         indentAndAppendLine("[Document start] Child nodes: " + childNodeCount);
         mDocTraversalDepth++;

         // Allow the visitor to continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Document node have been visited.
     /// 
     public int visitDocumentEnd(Document doc) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Document end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Section node is encountered in the document.
     /// 
     public int visitSectionStart(final Section section) {
         // Get the index of our section within the document
         NodeCollection docSections = section.getDocument().getChildNodes(NodeType.SECTION, false);
         int sectionIndex = docSections.indexOf(section);

         indentAndAppendLine("[Section start] Section index: " + sectionIndex);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Section node have been visited.
     /// 
     public int visitSectionEnd(final Section section) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Section end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Body node is encountered in the document.
     /// 
     public int visitBodyStart(final Body body) {
         int paragraphCount = body.getParagraphs().getCount();
         indentAndAppendLine("[Body start] Paragraphs: " + paragraphCount);
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Body node have been visited.
     /// 
     public int visitBodyEnd(final Body body) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Body end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Paragraph node is encountered in the document.
     /// 
     public int visitParagraphStart(final Paragraph paragraph) {
         indentAndAppendLine("[Paragraph start]");
         mDocTraversalDepth++;

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called after all the child nodes of a Paragraph node have been visited.
     /// 
     public int visitParagraphEnd(final Paragraph paragraph) {
         mDocTraversalDepth--;
         indentAndAppendLine("[Paragraph end]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a Run node is encountered in the document.
     /// 
     public int visitRun(final Run run) {
         indentAndAppendLine("[Run] \"" + run.getText() + "\"");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitSubDocument(final SubDocument subDocument) {
         indentAndAppendLine("[SubDocument]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
     {
         indentAndAppendLine("[SdtRangeStart]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a SubDocument node is encountered in the document.
     /// 
     public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
     {
         indentAndAppendLine("[SdtRangeEnd]");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Append a line to the StringBuilder and indent it depending on how deep the visitor is into the document tree.
     /// 
     /// 
     private void indentAndAppendLine(final String text) {
         for (int i = 0; i < mDocTraversalDepth; i++) {
             mAcceptingNodeChildTree.append("|  ");
         }

         mAcceptingNodeChildTree.append(text + "\r\n");
     }

     private int mDocTraversalDepth;
     private final StringBuilder mAcceptingNodeChildTree;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The document visitor. |

**Returns:**
int - The action to be taken by the visitor. The returned value is one of [VisitorAction](../../com.aspose.words/visitoraction/) constants.
### add(Shape watermark) {#add-com.aspose.words.Shape}
```
public void add(Shape watermark)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermark | [Shape](../../com.aspose.words/shape/) |  |

### appendDocument(Document srcDoc, int importFormatMode) {#appendDocument-com.aspose.words.Document-int}
```
public void appendDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |

### appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions}
```
public void appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document/) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions/) |  |

### cleanup() {#cleanup}
```
public void cleanup()
```


Cleans unused styles and lists from the document.

 **Examples:** 

Shows how to remove unused custom styles from a document.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style counts as "used" while applied to some part of the document,
 // which means that the four styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark the styles as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List list = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(list);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 doc.cleanup();

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Run the Cleanup method again to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup();

 Assert.assertEquals(4, doc.getStyles().getCount());
 
```

### cleanup(CleanupOptions options) {#cleanup-com.aspose.words.CleanupOptions}
```
public void cleanup(CleanupOptions options)
```


Cleans unused styles and lists from the document depending on given [CleanupOptions](../../com.aspose.words/cleanupoptions/).

 **Examples:** 

Shows how to remove all unused custom styles from a document.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List list = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(list);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| options | [CleanupOptions](../../com.aspose.words/cleanupoptions/) |  |

### clearSectionAttrs() {#clearSectionAttrs}
```
public void clearSectionAttrs()
```




### compare(Document document, String author, Date dateTime) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date}
```
public void compare(Document document, String author, Date dateTime)
```


Compares this document with another document producing changes as number of edit and format revisions [Revision](../../com.aspose.words/revision/).

 **Remarks:** 

Documents must not have revisions before comparison.

 **Examples:** 

Shows how to compare documents.

```

 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);
 builder.writeln("This is the original document.");

 Document docEdited = new Document();
 builder = new DocumentBuilder(docEdited);
 builder.writeln("This is the edited document.");

 // Comparing documents with revisions will throw an exception.
 if (docOriginal.getRevisions().getCount() == 0 && docEdited.getRevisions().getCount() == 0)
     docOriginal.compare(docEdited, "authorName", new Date());

 // After the comparison, the original document will gain a new revision
 // for every element that is different in the edited document.
 for (Revision r : docOriginal.getRevisions())
 {
     System.out.println("Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
     System.out.println("\tChanged text: \"{r.ParentNode.GetText()}\"");
 }

 // Accepting these revisions will transform the original document into the edited document.
 docOriginal.getRevisions().acceptAll();

 Assert.assertEquals(docOriginal.getText(), docEdited.getText());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Document to compare. |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. |

### compare(Document document, String author, Date dateTime, CompareOptions options) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public void compare(Document document, String author, Date dateTime, CompareOptions options)
```


Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../com.aspose.words/revision/). Allows to specify comparison options using [CompareOptions](../../com.aspose.words/compareoptions/).

 **Examples:** 

Shows how to filter specific types of document elements when making a comparison.

```

 // Create the original document and populate it with various kinds of elements.
 Document docOriginal = new Document();
 DocumentBuilder builder = new DocumentBuilder(docOriginal);

 // Paragraph text referenced with an endnote:
 builder.writeln("Hello world! This is the first paragraph.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Original endnote text.");

 // Table:
 builder.startTable();
 builder.insertCell();
 builder.write("Original cell 1 text");
 builder.insertCell();
 builder.write("Original cell 2 text");
 builder.endTable();

 // Textbox:
 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 150.0, 20.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.write("Original textbox contents");

 // DATE field:
 builder.moveTo(docOriginal.getFirstSection().getBody().appendParagraph(""));
 builder.insertField(" DATE ");

 // Comment:
 Comment newComment = new Comment(docOriginal, "John Doe", "J.D.", new Date());
 newComment.setText("Original comment.");
 builder.getCurrentParagraph().appendChild(newComment);

 // Header:
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.writeln("Original header contents.");

 // Create a clone of our document and perform a quick edit on each of the cloned document's elements.
 Document docEdited = (Document)docOriginal.deepClone(true);
 Paragraph firstParagraph = docEdited.getFirstSection().getBody().getFirstParagraph();

 firstParagraph.getRuns().get(0).setText("hello world! this is the first paragraph, after editing.");
 firstParagraph.getParagraphFormat().setStyle(docEdited.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1));
 ((Footnote)docEdited.getChild(NodeType.FOOTNOTE, 0, true)).getFirstParagraph().getRuns().get(1).setText("Edited endnote text.");
 ((Table)docEdited.getChild(NodeType.TABLE, 0, true)).getFirstRow().getCells().get(1).getFirstParagraph().getRuns().get(0).setText("Edited Cell 2 contents");
 ((Shape)docEdited.getChild(NodeType.SHAPE, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited textbox contents");
 ((FieldDate)docEdited.getRange().getFields().get(0)).setUseLunarCalendar(true);
 ((Comment)docEdited.getChild(NodeType.COMMENT, 0, true)).getFirstParagraph().getRuns().get(0).setText("Edited comment.");
 docEdited.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_PRIMARY).getFirstParagraph().getRuns().get(0).setText("Edited header contents.");

 // Comparing documents creates a revision for every edit in the edited document.
 // A CompareOptions object has a series of flags that can suppress revisions
 // on each respective type of element, effectively ignoring their change.
 CompareOptions compareOptions = new CompareOptions();
 compareOptions.setIgnoreFormatting(false);
 compareOptions.setIgnoreCaseChanges(false);
 compareOptions.setIgnoreComments(false);
 compareOptions.setIgnoreTables(false);
 compareOptions.setIgnoreFields(false);
 compareOptions.setIgnoreFootnotes(false);
 compareOptions.setIgnoreTextboxes(false);
 compareOptions.setIgnoreHeadersAndFooters(false);
 compareOptions.setTarget(ComparisonTargetType.NEW);

 docOriginal.compare(docEdited, "John Doe", new Date(), compareOptions);
 docOriginal.save(getArtifactsDir() + "Document.CompareOptions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) |  |
| author | java.lang.String |  |
| dateTime | java.util.Date |  |
| options | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### copyStylesFromTemplate(Document template) {#copyStylesFromTemplate-com.aspose.words.Document}
```
public void copyStylesFromTemplate(Document template)
```


Copies styles from the specified template to a document.

 **Remarks:** 

When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

 **Examples:** 

Shows how to copies styles from the template to a document via Document.

```

 Document template = new Document(getMyDir() + "Rendering.docx");
 Document target = new Document(getMyDir() + "Document.docx");

 target.copyStylesFromTemplate(template);
 
```

Shows how to copy styles from one document to another.

```

 // Create a document, and then add styles that we will copy to another document.
 Document template = new Document();

 Style style = template.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle1");
 style.getFont().setName("Times New Roman");
 style.getFont().setColor(Color.WHITE);

 style = template.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle2");
 style.getFont().setName("Arial");
 style.getFont().setColor(Color.RED);

 style = template.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle3");
 style.getFont().setName("Courier New");
 style.getFont().setColor(Color.BLUE);

 Assert.assertEquals(7, template.getStyles().getCount());

 // Create a document which we will copy the styles to.
 Document target = new Document();

 // Create a style with the same name as a style from the template document and add it to the target document.
 style = target.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle3");
 style.getFont().setName("Calibri");
 style.getFont().setColor(Color.ORANGE);

 Assert.assertEquals(5, target.getStyles().getCount());

 // There are two ways of calling the method to copy all the styles from one document to another.
 // 1 -  Passing the template document object:
 target.copyStylesFromTemplate(template);

 // Copying styles adds all styles from the template document to the target
 // and overwrites existing styles with the same name.
 Assert.assertEquals(7, target.getStyles().getCount());

 Assert.assertEquals("Courier New", target.getStyles().get("TemplateStyle3").getFont().getName());
 Assert.assertEquals(Color.BLUE.getRGB(), target.getStyles().get("TemplateStyle3").getFont().getColor().getRGB());

 // 2 -  Passing the local system filename of a template document:
 target.copyStylesFromTemplate(getMyDir() + "Rendering.docx");

 Assert.assertEquals(21, target.getStyles().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| template | [Document](../../com.aspose.words/document/) |  |

### copyStylesFromTemplate(String template) {#copyStylesFromTemplate-java.lang.String}
```
public void copyStylesFromTemplate(String template)
```


Copies styles from the specified template to a document.

 **Remarks:** 

When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

 **Examples:** 

Shows how to copy styles from one document to another.

```

 // Create a document, and then add styles that we will copy to another document.
 Document template = new Document();

 Style style = template.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle1");
 style.getFont().setName("Times New Roman");
 style.getFont().setColor(Color.WHITE);

 style = template.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle2");
 style.getFont().setName("Arial");
 style.getFont().setColor(Color.RED);

 style = template.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle3");
 style.getFont().setName("Courier New");
 style.getFont().setColor(Color.BLUE);

 Assert.assertEquals(7, template.getStyles().getCount());

 // Create a document which we will copy the styles to.
 Document target = new Document();

 // Create a style with the same name as a style from the template document and add it to the target document.
 style = target.getStyles().add(StyleType.PARAGRAPH, "TemplateStyle3");
 style.getFont().setName("Calibri");
 style.getFont().setColor(Color.ORANGE);

 Assert.assertEquals(5, target.getStyles().getCount());

 // There are two ways of calling the method to copy all the styles from one document to another.
 // 1 -  Passing the template document object:
 target.copyStylesFromTemplate(template);

 // Copying styles adds all styles from the template document to the target
 // and overwrites existing styles with the same name.
 Assert.assertEquals(7, target.getStyles().getCount());

 Assert.assertEquals("Courier New", target.getStyles().get("TemplateStyle3").getFont().getName());
 Assert.assertEquals(Color.BLUE.getRGB(), target.getStyles().get("TemplateStyle3").getFont().getColor().getRGB());

 // 2 -  Passing the local system filename of a template document:
 target.copyStylesFromTemplate(getMyDir() + "Rendering.docx");

 Assert.assertEquals(21, target.getStyles().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| template | java.lang.String |  |

### dd() {#dd}
```
public void dd()
```




### deepClone() {#deepClone}
```
public Document deepClone()
```


Performs a deep copy of the [Document](../../com.aspose.words/document/).

 **Examples:** 

Shows how to deep clone a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 // Cloning will produce a new document with the same contents as the original,
 // but with a unique copy of each of the original document's nodes.
 Document clone = doc.deepClone();

 Assert.assertEquals(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText(),
         clone.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).getText());
 Assert.assertNotEquals(doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).hashCode(),
         clone.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).hashCode());
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The cloned document.
### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

 **Remarks:** 

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

 **Examples:** 

Shows how to clone a composite node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();
 para.appendChild(new Run(doc, "Hello world!"));

 // Below are two ways of cloning a composite node.
 // 1 -  Create a clone of a node, and create a clone of each of its child nodes as well.
 Node cloneWithChildren = para.deepClone(true);

 Assert.assertTrue(((CompositeNode) cloneWithChildren).hasChildNodes());
 Assert.assertEquals("Hello world!", cloneWithChildren.getText().trim());

 // 2 -  Create a clone of a node just by itself without any children.
 Node cloneWithoutChildren = para.deepClone(false);

 Assert.assertFalse(((CompositeNode) cloneWithoutChildren).hasChildNodes());
 Assert.assertEquals("", cloneWithoutChildren.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| isCloneChildren | boolean | True to recursively clone the subtree under the specified node; false to clone only the node itself. |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node.
### ensureMinimum() {#ensureMinimum}
```
public void ensureMinimum()
```


If the document contains no sections, creates one section with one paragraph.

 **Examples:** 

Shows how to ensure that a document contains the minimal set of nodes required for editing its contents.

```

 // A newly created document contains one child Section, which includes one child Body and one child Paragraph.
 // We can edit the document body's contents by adding nodes such as Runs or inline Shapes to that paragraph.
 Document doc = new Document();
 NodeCollection nodes = doc.getChildNodes(NodeType.ANY, true);

 Assert.assertEquals(NodeType.SECTION, nodes.get(0).getNodeType());
 Assert.assertEquals(doc, nodes.get(0).getParentNode());

 Assert.assertEquals(NodeType.BODY, nodes.get(1).getNodeType());
 Assert.assertEquals(nodes.get(0), nodes.get(1).getParentNode());

 Assert.assertEquals(NodeType.PARAGRAPH, nodes.get(2).getNodeType());
 Assert.assertEquals(nodes.get(1), nodes.get(2).getParentNode());

 // This is the minimal set of nodes that we need to be able to edit the document.
 // We will no longer be able to edit the document if we remove any of them.
 doc.removeAllChildren();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.ANY, true).getCount());

 // Call this method to make sure that the document has at least those three nodes so we can edit it again.
 doc.ensureMinimum();

 Assert.assertEquals(NodeType.SECTION, nodes.get(0).getNodeType());
 Assert.assertEquals(NodeType.BODY, nodes.get(1).getNodeType());
 Assert.assertEquals(NodeType.PARAGRAPH, nodes.get(2).getNodeType());

 ((Paragraph) nodes.get(2)).getRuns().add(new Run(doc, "Hello world!"));
 
```

### expandTableStylesToDirectFormatting() {#expandTableStylesToDirectFormatting}
```
public void expandTableStylesToDirectFormatting()
```


Converts formatting specified in table styles into direct formatting on tables in the document.

 **Remarks:** 

This method exists because this version of Aspose.Words provides only limited support for table styles (see below). This method might be useful when you load a DOCX or WordprocessingML document that contains tables formatted with table styles and you need to query formatting of tables, cells, paragraphs or text.

This version of Aspose.Words provides limited support for table styles as follows:

 *  Table styles defined in DOCX or WordprocessingML documents are preserved as table styles when saving the document as DOCX or WordprocessingML.
 *  Table styles defined in DOCX or WordprocessingML documents are automatically converted to direct formatting on tables when saving the document into any other format, rendering or printing.
 *  Table styles defined in DOC documents are preserved as table styles when saving the document as DOC only.

 **Examples:** 

Shows how to apply the properties of a table's style directly to the table's elements.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Hello world!");
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setRowStripe(3);
 tableStyle.setCellSpacing(5.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);

 table.setStyle(tableStyle);

 // This method concerns table style properties such as the ones we set above.
 doc.expandTableStylesToDirectFormatting();

 doc.save(getArtifactsDir() + "Document.TableStyleToDirectFormatting.docx");
 
```

### extractPages(int index, int count) {#extractPages-int-int}
```
public Document extractPages(int index, int count)
```


Returns the [Document](../../com.aspose.words/document/) object representing specified range of pages.

 **Remarks:** 

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' \\u2013 the numbering, headers/footers and cross tables layout will be preserved. But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort. Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document. Any feedback would be greatly appreciated.

 **Examples:** 

Shows how to get specified range of pages from the document.

```

 Document doc = new Document(getMyDir() + "Layout entities.docx");

 doc = doc.extractPages(0, 2);

 doc.save(getArtifactsDir() + "Document.ExtractPages.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |

**Returns:**
[Document](../../com.aspose.words/document/)
### fetchInheritedSectionAttr(int key) {#fetchInheritedSectionAttr-int}
```
public Object fetchInheritedSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchSectionAttr(int key) {#fetchSectionAttr-int}
```
public Object fetchSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### get() {#get}
```
public Shape get()
```




**Returns:**
[Shape](../../com.aspose.words/shape/)
### getAncestor(int ancestorType) {#getAncestor-int}
```
public CompositeNode getAncestor(int ancestorType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | int |  |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getAncestor(Class ancestorType) {#getAncestor-java.lang.Class}
```
public CompositeNode getAncestor(Class ancestorType)
```


Gets the first ancestor of the specified object type.

 **Remarks:** 

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .

 **Examples:** 

Shows how to find out if a tables are nested.

```

 public void calculateDepthOfNestedTables() throws Exception {
     Document doc = new Document(getMyDir() + "Nested tables.docx");
     NodeCollection tables = doc.getChildNodes(NodeType.TABLE, true);
     for (int i = 0; i < tables.getCount(); i++) {
         Table table = (Table) tables.get(i);

         // Find out if any cells in the table have other tables as children.
         int count = getChildTableCount(table);
         System.out.print(MessageFormat.format("Table #{0} has {1} tables directly within its cells", i, count));

         // Find out if the table is nested inside another table, and, if so, at what depth.
         int tableDepth = getNestedDepthOfTable(table);

         if (tableDepth > 0)
             System.out.println(MessageFormat.format("Table #{0} is nested inside another table at depth of {1}", i, tableDepth));
         else
             System.out.println(MessageFormat.format("Table #{0} is a non nested table (is not a child of another table)", i));
     }
 }

 // Calculates what level a table is nested inside other tables.
 //
 // Returns An integer containing the level the table is nested at.
 // 0 = Table is not nested inside any other table
 // 1 = Table is nested within one parent table
 // 2 = Table is nested within two parent tables etc..
 private static int getNestedDepthOfTable(final Table table) {
     int depth = 0;
     Node parent = table.getAncestor(table.getNodeType());

     while (parent != null) {
         depth++;
         parent = parent.getAncestor(Table.class);
     }

     return depth;
 }

 // Determines if a table contains any immediate child table within its cells.
 // Does not recursively traverse through those tables to check for further tables.
 //
 // Returns true if at least one child cell contains a table.
 // Returns false if no cells in the table contains a table.
 private static int getChildTableCount(final Table table) {
     int childTableCount = 0;

     for (Row row : table.getRows()) {
         for (Cell cell : row.getCells()) {
             TableCollection childTables = cell.getTables();

             if (childTables.getCount() > 0) childTableCount++;
         }
     }

     return childTableCount;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.
### getAttachedTemplate() {#getAttachedTemplate}
```
public String getAttachedTemplate()
```


Gets the full path of the template attached to the document.

**Returns:**
java.lang.String - The full path of the template attached to the document.
### getAutomaticallyUpdateStyles() {#getAutomaticallyUpdateStyles}
```
public boolean getAutomaticallyUpdateStyles()
```


Gets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

 **Examples:** 

Shows how to attach a template to a document.

```

 Document doc = new Document();

 // Microsoft Word documents by default come with an attached template called "Normal.dotm".
 // There is no default template for blank Aspose.Words documents.
 Assert.assertEquals("", doc.getAttachedTemplate());

 // Attach a template, then set the flag to apply style changes
 // within the template to styles in our document.
 doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");
 doc.setAutomaticallyUpdateStyles(true);

 doc.save(getArtifactsDir() + "Document.AutomaticallyUpdateStyles.docx");
 
```

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Returns:**
boolean - A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.
### getBackgroundShape() {#getBackgroundShape}
```
public Shape getBackgroundShape()
```


Gets the background shape of the document. Can be  null .

 **Remarks:** 

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype/\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions/\#getDisplayBackgroundShape) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions/\#setDisplayBackgroundShape-boolean) to  true .

 **Examples:** 

Shows how to set a background shape for every page of a document.

```

 Document doc = new Document();

 Assert.assertNull(doc.getBackgroundShape());

 // The only shape type that we can use as a background is a rectangle.
 Shape shapeRectangle = new Shape(doc, ShapeType.RECTANGLE);

 // There are two ways of using this shape as a page background.
 // 1 -  A flat color:
 shapeRectangle.setFillColor(Color.BLUE);
 doc.setBackgroundShape(shapeRectangle);

 doc.save(getArtifactsDir() + "DocumentBase.BackgroundShape.FlatColor.docx");

 // 2 -  An image:
 shapeRectangle = new Shape(doc, ShapeType.RECTANGLE);
 shapeRectangle.getImageData().setImage(getImageDir() + "Transparent background logo.png");

 // Adjust the image's appearance to make it more suitable as a watermark.
 shapeRectangle.getImageData().setContrast(0.2);
 shapeRectangle.getImageData().setBrightness(0.7);

 doc.setBackgroundShape(shapeRectangle);

 Assert.assertTrue(doc.getBackgroundShape().hasImage());

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setCacheBackgroundGraphics(false);

 // Microsoft Word does not support shapes with images as backgrounds,
 // but we can still see these backgrounds in other save formats such as .pdf.
 doc.save(getArtifactsDir() + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
 
```

**Returns:**
[Shape](../../com.aspose.words/shape/) - The background shape of the document.
### getBibliography() {#getBibliography}
```
public Bibliography getBibliography()
```


Gets the [getBibliography()](../../com.aspose.words/document/\#getBibliography) object that represents the list of sources available in the document.

 **Examples:** 

Shows how to get bibliography sources available in the document.

```

 Document document = new Document(getMyDir() + "Bibliography sources.docx");

 Bibliography bibliography = document.getBibliography();
 Assert.assertEquals(12, bibliography.getSources().size());

 Collection sources = bibliography.getSources();
 Source source = sources.iterator().next();
 Assert.assertEquals("Book 0 (No LCID)", source.getTitle());
 Assert.assertEquals(SourceType.BOOK, source.getSourceType());
 Assert.assertNull(source.getAbbreviatedCaseNumber());
 Assert.assertNull(source.getAlbumTitle());
 Assert.assertNull(source.getBookTitle());
 Assert.assertNull(source.getBroadcaster());
 Assert.assertNull(source.getBroadcastTitle());
 Assert.assertNull(source.getCaseNumber());
 Assert.assertNull(source.getChapterNumber());
 Assert.assertNull(source.getComments());
 Assert.assertNull(source.getConferenceName());
 Assert.assertNull(source.getCountryOrRegion());
 Assert.assertNull(source.getCourt());
 Assert.assertNull(source.getDay());
 Assert.assertNull(source.getDayAccessed());
 Assert.assertNull(source.getDepartment());
 Assert.assertNull(source.getDistributor());
 Assert.assertNull(source.getEdition());
 Assert.assertNull(source.getGuid());
 Assert.assertNull(source.getInstitution());
 Assert.assertNull(source.getInternetSiteTitle());
 Assert.assertNull(source.getIssue());
 Assert.assertNull(source.getJournalName());
 Assert.assertNull(source.getLcid());
 Assert.assertNull(source.getMedium());
 Assert.assertNull(source.getMonth());
 Assert.assertNull(source.getMonthAccessed());
 Assert.assertNull(source.getNumberVolumes());
 Assert.assertNull(source.getPages());
 Assert.assertNull(source.getPatentNumber());
 Assert.assertNull(source.getPeriodicalTitle());
 Assert.assertNull(source.getProductionCompany());
 Assert.assertNull(source.getPublicationTitle());
 Assert.assertNull(source.getPublisher());
 Assert.assertNull(source.getRecordingNumber());
 Assert.assertNull(source.getRefOrder());
 Assert.assertNull(source.getReporter());
 Assert.assertNull(source.getShortTitle());
 Assert.assertNull(source.getStandardNumber());
 Assert.assertNull(source.getStateOrProvince());
 Assert.assertNull(source.getStation());
 Assert.assertEquals("BookNoLCID", source.getTag());
 Assert.assertNull(source.getTheater());
 Assert.assertNull(source.getThesisType());
 Assert.assertNull(source.getType());
 Assert.assertNull(source.getUrl());
 Assert.assertNull(source.getVersion());
 Assert.assertNull(source.getVolume());
 Assert.assertNull(source.getYear());
 Assert.assertNull(source.getYearAccessed());

 ContributorCollection contributors = source.getContributors();
 Assert.assertNull(contributors.getArtist());
 Assert.assertNull(contributors.getBookAuthor());
 Assert.assertNull(contributors.getCompiler());
 Assert.assertNull(contributors.getComposer());
 Assert.assertNull(contributors.getConductor());
 Assert.assertNull(contributors.getCounsel());
 Assert.assertNull(contributors.getDirector());
 Assert.assertNotNull(contributors.getEditor());
 Assert.assertNull(contributors.getInterviewee());
 Assert.assertNull(contributors.getInterviewer());
 Assert.assertNull(contributors.getInventor());
 Assert.assertNull(contributors.getPerformer());
 Assert.assertNull(contributors.getProducer());
 Assert.assertNotNull(contributors.getTranslator());
 Assert.assertNull(contributors.getWriter());

 Contributor editor  = contributors.getEditor();
 Assert.assertEquals(2, ((PersonCollection)editor).getCount());

 PersonCollection authors = (PersonCollection)contributors.getAuthor();
 Assert.assertEquals(2, authors.getCount());

 Person person = authors.get(0);
 Assert.assertEquals("Roxanne", person.getFirst());
 Assert.assertEquals("Brielle", person.getMiddle());
 Assert.assertEquals("Tejeda", person.getLast());
 
```

**Returns:**
[Bibliography](../../com.aspose.words/bibliography/) - The [getBibliography()](../../com.aspose.words/document/\#getBibliography) object that represents the list of sources available in the document.
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Returns a collection that represents all the built-in document properties of the document.

**Returns:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties/) - A collection that represents all the built-in document properties of the document.
### getChild(int nodeType, int index, boolean isDeep) {#getChild-int-int-boolean}
```
public Node getChild(int nodeType, int index, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| index | int |  |
| isDeep | boolean |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getChildNodes(int nodeType, boolean isDeep) {#getChildNodes-int-boolean}
```
public NodeCollection getChildNodes(int nodeType, boolean isDeep)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |
| isDeep | boolean |  |

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/)
### getCompatibilityOptions() {#getCompatibilityOptions}
```
public CompatibilityOptions getCompatibilityOptions()
```


Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word).

 **Examples:** 

Shows how to optimize the document for different versions of Microsoft Word.

```

 public void optimizeFor() throws Exception
 {
     Document doc = new Document();

     // This object contains an extensive list of flags unique to each document
     // that allow us to facilitate backward compatibility with older versions of Microsoft Word.
     CompatibilityOptions options = doc.getCompatibilityOptions();

     // Print the default settings for a blank document.
     System.out.println("\nDefault optimization settings:");
     printCompatibilityOptions(options);

     // We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
     doc.save(getArtifactsDir() + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

     // We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
     doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2010);
     System.out.println("\nOptimized for Word 2010:");
     printCompatibilityOptions(options);

     doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2000);
     System.out.println("\nOptimized for Word 2000:");
     printCompatibilityOptions(options);
 }

 /// 
 /// Groups all flags in a document's compatibility options object by state, then prints each group.
 /// 
 private static void printCompatibilityOptions(CompatibilityOptions options)
 {
     ArrayList enabledOptions = new ArrayList();
     ArrayList disabledOptions = new ArrayList();
     addOptionName(options.getAdjustLineHeightInTable(), "AdjustLineHeightInTable", enabledOptions, disabledOptions);
     addOptionName(options.getAlignTablesRowByRow(), "AlignTablesRowByRow", enabledOptions, disabledOptions);
     addOptionName(options.getAllowSpaceOfSameStyleInTable(), "AllowSpaceOfSameStyleInTable", enabledOptions, disabledOptions);
     addOptionName(options.getApplyBreakingRules(), "ApplyBreakingRules", enabledOptions, disabledOptions);
     addOptionName(options.getAutoSpaceLikeWord95(), "AutoSpaceLikeWord95", enabledOptions, disabledOptions);
     addOptionName(options.getAutofitToFirstFixedWidthCell(), "AutofitToFirstFixedWidthCell", enabledOptions, disabledOptions);
     addOptionName(options.getBalanceSingleByteDoubleByteWidth(), "BalanceSingleByteDoubleByteWidth", enabledOptions, disabledOptions);
     addOptionName(options.getCachedColBalance(), "CachedColBalance", enabledOptions, disabledOptions);
     addOptionName(options.getConvMailMergeEsc(), "ConvMailMergeEsc", enabledOptions, disabledOptions);
     addOptionName(options.getDisableOpenTypeFontFormattingFeatures(), "DisableOpenTypeFontFormattingFeatures", enabledOptions, disabledOptions);
     addOptionName(options.getDisplayHangulFixedWidth(), "DisplayHangulFixedWidth", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotAutofitConstrainedTables(), "DoNotAutofitConstrainedTables", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotBreakConstrainedForcedTable(), "DoNotBreakConstrainedForcedTable", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotBreakWrappedTables(), "DoNotBreakWrappedTables", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotExpandShiftReturn(), "DoNotExpandShiftReturn", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotLeaveBackslashAlone(), "DoNotLeaveBackslashAlone", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotSnapToGridInCell(), "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotSuppressIndentation(), "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotSuppressParagraphBorders(), "DoNotSuppressParagraphBorders", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotUseEastAsianBreakRules(), "DoNotUseEastAsianBreakRules", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotUseHTMLParagraphAutoSpacing(), "DoNotUseHTMLParagraphAutoSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotUseIndentAsNumberingTabStop(), "DoNotUseIndentAsNumberingTabStop", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotVertAlignCellWithSp(), "DoNotVertAlignCellWithSp", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotVertAlignInTxbx(), "DoNotVertAlignInTxbx", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotWrapTextWithPunct(), "DoNotWrapTextWithPunct", enabledOptions, disabledOptions);
     addOptionName(options.getFootnoteLayoutLikeWW8(), "FootnoteLayoutLikeWW8", enabledOptions, disabledOptions);
     addOptionName(options.getForgetLastTabAlignment(), "ForgetLastTabAlignment", enabledOptions, disabledOptions);
     addOptionName(options.getGrowAutofit(), "GrowAutofit", enabledOptions, disabledOptions);
     addOptionName(options.getLayoutRawTableWidth(), "LayoutRawTableWidth", enabledOptions, disabledOptions);
     addOptionName(options.getLayoutTableRowsApart(), "LayoutTableRowsApart", enabledOptions, disabledOptions);
     addOptionName(options.getLineWrapLikeWord6(), "LineWrapLikeWord6", enabledOptions, disabledOptions);
     addOptionName(options.getMWSmallCaps(), "MWSmallCaps", enabledOptions, disabledOptions);
     addOptionName(options.getNoColumnBalance(), "NoColumnBalance", enabledOptions, disabledOptions);
     addOptionName(options.getNoExtraLineSpacing(), "NoExtraLineSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getNoLeading(), "NoLeading", enabledOptions, disabledOptions);
     addOptionName(options.getNoSpaceRaiseLower(), "NoSpaceRaiseLower", enabledOptions, disabledOptions);
     addOptionName(options.getNoTabHangInd(), "NoTabHangInd", enabledOptions, disabledOptions);
     addOptionName(options.getOverrideTableStyleFontSizeAndJustification(), "OverrideTableStyleFontSizeAndJustification", enabledOptions, disabledOptions);
     addOptionName(options.getPrintBodyTextBeforeHeader(), "PrintBodyTextBeforeHeader", enabledOptions, disabledOptions);
     addOptionName(options.getPrintColBlack(), "PrintColBlack", enabledOptions, disabledOptions);
     addOptionName(options.getSelectFldWithFirstOrLastChar(), "SelectFldWithFirstOrLastChar", enabledOptions, disabledOptions);
     addOptionName(options.getShapeLayoutLikeWW8(), "ShapeLayoutLikeWW8", enabledOptions, disabledOptions);
     addOptionName(options.getShowBreaksInFrames(), "ShowBreaksInFrames", enabledOptions, disabledOptions);
     addOptionName(options.getSpaceForUL(), "SpaceForUL", enabledOptions, disabledOptions);
     addOptionName(options.getSpacingInWholePoints(), "SpacingInWholePoints", enabledOptions, disabledOptions);
     addOptionName(options.getSplitPgBreakAndParaMark(), "SplitPgBreakAndParaMark", enabledOptions, disabledOptions);
     addOptionName(options.getSubFontBySize(), "SubFontBySize", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressBottomSpacing(), "SuppressBottomSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressSpBfAfterPgBrk(), "SuppressSpBfAfterPgBrk", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressSpacingAtTopOfPage(), "SuppressSpacingAtTopOfPage", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressTopSpacing(), "SuppressTopSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressTopSpacingWP(), "SuppressTopSpacingWP", enabledOptions, disabledOptions);
     addOptionName(options.getSwapBordersFacingPgs(), "SwapBordersFacingPgs", enabledOptions, disabledOptions);
     addOptionName(options.getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(), "SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning", enabledOptions, disabledOptions);
     addOptionName(options.getTransparentMetafiles(), "TransparentMetafiles", enabledOptions, disabledOptions);
     addOptionName(options.getTruncateFontHeightsLikeWP6(), "TruncateFontHeightsLikeWP6", enabledOptions, disabledOptions);
     addOptionName(options.getUICompat97To2003(), "UICompat97To2003", enabledOptions, disabledOptions);
     addOptionName(options.getUlTrailSpace(), "UlTrailSpace", enabledOptions, disabledOptions);
     addOptionName(options.getUnderlineTabInNumList(), "UnderlineTabInNumList", enabledOptions, disabledOptions);
     addOptionName(options.getUseAltKinsokuLineBreakRules(), "UseAltKinsokuLineBreakRules", enabledOptions, disabledOptions);
     addOptionName(options.getUseAnsiKerningPairs(), "UseAnsiKerningPairs", enabledOptions, disabledOptions);
     addOptionName(options.getUseFELayout(), "UseFELayout", enabledOptions, disabledOptions);
     addOptionName(options.getUseNormalStyleForList(), "UseNormalStyleForList", enabledOptions, disabledOptions);
     addOptionName(options.getUsePrinterMetrics(), "UsePrinterMetrics", enabledOptions, disabledOptions);
     addOptionName(options.getUseSingleBorderforContiguousCells(), "UseSingleBorderforContiguousCells", enabledOptions, disabledOptions);
     addOptionName(options.getUseWord2002TableStyleRules(), "UseWord2002TableStyleRules", enabledOptions, disabledOptions);
     addOptionName(options.getUseWord2010TableStyleRules(), "UseWord2010TableStyleRules", enabledOptions, disabledOptions);
     addOptionName(options.getUseWord97LineBreakRules(), "UseWord97LineBreakRules", enabledOptions, disabledOptions);
     addOptionName(options.getWPJustification(), "WPJustification", enabledOptions, disabledOptions);
     addOptionName(options.getWPSpaceWidth(), "WPSpaceWidth", enabledOptions, disabledOptions);
     addOptionName(options.getWrapTrailSpaces(), "WrapTrailSpaces", enabledOptions, disabledOptions);
     System.out.println("\tEnabled options:");
     for (String optionName : enabledOptions)
         System.out.println("\t\t{optionName}");
     System.out.println("\tDisabled options:");
     for (String optionName : disabledOptions)
         System.out.println("\t\t{optionName}");
 }

 private static void addOptionName(boolean option, String optionName, ArrayList enabledOptions, ArrayList disabledOptions)
 {
     if (option)
         enabledOptions.add(optionName);
     else
         disabledOptions.add(optionName);
 }
 
```

**Returns:**
[CompatibilityOptions](../../com.aspose.words/compatibilityoptions/) - The corresponding [CompatibilityOptions](../../com.aspose.words/compatibilityoptions/) value.
### getCompliance() {#getCompliance}
```
public int getCompliance()
```


Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

 **Remarks:** 

If you created a new blank document or load non OOXML document returns the [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance/\#ECMA-376-2006) value.

 **Examples:** 

Shows how to read a loaded document's Open Office XML compliance version.

```

 // The compliance version varies between documents created by different versions of Microsoft Word.
 Document doc = new Document(getMyDir() + "Document.doc");

 Assert.assertEquals(doc.getCompliance(), OoxmlCompliance.ECMA_376_2006);

 doc = new Document(getMyDir() + "Document.docx");

 Assert.assertEquals(doc.getCompliance(), OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);
 
```

**Returns:**
int - The OOXML compliance version determined from the loaded document content. The returned value is one of [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/) constants.
### getContainer() {#getContainer}
```
public CompositeNode getContainer()
```




**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/)
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of immediate children of this node.

 **Examples:** 

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```

 Document doc = new Document();

 // An empty document, by default, has one paragraph.
 Assert.assertEquals(1, doc.getFirstSection().getBody().getParagraphs().getCount());

 // Composite nodes such as our paragraph can contain other composite and inline nodes as children.
 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 Run paragraphText = new Run(doc, "Initial text. ");
 paragraph.appendChild(paragraphText);

 // Create three more run nodes.
 Run run1 = new Run(doc, "Run 1. ");
 Run run2 = new Run(doc, "Run 2. ");
 Run run3 = new Run(doc, "Run 3. ");

 // The document body will not display these runs until we insert them into a composite node
 // that itself is a part of the document's node tree, as we did with the first run.
 // We can determine where the text contents of nodes that we insert
 // appears in the document by specifying an insertion location relative to another node in the paragraph.
 Assert.assertEquals("Initial text.", paragraph.getText().trim());

 // Insert the second run into the paragraph in front of the initial run.
 paragraph.insertBefore(run2, paragraphText);

 Assert.assertEquals("Run 2. Initial text.", paragraph.getText().trim());

 // Insert the third run after the initial run.
 paragraph.insertAfter(run3, paragraphText);

 Assert.assertEquals("Run 2. Initial text. Run 3.", paragraph.getText().trim());

 // Insert the first run to the start of the paragraph's child nodes collection.
 paragraph.prependChild(run1);

 Assert.assertEquals("Run 1. Run 2. Initial text. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(4, paragraph.getChildNodes(NodeType.ANY, true).getCount());

 // We can modify the contents of the run by editing and deleting existing child nodes.
 ((Run) paragraph.getChildNodes(NodeType.RUN, true).get(1)).setText("Updated run 2. ");
 paragraph.getChildNodes(NodeType.RUN, true).remove(paragraphText);

 Assert.assertEquals("Run 1. Updated run 2. Run 3.", paragraph.getText().trim());
 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, true).getCount());
 
```

**Returns:**
int - The number of immediate children of this node.
### getCurrentNode() {#getCurrentNode}
```
public Node getCurrentNode()
```




**Returns:**
[Node](../../com.aspose.words/node/)
### getCustomDocumentProperties() {#getCustomDocumentProperties}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


Returns a collection that represents all the custom document properties of the document.

**Returns:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties/) - A collection that represents all the custom document properties of the document.
### getCustomNodeId() {#getCustomNodeId}
```
public int getCustomNodeId()
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Returns:**
int - The corresponding  int  value.
### getCustomXmlParts() {#getCustomXmlParts}
```
public CustomXmlPartCollection getCustomXmlParts()
```


Gets the collection of Custom XML Data Storage Parts.

 **Remarks:** 

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

 **Examples:** 

Shows how to create a structured document tag with custom XML data.

```

 Document doc = new Document();

 // Construct an XML part that contains data and add it to the document's collection.
 // If we enable the "Developer" tab in Microsoft Word,
 // we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 Assert.assertEquals(xmlPart.getData(), xmlPartContent.getBytes());
 Assert.assertEquals(xmlPart.getId(), xmlPartId);

 // Below are two ways to refer to XML parts.
 // 1 -  By an index in the custom XML part collection:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().get(0));

 // 2 -  By GUID:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().getById(xmlPartId));

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone a part, and then insert it into the collection.
 CustomXmlPart xmlPartClone = xmlPart.deepClone();
 xmlPartClone.setId(UUID.randomUUID().toString());
 doc.getCustomXmlParts().add(xmlPartClone);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 2);

 // Iterate through the collection and print the contents of each part.
 Iterator enumerator = doc.getCustomXmlParts().iterator();
 int index = 0;
 while (enumerator.hasNext()) {
     CustomXmlPart customXmlPart = enumerator.next();
     System.out.println(MessageFormat.format("XML part index {0}, ID: {1}", index, customXmlPart.getId()));
     System.out.println(MessageFormat.format("\tContent: {0}", customXmlPart.getData()));
     index++;
 }

 // Use the "RemoveAt" method to remove the cloned part by index.
 doc.getCustomXmlParts().removeAt(1);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 1);

 // Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
 CustomXmlPartCollection customXmlParts = doc.getCustomXmlParts().deepClone();
 customXmlParts.clear();

 // Create a structured document tag that will display our part's contents and insert it into the document body.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[1]", "");

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CustomXml.docx");
 
```

**Returns:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection/) - The collection of Custom XML Data Storage Parts.
### getDefaultTabStop() {#getDefaultTabStop}
```
public double getDefaultTabStop()
```


Gets the interval (in points) between the default tab stops.

 **Examples:** 

Shows how to set a custom interval for tab stop positions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

**Returns:**
double - The interval (in points) between the default tab stops.
### getDigitalSignatures() {#getDigitalSignatures}
```
public DigitalSignatureCollection getDigitalSignatures()
```


Gets the collection of digital signatures for this document and their validation results.

 **Remarks:** 

This collection contains digital signatures that were loaded from the original document. These digital signatures will not be saved when you save this [Document](../../com.aspose.words/document/) object into a file or stream because saving or converting will produce a document that is different from the original and the original digital signatures will no longer be valid.

This collection is never  null . If the document is not signed, it will contain zero elements.

 **Examples:** 

Shows how to validate and display information about each signature in a document.

```

 Document doc = new Document(getMyDir() + "Digitally signed.docx");

 for (DigitalSignature signature : doc.getDigitalSignatures()) {
     System.out.println("*** Signature Found ***");
     System.out.println("Is valid: " + signature.isValid());
     // This property is available in MS Word documents only
     System.out.println("Reason for signing: " + signature.getComments());
     System.out.println("Signature type: " + signature.getSignatureType());
     System.out.println("Time of signing: " + signature.getSignTime());
     System.out.println("Subject name: " + signature.getSubjectName());
     System.out.println("Issuer name: " + signature.getIssuerName());
     System.out.println();
 }
 
```

Shows how to sign documents with X.509 certificates.

```

 // Verify that a document is not signed.
 Assert.assertFalse(FileFormatUtil.detectFileFormat(getMyDir() + "Document.docx").hasDigitalSignature());

 // Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
 CertificateHolder certificateHolder = CertificateHolder.create(getMyDir() + "morzal.pfx", "aw", null);

 SignOptions signOptions = new SignOptions();
 signOptions.setSignTime(new Date());

 // There are two ways of saving a signed copy of a document to the local file system:
 // 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
 DigitalSignatureUtil.sign(getMyDir() + "Document.docx", getArtifactsDir() + "Document.DigitalSignature.docx",
         certificateHolder, signOptions);

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // 2 - Take a document from a stream, and save a signed copy to another stream.
 InputStream inDoc = new FileInputStream(getMyDir() + "Document.docx");
 try {
     OutputStream outDoc = new FileOutputStream(getArtifactsDir() + "Document.DigitalSignature.docx");
     try {
         DigitalSignatureUtil.sign(inDoc, outDoc, certificateHolder);
     } finally {
         if (outDoc != null) outDoc.close();
     }
 } finally {
     if (inDoc != null) inDoc.close();
 }

 Assert.assertTrue(FileFormatUtil.detectFileFormat(getArtifactsDir() + "Document.DigitalSignature.docx").hasDigitalSignature());

 // Please verify that all of the document's digital signatures are valid and check their details.
 Document signedDoc = new Document(getArtifactsDir() + "Document.DigitalSignature.docx");
 DigitalSignatureCollection digitalSignatureCollection = signedDoc.getDigitalSignatures();

 Assert.assertTrue(digitalSignatureCollection.isValid());
 Assert.assertEquals(1, digitalSignatureCollection.getCount());
 Assert.assertEquals(DigitalSignatureType.XML_DSIG, digitalSignatureCollection.get(0).getSignatureType());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getIssuerName());
 Assert.assertEquals("CN=Morzal.Me", signedDoc.getDigitalSignatures().get(0).getSubjectName());
 
```

**Returns:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection/) - The collection of digital signatures for this document and their validation results.
### getDirectSectionAttr(int key) {#getDirectSectionAttr-int}
```
public Object getDirectSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets this instance.

 **Examples:** 

Shows how to create simple document.

```

 Document doc = new Document();

 // New Document objects by default come with the minimal set of nodes
 // required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
 doc.appendChild(new Section(doc))
     .appendChild(new Body(doc))
     .appendChild(new Paragraph(doc))
     .appendChild(new Run(doc, "Hello world!"));
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - This instance.
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Provides options that control numbering and positioning of endnotes in this document.

 **Examples:** 

Shows how to select a different place where the document collects and displays its endnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // An endnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting an endnote adds a small superscript reference symbol
 // at the main body text where we insert the endnote.
 // Each endnote also creates an entry at the end of the document, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote contents.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("This is the second section.");

 // We can use the "Position" property to determine where the document will place all its endnotes.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfDocument",
 // every footnote will show up in a collection at the end of the document. This is the default value.
 // If we set the value of the "Position" property to "EndnotePosition.EndOfSection",
 // every footnote will show up in a collection at the end of the section whose text contains the endnote's reference mark.
 doc.getEndnoteOptions().setPosition(endnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionEndnote.docx");
 
```

Shows how to set a number at which the document begins the footnote/endnote count.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```

Shows how to change the number style of footnote/endnote reference marks.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

Shows how to restart footnote/endnote numbering at certain places in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions/) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions/) value.
### getFieldOptions() {#getFieldOptions}
```
public FieldOptions getFieldOptions()
```


Gets a [FieldOptions](../../com.aspose.words/fieldoptions/) object that represents options to control field handling in the document.

**Returns:**
[FieldOptions](../../com.aspose.words/fieldoptions/) - A [FieldOptions](../../com.aspose.words/fieldoptions/) object that represents options to control field handling in the document.
### getFirstChild() {#getFirstChild}
```
public Node getFirstChild()
```


Gets the first child of the node.

 **Remarks:** 

If there is no first child node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFirstSection() {#getFirstSection}
```
public Section getFirstSection()
```


Gets the first section in the document.

 **Remarks:** 

Returns  null  if there are no sections.

 **Examples:** 

Shows how to replace text in a document's footer.

```

 Document doc = new Document(getMyDir() + "Footer.docx");

 HeaderFooterCollection headersFooters = doc.getFirstSection().getHeadersFooters();
 HeaderFooter footer = headersFooters.getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 FindReplaceOptions options = new FindReplaceOptions();
 options.setMatchCase(false);
 options.setFindWholeWordsOnly(false);

 int currentYear = Calendar.YEAR;
 footer.getRange().replace("(C) 2006 Aspose Pty Ltd.", MessageFormat.format("Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

 doc.save(getArtifactsDir() + "HeaderFooter.ReplaceText.docx");
 
```

Shows how to create a new section with a document builder.

```

 Document doc = new Document();

 // A blank document contains one section by default,
 // which contains child nodes that we can edit.
 Assert.assertEquals(1, doc.getSections().getCount());

 // Use a document builder to add text to the first section.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a second section by inserting a section break.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(2, doc.getSections().getCount());

 // Each section has its own page setup settings.
 // We can split the text in the second section into two columns.
 // This will not affect the text in the first section.
 doc.getLastSection().getPageSetup().getTextColumns().setCount(2);
 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 Assert.assertEquals(1, doc.getFirstSection().getPageSetup().getTextColumns().getCount());
 Assert.assertEquals(2, doc.getLastSection().getPageSetup().getTextColumns().getCount());

 doc.save(getArtifactsDir() + "Section.Create.docx");
 
```

Shows how to iterate through the children of a composite node.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Primary header");
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 builder.write("Primary footer");

 Section section = doc.getFirstSection();

 // A Section is a composite node and can contain child nodes,
 // but only if those child nodes are of a "Body" or "HeaderFooter" node type.
 for (Node node : section) {
     switch (node.getNodeType()) {
         case NodeType.BODY: {
             Body body = (Body) node;

             System.out.println("Body:");
             System.out.println("\t\"{body.GetText().Trim()}\"");
             break;
         }
         case NodeType.HEADER_FOOTER: {
             HeaderFooter headerFooter = (HeaderFooter) node;

             System.out.println("HeaderFooter type: {headerFooter.HeaderFooterType}:");
             System.out.println("\t\"{headerFooter.GetText().Trim()}\"");
             break;
         }
         default: {
             throw new Exception("Unexpected node type in a section.");
         }
     }
 }
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The first section in the document.
### getFontInfos() {#getFontInfos}
```
public FontInfoCollection getFontInfos()
```


Provides access to properties of fonts used in this document.

 **Remarks:** 

This collection of font definitions is loaded as is from the document. Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

 **Examples:** 

Shows how to save a document with embedded TrueType fonts.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 FontInfoCollection fontInfos = doc.getFontInfos();
 fontInfos.setEmbedTrueTypeFonts(embedAllFonts);
 fontInfos.setEmbedSystemFonts(embedAllFonts);
 fontInfos.setSaveSubsetFonts(embedAllFonts);

 doc.save(getArtifactsDir() + "Font.FontInfoCollection.docx");
 
```

Shows how to print the details of what fonts are present in a document.

```

 Document doc = new Document(getMyDir() + "Embedded font.docx");

 FontInfoCollection allFonts = doc.getFontInfos();
 // Print all the used and unused fonts in the document.
 for (int i = 0; i < allFonts.getCount(); i++) {
     System.out.println("Font index #{i}");
     System.out.println("\tName: {allFonts[i].Name}");
 }
 
```

**Returns:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection/) - The corresponding [FontInfoCollection](../../com.aspose.words/fontinfocollection/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Gets document font settings.

 **Remarks:** 

This property allows to specify font settings per document. If set to  null , default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) will be used.

The default value is  null .

 **Examples:** 

Shows how set font substitution rules.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] fontSources = FontSettings.getDefaultInstance().getFontsSources();

 // The default font sources contain the first font that the document uses.
 Assert.assertEquals(1, fontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The second font, "Amethysta", is unavailable.
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // We can configure a font substitution table which determines
 // which fonts Aspose.Words will use as substitutes for unavailable fonts.
 // Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
 // If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().setSubstitutes(
         "Amethysta", "Arvo", "Courier New");

 // "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo".
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // "Arvo" is also unavailable, but "Courier New" is.
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Courier New")));

 // The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
 doc.save(getArtifactsDir() + "FontSettings.TableSubstitution.pdf");
 
```

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - Document font settings.
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Provides options that control numbering and positioning of footnotes in this document.

 **Examples:** 

Shows how to select a different place where the document collects and displays its footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```

Shows how to set a number at which the document begins the footnote/endnote count.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes, which both begin at 1.
 Assert.assertEquals(1, doc.getFootnoteOptions().getStartNumber());
 Assert.assertEquals(1, doc.getEndnoteOptions().getStartNumber());

 // We can use the "StartNumber" property to get the document to
 // begin a footnote or endnote count at a different number.
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.ARABIC);
 doc.getEndnoteOptions().setStartNumber(50);

 doc.save(getArtifactsDir() + "InlineStory.StartNumber.docx");
 
```

Shows how to change the number style of footnote/endnote reference marks.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.", "Custom footnote reference mark");

 builder.insertParagraph();

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.", "Custom endnote reference mark");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and for endnotes. By default, footnotes display their numbers using Arabic numerals,
 // and endnotes display their numbers in lowercase Roman numerals.
 Assert.assertEquals(NumberStyle.ARABIC, doc.getFootnoteOptions().getNumberStyle());
 Assert.assertEquals(NumberStyle.LOWERCASE_ROMAN, doc.getEndnoteOptions().getNumberStyle());

 // We can use the "NumberStyle" property to apply custom numbering styles to footnotes and endnotes.
 // This will not affect footnotes/endnotes with custom reference marks.
 doc.getFootnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 doc.getEndnoteOptions().setNumberStyle(NumberStyle.UPPERCASE_LETTER);

 doc.save(getArtifactsDir() + "InlineStory.RefMarkNumberStyle.docx");
 
```

Shows how to restart footnote/endnote numbering at certain places in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions/) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions/) value.
### getFrameset() {#getFrameset}
```
public Frameset getFrameset()
```


Returns a [getFrameset()](../../com.aspose.words/document/\#getFrameset) instance if this document represents a frames page.

 **Remarks:** 

If the document is not framed, the property has the  null  value.

 **Examples:** 

Shows how to access frames on-page.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Returns:**
[Frameset](../../com.aspose.words/frameset/) - A [getFrameset()](../../com.aspose.words/document/\#getFrameset) instance if this document represents a frames page.
### getGlossaryDocument() {#getGlossaryDocument}
```
public GlossaryDocument getGlossaryDocument()
```


Gets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

 **Remarks:** 

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument/) object and assigning to this property.

 **Examples:** 

Shows how to add a custom building block to a document.

```

 public void createAndInsert() throws Exception {
     // A document's glossary document stores building blocks.
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();
     doc.setGlossaryDocument(glossaryDoc);

     // Create a building block, name it, and then add it to the glossary document.
     BuildingBlock block = new BuildingBlock(glossaryDoc);
     block.setName("Custom Block");

     glossaryDoc.appendChild(block);

     // All new building block GUIDs have the same zero value by default, and we can give them a new unique value.
     Assert.assertEquals(block.getGuid().toString(), "00000000-0000-0000-0000-000000000000");

     block.setGuid(UUID.randomUUID());

     // The following properties categorize building blocks
     // in the menu we can access in Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     Assert.assertEquals(block.getCategory(), "(Empty Category)");
     Assert.assertEquals(block.getType(), BuildingBlockType.NONE);
     Assert.assertEquals(block.getGallery(), BuildingBlockGallery.ALL);
     Assert.assertEquals(block.getBehavior(), BuildingBlockBehavior.CONTENT);

     // Before we can add this building block to our document, we will need to give it some contents,
     // which we will do using a document visitor. This visitor will also set a category, gallery, and behavior.
     BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
     // Visit start/end of the BuildingBlock.
     block.accept(visitor);
     // Visit only start of the BuildingBlock.
     block.acceptStart(visitor);
     // Visit only end of the BuildingBlock.
     block.acceptEnd(visitor);

     // We can access the block that we just made from the glossary document.
     BuildingBlock customBlock = glossaryDoc.getBuildingBlock(BuildingBlockGallery.QUICK_PARTS,
             "My custom building blocks", "Custom Block");

     // The block itself is a section that contains the text.
     Assert.assertEquals(MessageFormat.format("Text inside {0}\f", customBlock.getName()), customBlock.getFirstSection().getBody().getFirstParagraph().getText());
     Assert.assertEquals(customBlock.getFirstSection(), customBlock.getLastSection());
     // Now, we can insert it into the document as a new section.
     doc.appendChild(doc.importNode(customBlock.getFirstSection(), true));

     // We can also find it in Microsoft Word's Building Blocks Organizer and place it manually.
     doc.save(getArtifactsDir() + "BuildingBlocks.CreateAndInsert.dotx");
 }

 /// 
 /// Sets up a visited building block to be inserted into the document as a quick part and adds text to its contents.
 /// 
 public static class BuildingBlockVisitor extends DocumentVisitor {
     public BuildingBlockVisitor(final GlossaryDocument ownerGlossaryDoc) {
         mBuilder = new StringBuilder();
         mGlossaryDoc = ownerGlossaryDoc;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         // Configure the building block as a quick part, and add properties used by Building Blocks Organizer.
         block.setBehavior(BuildingBlockBehavior.PARAGRAPH);
         block.setCategory("My custom building blocks");
         block.setDescription("Using this block in the Quick Parts section of word will place its contents at the cursor.");
         block.setGallery(BuildingBlockGallery.QUICK_PARTS);

         // Add a section with text.
         // Inserting the block into the document will append this section with its child nodes at the location.
         Section section = new Section(mGlossaryDoc);
         block.appendChild(section);
         block.getFirstSection().ensureMinimum();

         Run run = new Run(mGlossaryDoc, "Text inside " + block.getName());
         block.getFirstSection().getBody().getFirstParagraph().appendChild(run);

         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("Visited " + block.getName() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
     private final GlossaryDocument mGlossaryDoc;
 }
 
```

**Returns:**
[GlossaryDocument](../../com.aspose.words/glossarydocument/) - The glossary document within this document or template.
### getGrammarChecked() {#getGrammarChecked}
```
public boolean getGrammarChecked()
```


Returns  true  if the document has been checked for grammar.

 **Remarks:** 

To recheck the grammar in the document, set this property to  false .

 **Examples:** 

Shows how to set spelling or grammar verifying.

```

 Document doc = new Document();

 // The string with spelling errors.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().add(new Run(doc, "The speeling in this documentz is all broked."));

 // Spelling/Grammar check start if we set properties to false.
 // We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
 // Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
 doc.setSpellingChecked(checkSpellingGrammar);
 doc.setGrammarChecked(checkSpellingGrammar);

 doc.save(getArtifactsDir() + "Document.SpellingOrGrammar.docx");
 
```

**Returns:**
boolean -  true  if the document has been checked for grammar.
### getHyphenationOptions() {#getHyphenationOptions}
```
public HyphenationOptions getHyphenationOptions()
```


Provides access to document hyphenation options.

 **Examples:** 

Shows how to configure automatic hyphenation.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(24.0);
 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.getHyphenationOptions().setAutoHyphenation(true);
 doc.getHyphenationOptions().setConsecutiveHyphenLimit(2);
 doc.getHyphenationOptions().setHyphenationZone(720);
 doc.getHyphenationOptions().setHyphenateCaps(true);

 doc.save(getArtifactsDir() + "Document.HyphenationOptions.docx");
 
```

**Returns:**
[HyphenationOptions](../../com.aspose.words/hyphenationoptions/) - The corresponding [HyphenationOptions](../../com.aspose.words/hyphenationoptions/) value.
### getIncludeTextboxesFootnotesEndnotesInStat() {#getIncludeTextboxesFootnotesEndnotesInStat}
```
public boolean getIncludeTextboxesFootnotesEndnotesInStat()
```


Specifies whether to include textboxes, footnotes and endnotes in word count statistics.

 **Examples:** 

Shows how to include or exclude textboxes, footnotes and endnotes from word count statistics.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Lorem ipsum");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "sit amet");

 // By default option is set to 'false'.
 doc.updateWordCount();
 // Words count without textboxes, footnotes and endnotes.
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getWords());

 doc.setIncludeTextboxesFootnotesEndnotesInStat(true);
 doc.updateWordCount();
 // Words count with textboxes, footnotes and endnotes.
 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getWords());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getJustificationMode() {#getJustificationMode}
```
public int getJustificationMode()
```


Gets the character spacing adjustment of a document.

 **Examples:** 

Shows how to manage character spacing control.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```

**Returns:**
int - The character spacing adjustment of a document. The returned value is one of [JustificationMode](../../com.aspose.words/justificationmode/) constants.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node.

 **Remarks:** 

If there is no last child node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLastSection() {#getLastSection}
```
public Section getLastSection()
```


Gets the last section in the document.

 **Remarks:** 

Returns  null  if there are no sections.

 **Examples:** 

Shows how to create a new section with a document builder.

```

 Document doc = new Document();

 // A blank document contains one section by default,
 // which contains child nodes that we can edit.
 Assert.assertEquals(1, doc.getSections().getCount());

 // Use a document builder to add text to the first section.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a second section by inserting a section break.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(2, doc.getSections().getCount());

 // Each section has its own page setup settings.
 // We can split the text in the second section into two columns.
 // This will not affect the text in the first section.
 doc.getLastSection().getPageSetup().getTextColumns().setCount(2);
 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 Assert.assertEquals(1, doc.getFirstSection().getPageSetup().getTextColumns().getCount());
 Assert.assertEquals(2, doc.getLastSection().getPageSetup().getTextColumns().getCount());

 doc.save(getArtifactsDir() + "Section.Create.docx");
 
```

**Returns:**
[Section](../../com.aspose.words/section/) - The last section in the document.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Gets a [LayoutOptions](../../com.aspose.words/layoutoptions/) object that represents options to control the layout process of this document.

 **Examples:** 

Shows how to hide text in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Insert hidden text, then specify whether we wish to omit it from a rendered document.
 builder.writeln("This text is not hidden.");
 builder.getFont().setHidden(true);
 builder.writeln("This text is hidden.");

 doc.getLayoutOptions().setShowHiddenText(showHiddenText);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsHiddenText.pdf");
 
```

Shows how to show paragraph marks in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 // Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
 // with a pilcrow (¶) symbol when we render the document.
 builder.writeln("Hello world!");
 builder.writeln("Hello again!");

 doc.getLayoutOptions().setShowParagraphMarks(showParagraphMarks);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsParagraphMarks.pdf");
 
```

Shows how to alter the appearance of revisions in a rendered output document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a revision, then change the color of all revisions to green.
 builder.writeln("This is not a revision.");
 doc.startTrackRevisions("John Doe", new Date());
 builder.writeln("This is a revision.");
 doc.stopTrackRevisions();
 builder.writeln("This is not a revision.");

 // Remove the bar that appears to the left of every revised line.
 doc.getLayoutOptions().getRevisionOptions().setInsertedTextColor(RevisionColor.BRIGHT_GREEN);
 doc.getLayoutOptions().getRevisionOptions().setShowRevisionBars(false);
 doc.getLayoutOptions().getRevisionOptions().setRevisionBarsPosition(HorizontalAlignment.RIGHT);

 doc.save(getArtifactsDir() + "Document.LayoutOptionsRevisions.pdf");
 
```

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - A [LayoutOptions](../../com.aspose.words/layoutoptions/) object that represents options to control the layout process of this document.
### getLists() {#getLists}
```
public ListCollection getLists()
```


Provides access to the list formatting used in the document.

 **Remarks:** 

For more information see the description of the [ListCollection](../../com.aspose.words/listcollection/) class.

 **Examples:** 

Shows how to work with list levels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertFalse(builder.getListFormat().isListItem());

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create using a document builder.
 // 1 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.NUMBER_DEFAULT));

 Assert.assertTrue(builder.getListFormat().isListItem());

 // By setting the "ListLevelNumber" property, we can increase the list level
 // to begin a self-contained sub-list at the current list item.
 // The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
 // Deeper list levels use letters and lowercase Roman numerals.
 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // 2 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 // Deeper levels of this list will use different symbols, such as "\u25a0" and "\u25cb".
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));

 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
 builder.getListFormat().setList(null);

 Assert.assertFalse(builder.getListFormat().isListItem());

 doc.save(getArtifactsDir() + "Lists.SpecifyListLevel.docx");
 
```

**Returns:**
[ListCollection](../../com.aspose.words/listcollection/) - The corresponding [ListCollection](../../com.aspose.words/listcollection/) value.
### getMailMerge() {#getMailMerge}
```
public MailMerge getMailMerge()
```


Returns a [MailMerge](../../com.aspose.words/mailmerge/) object that represents the mail merge functionality for the document.

 **Examples:** 

Shows how to execute a mail merge with data from a DataTable.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // This example creates a table, but you would normally load table from a database
 DataTable table = new DataTable("Test");
 table.getColumns().add("CustomerName");
 table.getColumns().add("Address");
 table.getRows().add("Thomas Hardy", "120 Hanover Sq., London");
 table.getRows().add("Paolo Accorti", "Via Monte Bianco 34, Torino");

 // Field values from the table are inserted into the mail merge fields found in the document
 doc.getMailMerge().execute(table);

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.docx");

 // Create a copy of our document to perform another mail merge
 doc = new Document();
 builder = new DocumentBuilder(doc);
 builder.insertField(" MERGEFIELD CustomerName ");
 builder.insertParagraph();
 builder.insertField(" MERGEFIELD Address ");

 // We can also source values for a mail merge from a single row in the table
 doc.getMailMerge().execute(table.getRows().get(1));

 doc.save(getArtifactsDir() + "MailMerge.ExecuteDataTable.OneRow.docx");
 
```

**Returns:**
[MailMerge](../../com.aspose.words/mailmerge/) - A [MailMerge](../../com.aspose.words/mailmerge/) object that represents the mail merge functionality for the document.
### getMailMergeSettings() {#getMailMergeSettings}
```
public MailMergeSettings getMailMergeSettings()
```


Gets the object that contains all of the mail merge information for a document.

 **Remarks:** 

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

This object is never  null .

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/) - The object that contains all of the mail merge information for a document.
### getNextMatchingNode(Node curNode) {#getNextMatchingNode-com.aspose.words.Node}
```
public Node getNextMatchingNode(Node curNode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| curNode | [Node](../../com.aspose.words/node/) |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### getNextSibling() {#getNextSibling}
```
public Node getNextSibling()
```


Gets the node immediately following this node.

 **Remarks:** 

If there is no next node, a  null  is returned.

 **Examples:** 

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```

 Document doc = new Document(getMyDir() + "Paragraphs.docx");

 for (Node node = doc.getFirstSection().getBody().getFirstChild(); node != null; node = node.getNextSibling()) {
     System.out.println(Node.nodeTypeToString(node.getNodeType()));
 }
 
```

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeChangingCallback() {#getNodeChangingCallback}
```
public INodeChangingCallback getNodeChangingCallback()
```


Called when a node is inserted or removed in the document.

 **Examples:** 

Shows how customize node changing with a callback.

```

 public void fontChangeViaCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Set the node changing callback to custom implementation,
     // then add/remove nodes to get it to generate a log.
     HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
     doc.setNodeChangingCallback(callback);

     builder.writeln("Hello world!");
     builder.writeln("Hello again!");
     builder.insertField(" HYPERLINK \"https://www.google.com/\" ");
     builder.insertShape(ShapeType.RECTANGLE, 300.0, 300.0);

     doc.getRange().getFields().get(0).remove();

     System.out.println(callback.getLog());
 }

 /// 
 /// Logs the date and time of each node insertion and removal.
 /// Sets a custom font name/size for the text contents of Run nodes.
 /// 
 public static class HandleNodeChangingFontChanger implements INodeChangingCallback {
     public void nodeInserted(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash:\t{0}", args.getNode().hashCode()));

         if (args.getNode().getNodeType() == NodeType.RUN) {
             Font font = ((Run) args.getNode()).getFont();
             mLog.append(MessageFormat.format("\tFont:\tChanged from \"{0}\" {1}pt", font.getName(), font.getSize()));

             font.setSize(24.0);
             font.setName("Arial");

             mLog.append(MessageFormat.format(" to \"{0}\" {1}pt", font.getName(), font.getSize()));
             mLog.append(MessageFormat.format("\tContents:\n\t\t\"{0}\"", args.getNode().getText()));
         }
     }

     public void nodeInserting(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode insertion:", new Date()));
     }

     public void nodeRemoved(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash code:\t{0}", args.getNode().hashCode()));
     }

     public void nodeRemoving(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode removal:", new Date()));
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) - The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) value.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.DOCUMENT](../../com.aspose.words/nodetype/\#DOCUMENT).

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
int - [NodeType.DOCUMENT](../../com.aspose.words/nodetype/\#DOCUMENT). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getOriginalFileName() {#getOriginalFileName}
```
public String getOriginalFileName()
```


Gets the original file name of the document.

 **Remarks:** 

Returns  null  if the document was loaded from a stream or created blank.

 **Examples:** 

Shows how to retrieve details of a document's load operation.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Assert.assertEquals(getMyDir() + "Document.docx", doc.getOriginalFileName());
 Assert.assertEquals(LoadFormat.DOCX, doc.getOriginalLoadFormat());
 
```

Shows how to use the FileFormatUtil methods to detect the format of a document.

```

 // Load a document from a file that is missing a file extension, and then detect its file format.
 FileInputStream docStream = new FileInputStream(getMyDir() + "Word document with missing file extension");

 FileFormatInfo info = FileFormatUtil.detectFileFormat(docStream);

 int loadFormat = info.getLoadFormat();

 Assert.assertEquals(LoadFormat.DOC, loadFormat);

 // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
 // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
 String fileExtension = FileFormatUtil.loadFormatToExtension(loadFormat);

 int saveFormat = FileFormatUtil.extensionToSaveFormat(fileExtension);

 // 2 -  Convert the LoadFormat directly to its SaveFormat:
 saveFormat = FileFormatUtil.loadFormatToSaveFormat(loadFormat);

 // Load a document from the stream, and then save it to the automatically detected file extension.
 Document doc = new Document(docStream);

 Assert.assertEquals(".doc", FileFormatUtil.saveFormatToExtension(saveFormat));

 doc.save(getArtifactsDir() + "File.SaveToDetectedFileFormat" + FileFormatUtil.saveFormatToExtension(saveFormat));
 
```

**Returns:**
java.lang.String - The original file name of the document.
### getOriginalLoadFormat() {#getOriginalLoadFormat}
```
public int getOriginalLoadFormat()
```


Gets the format of the original document that was loaded into this object.

 **Remarks:** 

If you created a new blank document, returns the [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC) value.

 **Examples:** 

Shows how to retrieve details of a document's load operation.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Assert.assertEquals(getMyDir() + "Document.docx", doc.getOriginalFileName());
 Assert.assertEquals(LoadFormat.DOCX, doc.getOriginalLoadFormat());
 
```

**Returns:**
int - The format of the original document that was loaded into this object. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat/) constants.
### getPackageCustomParts() {#getPackageCustomParts}
```
public CustomPartCollection getPackageCustomParts()
```


Gets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

 **Remarks:** 

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document/\#getCustomXmlParts) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document/\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

 **Examples:** 

Shows how to access a document's arbitrary custom parts collection.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Returns:**
[CustomPartCollection](../../com.aspose.words/custompartcollection/) - The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".
### getPageColor() {#getPageColor}
```
public Color getPageColor()
```


Gets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

 **Remarks:** 

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

 **Examples:** 

Shows how to set the background color for all pages of a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.setPageColor(Color.lightGray);

 doc.save(getArtifactsDir() + "DocumentBase.SetPageColor.docx");
 
```

**Returns:**
java.awt.Color - The page color of the document.
### getPageCount() {#getPageCount}
```
public int getPageCount()
```


Gets the number of pages in the document as calculated by the most recent page layout operation.

 **Examples:** 

Shows how to count the number of pages in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Page 1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Page 2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Page 3");

 // Verify the expected page count of the document.
 Assert.assertEquals(3, doc.getPageCount());

 // Getting the PageCount property invoked the document's page layout to calculate the value.
 // This operation will not need to be re-done when rendering the document to a fixed page save format,
 // such as .pdf. So you can save some time, especially with more complex documents.
 doc.save(getArtifactsDir() + "Document.GetPageCount.pdf");
 
```

**Returns:**
int - The number of pages in the document as calculated by the most recent page layout operation.
### getPageInfo(int pageIndex) {#getPageInfo-int}
```
public PageInfo getPageInfo(int pageIndex)
```


Gets the page size, orientation and other information about a page that might be useful for printing or rendering.

 **Examples:** 

Shows how to check whether the page is in color or not.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |

**Returns:**
[PageInfo](../../com.aspose.words/pageinfo/)
### getParentNode() {#getParentNode}
```
public CompositeNode getParentNode()
```


Gets the immediate parent of this node.

 **Remarks:** 

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

 **Examples:** 

Shows how to access a node's parent node.

```

 Document doc = new Document();
 Paragraph para = doc.getFirstSection().getBody().getFirstParagraph();

 // Append a child Run node to the document's first paragraph.
 Run run = new Run(doc, "Hello world!");
 para.appendChild(run);

 // The paragraph is the parent node of the run node. We can trace this lineage
 // all the way to the document node, which is the root of the document's node tree.
 Assert.assertEquals(para, run.getParentNode());
 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals(doc.getFirstSection(), doc.getFirstSection().getBody().getParentNode());
 Assert.assertEquals(doc, doc.getFirstSection().getParentNode());
 
```

Shows how to create a node and set its owning document.

```

 Document doc = new Document();
 Paragraph para = new Paragraph(doc);
 para.appendChild(new Run(doc, "Hello world!"));

 // We have not yet appended this paragraph as a child to any composite node.
 Assert.assertNull(para.getParentNode());

 // If a node is an appropriate child node type of another composite node,
 // we can attach it as a child only if both nodes have the same owner document.
 // The owner document is the document we passed to the node's constructor.
 // We have not attached this paragraph to the document, so the document does not contain its text.
 Assert.assertEquals(para.getDocument(), doc);
 Assert.assertEquals("", doc.getText().trim());

 // Since the document owns this paragraph, we can apply one of its styles to the paragraph's contents.
 para.getParagraphFormat().setStyleName("Heading 1");

 // Add this node to the document, and then verify its contents.
 doc.getFirstSection().getBody().appendChild(para);

 Assert.assertEquals(doc.getFirstSection().getBody(), para.getParentNode());
 Assert.assertEquals("Hello world!", doc.getText().trim());
 
```

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node.

 **Remarks:** 

If there is no preceding node, a  null  is returned.

 **Examples:** 

Shows how to use of methods of Node and CompositeNode to remove a section before the last section in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Section 1 text.");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("Section 2 text.");

 // Both sections are siblings of each other.
 Section lastSection = (Section) doc.getLastChild();
 Section firstSection = (Section) lastSection.getPreviousSibling();

 // Remove a section based on its sibling relationship with another section.
 if (lastSection.getPreviousSibling() != null)
     doc.removeChild(firstSection);

 // The section we removed was the first one, leaving the document with only the second.
 Assert.assertEquals("Section 2 text.", doc.getText().trim());
 
```

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getProtectionType() {#getProtectionType}
```
public int getProtectionType()
```


Gets the currently active document protection type.

 **Remarks:** 

This property allows to retrieve the currently set document protection type. To change the document protection type use the **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** and [unprotect()](../../com.aspose.words/document/\#unprotect) methods.

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection)

 **Examples:** 

Shows how to protect and unprotect a document.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "password");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 // If we open this document with Microsoft Word intending to edit it,
 // we will need to apply the password to get through the protection.
 doc.save(getArtifactsDir() + "Document.Protect.docx");

 // Note that the protection only applies to Microsoft Word users opening our document.
 // We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
 Document protectedDoc = new Document(getArtifactsDir() + "Document.Protect.docx");

 Assert.assertEquals(ProtectionType.READ_ONLY, protectedDoc.getProtectionType());

 DocumentBuilder builder = new DocumentBuilder(protectedDoc);
 builder.writeln("Text added to a protected document.");
 // There are two ways of removing protection from a document.
 // 1 - With no password:
 doc.unprotect();

 Assert.assertEquals(ProtectionType.NO_PROTECTION, doc.getProtectionType());

 doc.protect(ProtectionType.READ_ONLY, "NewPassword");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 doc.unprotect("WrongPassword");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 // 2 - With the correct password:
 doc.unprotect("NewPassword");

 Assert.assertEquals(ProtectionType.NO_PROTECTION, doc.getProtectionType());
 
```

**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**

**Returns:**
int - The currently active document protection type. The returned value is one of [ProtectionType](../../com.aspose.words/protectiontype/) constants.
### getPunctuationKerning() {#getPunctuationKerning}
```
public boolean getPunctuationKerning()
```


Specifies whether kerning applies to both Latin text and punctuation.

**Returns:**
boolean - The corresponding  boolean  value.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

 **Examples:** 

Shows how to delete all the nodes from a range.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRemovePersonalInformation() {#getRemovePersonalInformation}
```
public boolean getRemovePersonalInformation()
```


Gets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

 **Examples:** 

Shows how to enable the removal of personal information during a manual save.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some content with personal information.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 doc.getBuiltInDocumentProperties().setCompany("Placeholder Inc.");

 doc.startTrackRevisions(doc.getBuiltInDocumentProperties().getAuthor(), new Date());
 builder.write("Hello world!");
 doc.stopTrackRevisions();

 // This flag is equivalent to File -> Options -> Trust Center -> Trust Center Settings... ->
 // Privacy Options -> "Remove personal information from file properties on save" in Microsoft Word.
 doc.setRemovePersonalInformation(saveWithoutPersonalInfo);

 // This option will not take effect during a save operation made using Aspose.Words.
 // Personal data will be removed from our document with the flag set when we save it manually using Microsoft Word.
 doc.save(getArtifactsDir() + "Document.RemovePersonalInformation.docx");
 doc = new Document(getArtifactsDir() + "Document.RemovePersonalInformation.docx");

 Assert.assertEquals(saveWithoutPersonalInfo, doc.getRemovePersonalInformation());
 Assert.assertEquals("John Doe", doc.getBuiltInDocumentProperties().getAuthor());
 Assert.assertEquals("Placeholder Inc.", doc.getBuiltInDocumentProperties().getCompany());
 Assert.assertEquals("John Doe", doc.getRevisions().get(0).getAuthor());
 
```

**Returns:**
boolean - A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources are loaded.

 **Examples:** 

Shows how to customize the process of loading external resources into a document.

```

 public void resourceLoadingCallback() throws Exception {
     Document doc = new Document();
     doc.setResourceLoadingCallback(new ImageNameHandler());

     DocumentBuilder builder = new DocumentBuilder(doc);

     // Images usually are inserted using a URI, or a byte array.
     // Every instance of a resource load will call our callback's ResourceLoading method.
     builder.insertImage("Google logo");
     builder.insertImage("Aspose logo");
     builder.insertImage("Watermark");

     Assert.assertEquals(3, doc.getChildNodes(NodeType.SHAPE, true).getCount());

     doc.save(getArtifactsDir() + "DocumentBase.ResourceLoadingCallback.docx");
 }

 /// 
 /// Allows us to load images into a document using predefined shorthands, as opposed to URIs.
 /// This will separate image loading logic from the rest of the document construction.
 /// 
 private static class ImageNameHandler implements IResourceLoadingCallback {
     public int resourceLoading(final ResourceLoadingArgs args) throws URISyntaxException, IOException {
         if (args.getResourceType() == ResourceType.IMAGE) {
             // If this callback encounters one of the image shorthands while loading an image,
             // it will apply unique logic for each defined shorthand instead of treating it as a URI.
             if ("Google logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(new URI("http://www.google.com/images/logos/ps_logo2.png").toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Aspose logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getAsposelogoUri().toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Watermark".equals(args.getOriginalUri())) {
                 InputStream imageStream = new FileInputStream(getImageDir() + "Transparent background logo.png");
                 args.setData(DocumentHelper.getBytesFromStream(imageStream));

                 return ResourceLoadingAction.USER_PROVIDED;
             }
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value.
### getRevisions() {#getRevisions}
```
public RevisionCollection getRevisions()
```


Gets a collection of revisions (tracked changes) that exist in this document.

 **Remarks:** 

The returned collection is a "live" collection, which means if you remove parts of a document that contain revisions, the deleted revisions will automatically disappear from this collection.

 **Examples:** 

Shows how to work with revisions in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normal editing of the document does not count as a revision.
 builder.write("This does not count as a revision. ");

 Assert.assertFalse(doc.hasRevisions());

 // To register our edits as revisions, we need to declare an author, and then start tracking them.
 doc.startTrackRevisions("John Doe", new Date());

 builder.write("This is revision #1. ");

 Assert.assertTrue(doc.hasRevisions());
 Assert.assertEquals(1, doc.getRevisions().getCount());

 // This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
 // The "StartTrackRevisions" method does not affect its value,
 // and the document is tracking revisions programmatically despite it having a value of "false".
 // If we open this document using Microsoft Word, it will not be tracking revisions.
 Assert.assertFalse(doc.getTrackRevisions());

 // We have added text using the document builder, so the first revision is an insertion-type revision.
 Revision revision = doc.getRevisions().get(0);
 Assert.assertEquals("John Doe", revision.getAuthor());
 Assert.assertEquals("This is revision #1. ", revision.getParentNode().getText());
 Assert.assertEquals(RevisionType.INSERTION, revision.getRevisionType());
 Assert.assertEquals(revision.getDateTime().getDate(), new Date().getDate());
 Assert.assertEquals(doc.getRevisions().getGroups().get(0), revision.getGroup());

 // Remove a run to create a deletion-type revision.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();

 // Adding a new revision places it at the beginning of the revision collection.
 Assert.assertEquals(RevisionType.DELETION, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(2, doc.getRevisions().getCount());

 // Insert revisions show up in the document body even before we accept/reject the revision.
 // Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
 // also linger in the document until we accept the revision.
 Assert.assertEquals("This does not count as a revision. This is revision #1.", doc.getText().trim());

 // Accepting the delete revision will remove its parent node from the paragraph text
 // and then remove the collection's revision itself.
 doc.getRevisions().get(0).accept();

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1.", doc.getText().trim());

 builder.writeln("");
 builder.write("This is revision #2.");

 // Now move the node to create a moving revision type.
 Node node = doc.getFirstSection().getBody().getParagraphs().get(1);
 Node endNode = doc.getFirstSection().getBody().getParagraphs().get(1).getNextSibling();
 Node referenceNode = doc.getFirstSection().getBody().getParagraphs().get(0);

 while (node != endNode)
 {
     Node nextNode = node.getNextSibling();
     doc.getFirstSection().getBody().insertBefore(node, referenceNode);
     node = nextNode;
 }

 Assert.assertEquals(RevisionType.MOVING, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(8, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.getText().trim());

 // The moving revision is now at index 1. Reject the revision to discard its contents.
 doc.getRevisions().get(1).reject();

 Assert.assertEquals(6, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1. \rThis is revision #2.", doc.getText().trim());
 
```

**Returns:**
[RevisionCollection](../../com.aspose.words/revisioncollection/) - A collection of revisions (tracked changes) that exist in this document.
### getRevisionsView() {#getRevisionsView}
```
public int getRevisionsView()
```


Gets a value indicating whether to work with the original or revised version of a document.

 **Remarks:** 

The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview/\#ORIGINAL)** .

 **Examples:** 

Shows how to switch between the revised and the original view of a document.

```

 Document doc = new Document(getMyDir() + "Revisions at list levels.docx");
 doc.updateListLabels();

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("1.", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("", paragraphs.get(2).getListLabel().getLabelString());

 // View the document object as if all the revisions are accepted. Currently supports list labels.
 doc.setRevisionsView(RevisionsView.FINAL);

 Assert.assertEquals("", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("1.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(2).getListLabel().getLabelString());
 
```

**Returns:**
int - A value indicating whether to work with the original or revised version of a document. The returned value is one of [RevisionsView](../../com.aspose.words/revisionsview/) constants.
### getSections() {#getSections}
```
public SectionCollection getSections()
```


Returns a collection that represents all sections in the document.

 **Examples:** 

Shows how to add and remove sections in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Section 1");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Section 2");

 Assert.assertEquals("Section 1\fSection 2", doc.getText().trim());

 // Delete the first section from the document.
 doc.getSections().removeAt(0);

 Assert.assertEquals("Section 2", doc.getText().trim());

 // Append a copy of what is now the first section to the end of the document.
 int lastSectionIdx = doc.getSections().getCount() - 1;
 Section newSection = doc.getSections().get(lastSectionIdx).deepClone();
 doc.getSections().add(newSection);

 Assert.assertEquals("Section 2\fSection 2", doc.getText().trim());
 
```

Shows how to specify how a new section separates itself from the previous.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

**Returns:**
[SectionCollection](../../com.aspose.words/sectioncollection/) - A collection that represents all sections in the document.
### getShadeFormData() {#getShadeFormData}
```
public boolean getShadeFormData()
```


Specifies whether to turn on the gray shading on form fields.

 **Examples:** 

Shows how to apply gray shading to form fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Hello world! ");
 builder.insertTextInput("My form field", TextFormFieldType.REGULAR, "",
         "Text contents of form field, which are shaded in grey by default.", 0);

 // We can turn the grey shading off, so the bookmarked text will blend in with the other text.
 doc.setShadeFormData(useGreyShading);
 doc.save(getArtifactsDir() + "Document.ShadeFormData.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowGrammaticalErrors() {#getShowGrammaticalErrors}
```
public boolean getShowGrammaticalErrors()
```


Specifies whether to display grammar errors in this document.

 **Examples:** 

Shows how to show/hide errors in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two sentences with mistakes that would be picked up
 // by the spelling and grammar checkers in Microsoft Word.
 builder.writeln("There is a speling error in this sentence.");
 builder.writeln("Their is a grammatical error in this sentence.");

 // If these options are enabled, then spelling errors will be underlined
 // in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
 doc.setShowGrammaticalErrors(showErrors);
 doc.setShowSpellingErrors(showErrors);

 doc.save(getArtifactsDir() + "Document.SpellingAndGrammarErrors.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowSpellingErrors() {#getShowSpellingErrors}
```
public boolean getShowSpellingErrors()
```


Specifies whether to display spelling errors in this document.

 **Examples:** 

Shows how to show/hide errors in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two sentences with mistakes that would be picked up
 // by the spelling and grammar checkers in Microsoft Word.
 builder.writeln("There is a speling error in this sentence.");
 builder.writeln("Their is a grammatical error in this sentence.");

 // If these options are enabled, then spelling errors will be underlined
 // in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
 doc.setShowGrammaticalErrors(showErrors);
 doc.setShowSpellingErrors(showErrors);

 doc.save(getArtifactsDir() + "Document.SpellingAndGrammarErrors.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getSpellingChecked() {#getSpellingChecked}
```
public boolean getSpellingChecked()
```


Returns  true  if the document has been checked for spelling.

 **Remarks:** 

To recheck the spelling in the document, set this property to  false .

 **Examples:** 

Shows how to set spelling or grammar verifying.

```

 Document doc = new Document();

 // The string with spelling errors.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().add(new Run(doc, "The speeling in this documentz is all broked."));

 // Spelling/Grammar check start if we set properties to false.
 // We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
 // Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
 doc.setSpellingChecked(checkSpellingGrammar);
 doc.setGrammarChecked(checkSpellingGrammar);

 doc.save(getArtifactsDir() + "Document.SpellingOrGrammar.docx");
 
```

**Returns:**
boolean -  true  if the document has been checked for spelling.
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Returns a collection of styles defined in the document.

 **Remarks:** 

For more information see the description of the [StyleCollection](../../com.aspose.words/stylecollection/) class.

 **Examples:** 

Shows how to access a document's style collection.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - A collection of styles defined in the document.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

 **Remarks:** 

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Shows the difference between calling the GetText and ToString methods on a node.

```

 Document doc = new Document();

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertField("MERGEFIELD Field");

 // GetText will retrieve the visible text as well as field codes and special characters.
 Assert.assertEquals("MERGEFIELD Field«Field»\f", doc.getText());

 // ToString will give us the document's appearance if saved to a passed save format.
 Assert.assertEquals("«Field»\r\n", doc.toString(SaveFormat.TEXT));
 
```

Shows how to output all paragraphs in a document that are list items.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
java.lang.String
### getTheme() {#getTheme}
```
public Theme getTheme()
```


Gets the [getTheme()](../../com.aspose.words/document/\#getTheme) object for this document.

 **Examples:** 

Shows how to set custom colors and fonts for themes.

```

 Document doc = new Document(getMyDir() + "Theme colors.docx");

 // The "Theme" object gives us access to the document theme, a source of default fonts and colors.
 Theme theme = doc.getTheme();

 // Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
 theme.getMajorFonts().setLatin("Courier New");
 theme.getMinorFonts().setLatin("Agency FB");

 // Other languages may also have their custom fonts in this theme.
 Assert.assertEquals(theme.getMajorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMajorFonts().getEastAsian(), "");
 Assert.assertEquals(theme.getMinorFonts().getComplexScript(), "");
 Assert.assertEquals(theme.getMinorFonts().getEastAsian(), "");

 // The "Colors" property contains the color palette from Microsoft Word,
 // which appears when changing shading or font color.
 // Apply custom colors to the color palette so we have easy access to them in Microsoft Word
 // when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
 // or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
 ThemeColors colors = theme.getColors();
 colors.setDark1(Color.BLUE);
 colors.setLight1(Color.GREEN);
 colors.setDark2(Color.MAGENTA);
 colors.setLight2(Color.BLACK);

 colors.setAccent1(Color.RED);
 colors.setAccent2(Color.PINK);
 colors.setAccent3(Color.YELLOW);
 colors.setAccent4(Color.orange);
 colors.setAccent5(Color.cyan);
 colors.setAccent6(Color.darkGray);

 // Apply custom colors to hyperlinks in their clicked and un-clicked states.
 colors.setHyperlink(Color.WHITE);
 colors.setFollowedHyperlink(Color.lightGray);

 doc.save(getArtifactsDir() + "Themes.CustomColorsAndFonts.docx");
 
```

**Returns:**
[Theme](../../com.aspose.words/theme/) - The [getTheme()](../../com.aspose.words/document/\#getTheme) object for this document.
### getTrackRevisions() {#getTrackRevisions}
```
public boolean getTrackRevisions()
```


True if changes are tracked when this document is edited in Microsoft Word.

 **Remarks:** 

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document/\#startTrackRevisions-java.lang.String--java.util.Date) method.

 **Examples:** 

Shows how to work with revisions in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normal editing of the document does not count as a revision.
 builder.write("This does not count as a revision. ");

 Assert.assertFalse(doc.hasRevisions());

 // To register our edits as revisions, we need to declare an author, and then start tracking them.
 doc.startTrackRevisions("John Doe", new Date());

 builder.write("This is revision #1. ");

 Assert.assertTrue(doc.hasRevisions());
 Assert.assertEquals(1, doc.getRevisions().getCount());

 // This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
 // The "StartTrackRevisions" method does not affect its value,
 // and the document is tracking revisions programmatically despite it having a value of "false".
 // If we open this document using Microsoft Word, it will not be tracking revisions.
 Assert.assertFalse(doc.getTrackRevisions());

 // We have added text using the document builder, so the first revision is an insertion-type revision.
 Revision revision = doc.getRevisions().get(0);
 Assert.assertEquals("John Doe", revision.getAuthor());
 Assert.assertEquals("This is revision #1. ", revision.getParentNode().getText());
 Assert.assertEquals(RevisionType.INSERTION, revision.getRevisionType());
 Assert.assertEquals(revision.getDateTime().getDate(), new Date().getDate());
 Assert.assertEquals(doc.getRevisions().getGroups().get(0), revision.getGroup());

 // Remove a run to create a deletion-type revision.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();

 // Adding a new revision places it at the beginning of the revision collection.
 Assert.assertEquals(RevisionType.DELETION, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(2, doc.getRevisions().getCount());

 // Insert revisions show up in the document body even before we accept/reject the revision.
 // Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
 // also linger in the document until we accept the revision.
 Assert.assertEquals("This does not count as a revision. This is revision #1.", doc.getText().trim());

 // Accepting the delete revision will remove its parent node from the paragraph text
 // and then remove the collection's revision itself.
 doc.getRevisions().get(0).accept();

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1.", doc.getText().trim());

 builder.writeln("");
 builder.write("This is revision #2.");

 // Now move the node to create a moving revision type.
 Node node = doc.getFirstSection().getBody().getParagraphs().get(1);
 Node endNode = doc.getFirstSection().getBody().getParagraphs().get(1).getNextSibling();
 Node referenceNode = doc.getFirstSection().getBody().getParagraphs().get(0);

 while (node != endNode)
 {
     Node nextNode = node.getNextSibling();
     doc.getFirstSection().getBody().insertBefore(node, referenceNode);
     node = nextNode;
 }

 Assert.assertEquals(RevisionType.MOVING, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(8, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.getText().trim());

 // The moving revision is now at index 1. Reject the revision to discard its contents.
 doc.getRevisions().get(1).reject();

 Assert.assertEquals(6, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1. \rThis is revision #2.", doc.getText().trim());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getVariables() {#getVariables}
```
public VariableCollection getVariables()
```


Returns the collection of variables added to a document or template.

 **Examples:** 

Shows how to work with a document's variable collection.

```

 Document doc = new Document();
 VariableCollection variables = doc.getVariables();

 // Every document has a collection of key/value pair variables, which we can add items to.
 variables.add("Home address", "123 Main St.");
 variables.add("City", "London");
 variables.add("Bedrooms", "3");

 Assert.assertEquals(3, variables.getCount());

 // We can display the values of variables in the document body using DOCVARIABLE fields.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocVariable field = (FieldDocVariable) builder.insertField(FieldType.FIELD_DOC_VARIABLE, true);
 field.setVariableName("Home address");
 field.update();

 Assert.assertEquals("123 Main St.", field.getResult());

 // Assigning values to existing keys will update them.
 variables.add("Home address", "456 Queen St.");

 // We will then have to update DOCVARIABLE fields to ensure they display an up-to-date value.
 Assert.assertEquals("123 Main St.", field.getResult());

 field.update();

 Assert.assertEquals("456 Queen St.", field.getResult());

 // Verify that the document variables with a certain name or value exist.
 Assert.assertTrue(variables.contains("City"));
 Assert.assertTrue(IterableUtils.matchesAny(variables, s -> s.getValue() == "London"));

 // The collection of variables automatically sorts variables alphabetically by name.
 Assert.assertEquals(0, variables.indexOfKey("Bedrooms"));
 Assert.assertEquals(1, variables.indexOfKey("City"));
 Assert.assertEquals(2, variables.indexOfKey("Home address"));

 // Below are three ways of removing document variables from a collection.
 // 1 -  By name:
 variables.remove("City");

 Assert.assertFalse(variables.contains("City"));

 // 2 -  By index:
 variables.removeAt(1);

 Assert.assertFalse(variables.contains("Home address"));

 // 3 -  Clear the whole collection at once:
 variables.clear();

 Assert.assertEquals(variables.getCount(), 0);
 
```

**Returns:**
[VariableCollection](../../com.aspose.words/variablecollection/) - The collection of variables added to a document or template.
### getVbaProject() {#getVbaProject}
```
public VbaProject getVbaProject()
```


Gets a [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject).

 **Examples:** 

Shows how to access a document's VBA project information.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```

**Returns:**
[VbaProject](../../com.aspose.words/vbaproject/) - A [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject).
### getVersionsCount() {#getVersionsCount}
```
public int getVersionsCount()
```


Gets the number of document versions that was stored in the DOC document.

 **Remarks:** 

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports versions only for DOC files.

This property allows to detect if there were document versions stored in this document before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions. If you save this document using Aspose.Words, the document will be saved without versions.

 **Examples:** 

Shows how to work with the versions count feature of older Microsoft Word documents.

```

 Document doc = new Document(getMyDir() + "Versions.doc");

 // We can read this property of a document, but we cannot preserve it while saving.
 Assert.assertEquals(4, doc.getVersionsCount());

 doc.save(getArtifactsDir() + "Document.VersionsCount.doc");
 doc = new Document(getArtifactsDir() + "Document.VersionsCount.doc");

 Assert.assertEquals(0, doc.getVersionsCount());
 
```

**Returns:**
int - The number of document versions that was stored in the DOC document.
### getViewOptions() {#getViewOptions}
```
public ViewOptions getViewOptions()
```


Provides options to control how the document is displayed in Microsoft Word.

 **Examples:** 

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.getViewOptions().setViewType(ViewType.PAGE_LAYOUT);
 doc.getViewOptions().setZoomPercent(50);

 Assert.assertEquals(ZoomType.CUSTOM, doc.getViewOptions().getZoomType());
 Assert.assertEquals(ZoomType.NONE, doc.getViewOptions().getZoomType());

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomPercentage.doc");
 
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
 // to automatically zoom the document to fit the width of the page.
 // Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
 // to automatically zoom the document to make the entire first page visible.
 // Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
 // to automatically zoom the document to fit the inner text margins of the first page.
 doc.getViewOptions().setZoomType(zoomType);

 doc.save(getArtifactsDir() + "ViewOptions.SetZoomType.doc");
 
```

**Returns:**
[ViewOptions](../../com.aspose.words/viewoptions/) - The corresponding [ViewOptions](../../com.aspose.words/viewoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.

 **Remarks:** 

Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document/\#getPageCount) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

 **Examples:** 

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```

 public void substitutionWarning() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Times New Roman");
     builder.writeln("Hello world!");

     FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
     doc.setWarningCallback(callback);

     // Store the current collection of font sources, which will be the default font source for every document
     // for which we do not specify a different font source.
     FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

     // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
     FontSettings.getDefaultInstance().setFontsFolder("", false);

     // When rendering the document, there will be no place to find the "Times New Roman" font.
     // This will cause a font substitution warning, which our callback will detect.
     doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarning.pdf");

     FontSettings.getDefaultInstance().setFontsSources(originalFontSources);

     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getWarningType() == WarningType.FONT_SUBSTITUTION);
     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getDescription()
             .equals("Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
 }

 private static class FontSubstitutionWarningCollector implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```

 public void enableFontSubstitution() throws Exception {
     // Open a document that contains text formatted with a font that does not exist in any of our font sources.
     Document doc = new Document(getMyDir() + "Missing font.docx");

     // Assign a callback for handling font substitution warnings.
     HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
     doc.setWarningCallback(substitutionWarningHandler);

     // Set a default font name and enable font substitution.
     FontSettings fontSettings = new FontSettings();
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

     // Original font metrics should be used after font substitution.
     doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

     // We will get a font substitution warning if we save a document with a missing font.
     doc.setFontSettings(fontSettings);
     doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

     Iterator warnings = substitutionWarningHandler.FontWarnings.iterator();

     while (warnings.hasNext())
         System.out.println(warnings.next().getDescription());

     // We can also verify warnings in the collection and clear them.
     Assert.assertEquals(WarningSource.LAYOUT, substitutionWarningHandler.FontWarnings.get(0).getSource());
     Assert.assertEquals("Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
             substitutionWarningHandler.FontWarnings.get(0).getDescription());

     substitutionWarningHandler.FontWarnings.clear();

     Assert.assertTrue(substitutionWarningHandler.FontWarnings.getCount() == 0);
 }

 public static class HandleDocumentSubstitutionWarnings implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontWarnings.warning(info);
     }

     public WarningInfoCollection FontWarnings = new WarningInfoCollection();
 }
 
```

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### getWatermark() {#getWatermark}
```
public Watermark getWatermark()
```


Provides access to the document watermark.

 **Examples:** 

Shows how to create a text watermark.

```

 Document doc = new Document();

 // Add a plain text watermark.
 doc.getWatermark().setText("Aspose Watermark");

 // If we wish to edit the text formatting using it as a watermark,
 // we can do so by passing a TextWatermarkOptions object when creating the watermark.
 TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
 textWatermarkOptions.setFontFamily("Arial");
 textWatermarkOptions.setFontSize(36f);
 textWatermarkOptions.setColor(Color.BLACK);
 textWatermarkOptions.setLayout(WatermarkLayout.DIAGONAL);
 textWatermarkOptions.isSemitrasparent(false);

 doc.getWatermark().setText("Aspose Watermark", textWatermarkOptions);

 doc.save(getArtifactsDir() + "Document.TextWatermark.docx");

 // We can remove a watermark from a document like this.
 if (doc.getWatermark().getType() == WatermarkType.TEXT)
     doc.getWatermark().remove();
 
```

**Returns:**
[Watermark](../../com.aspose.words/watermark/) - The corresponding [Watermark](../../com.aspose.words/watermark/) value.
### getWebExtensionTaskPanes() {#getWebExtensionTaskPanes}
```
public TaskPaneCollection getWebExtensionTaskPanes()
```


Returns a collection that represents a list of task pane add-ins.

 **Examples:** 

Shows how to add a web extension to a document.

```

 Document doc = new Document();

 // Create task pane with "MyScript" add-in, which will be used by the document,
 // then set its default location.
 TaskPane myScriptTaskPane = new TaskPane();
 doc.getWebExtensionTaskPanes().add(myScriptTaskPane);
 myScriptTaskPane.setDockState(TaskPaneDockState.RIGHT);
 myScriptTaskPane.isVisible(true);
 myScriptTaskPane.setWidth(300.0);
 myScriptTaskPane.isLocked(true);

 // If there are multiple task panes in the same docking location, we can set this index to arrange them.
 myScriptTaskPane.setRow(1);

 // Create an add-in called "MyScript Math Sample", which the task pane will display within.
 WebExtension webExtension = myScriptTaskPane.getWebExtension();

 // Set application store reference parameters for our add-in, such as the ID.
 webExtension.getReference().setId("WA104380646");
 webExtension.getReference().setVersion("1.0.0.0");
 webExtension.getReference().setStoreType(WebExtensionStoreType.OMEX);
 webExtension.getReference().setStore("English (United States)");
 webExtension.getProperties().add(new WebExtensionProperty("MyScript", "MyScript Math Sample"));
 webExtension.getBindings().add(new WebExtensionBinding("MyScript", WebExtensionBindingType.TEXT, "104380646"));

 // Allow the user to interact with the add-in.
 webExtension.isFrozen(false);

 // We can access the web extension in Microsoft Word via Developer -> Add-ins.
 doc.save(getArtifactsDir() + "Document.WebExtension.docx");

 // Remove all web extension task panes at once like this.
 doc.getWebExtensionTaskPanes().clear();

 Assert.assertEquals(0, doc.getWebExtensionTaskPanes().getCount());
 
```

**Returns:**
[TaskPaneCollection](../../com.aspose.words/taskpanecollection/) - A collection that represents a list of task pane add-ins.
### getWriteProtection() {#getWriteProtection}
```
public WriteProtection getWriteProtection()
```


Provides access to the document write protection options.

 **Examples:** 

Shows how to protect a document with a password.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world! This document is protected.");
 // Enter a password up to 15 characters in length, and then verify the document's protection status.
 doc.getWriteProtection().setPassword("MyPassword");
 doc.getWriteProtection().setReadOnlyRecommended(true);

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());
 Assert.assertTrue(doc.getWriteProtection().validatePassword("MyPassword"));

 // Protection does not prevent the document from being edited programmatically, nor does it encrypt the contents.
 doc.save(getArtifactsDir() + "Document.WriteProtection.docx");
 doc = new Document(getArtifactsDir() + "Document.WriteProtection.docx");

 Assert.assertTrue(doc.getWriteProtection().isWriteProtected());

 builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln("Writing text in a protected document.");

 Assert.assertEquals("Hello world! This document is protected." +
         "\rWriting text in a protected document.", doc.getText().trim());
 
```

**Returns:**
[WriteProtection](../../com.aspose.words/writeprotection/) - The corresponding [WriteProtection](../../com.aspose.words/writeprotection/) value.
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

 **Examples:** 

Shows how to combine the rows from two tables into one.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // Below are two ways of getting a table from a document.
 // 1 -  From the "Tables" collection of a Body node:
 Table firstTable = doc.getFirstSection().getBody().getTables().get(0);

 // 2 -  Using the "GetChild" method:
 Table secondTable = (Table) doc.getChild(NodeType.TABLE, 1, true);

 // Append all rows from the current table to the next.
 while (secondTable.hasChildNodes())
     firstTable.getRows().add(secondTable.getFirstRow());

 // Remove the empty table container.
 secondTable.remove();

 doc.save(getArtifactsDir() + "Table.CombineTables.docx");
 
```

**Returns:**
boolean -  true  if this node has any child nodes.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Returns  true  if the document has a VBA project (macros).

 **Examples:** 

Shows how to use MACROBUTTON fields to allow us to run a document's macros by clicking.

```

 Document doc = new Document(getMyDir() + "Macro.docm");
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertTrue(doc.hasMacros());

 // Insert a MACROBUTTON field, and reference one of the document's macros by name in the MacroName property.
 FieldMacroButton field = (FieldMacroButton) builder.insertField(FieldType.FIELD_MACRO_BUTTON, true);
 field.setMacroName("MyMacro");
 field.setDisplayText("Double click to run macro: " + field.getMacroName());

 Assert.assertEquals(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.getFieldCode());

 // Use the property to reference "ViewZoom200", a macro that ships with Microsoft Word.
 // We can find all other macros via View -> Macros (dropdown) -> View Macros.
 // In that menu, select "Word Commands" from the "Macros in:" drop down.
 // If our document contains a custom macro with the same name as a stock macro,
 // our macro will be the one that the MACROBUTTON field runs.
 builder.insertParagraph();
 field = (FieldMacroButton) builder.insertField(FieldType.FIELD_MACRO_BUTTON, true);
 field.setMacroName("ViewZoom200");
 field.setDisplayText("Run " + field.getMacroName());

 Assert.assertEquals(field.getFieldCode(), " MACROBUTTON  ViewZoom200 Run ViewZoom200");

 // Save the document as a macro-enabled document type.
 doc.save(getArtifactsDir() + "Field.MACROBUTTON.docm");
 
```

**Returns:**
boolean -  true  if the document has a VBA project (macros).
### hasRevisions() {#hasRevisions}
```
public boolean hasRevisions()
```


Returns  true  if the document has any tracked changes.

 **Remarks:** 

This property is a shortcut for comparing [RevisionCollection.getCount()](../../com.aspose.words/revisioncollection/\#getCount) to zero.

 **Examples:** 

Shows how to work with revisions in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normal editing of the document does not count as a revision.
 builder.write("This does not count as a revision. ");

 Assert.assertFalse(doc.hasRevisions());

 // To register our edits as revisions, we need to declare an author, and then start tracking them.
 doc.startTrackRevisions("John Doe", new Date());

 builder.write("This is revision #1. ");

 Assert.assertTrue(doc.hasRevisions());
 Assert.assertEquals(1, doc.getRevisions().getCount());

 // This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
 // The "StartTrackRevisions" method does not affect its value,
 // and the document is tracking revisions programmatically despite it having a value of "false".
 // If we open this document using Microsoft Word, it will not be tracking revisions.
 Assert.assertFalse(doc.getTrackRevisions());

 // We have added text using the document builder, so the first revision is an insertion-type revision.
 Revision revision = doc.getRevisions().get(0);
 Assert.assertEquals("John Doe", revision.getAuthor());
 Assert.assertEquals("This is revision #1. ", revision.getParentNode().getText());
 Assert.assertEquals(RevisionType.INSERTION, revision.getRevisionType());
 Assert.assertEquals(revision.getDateTime().getDate(), new Date().getDate());
 Assert.assertEquals(doc.getRevisions().getGroups().get(0), revision.getGroup());

 // Remove a run to create a deletion-type revision.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();

 // Adding a new revision places it at the beginning of the revision collection.
 Assert.assertEquals(RevisionType.DELETION, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(2, doc.getRevisions().getCount());

 // Insert revisions show up in the document body even before we accept/reject the revision.
 // Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
 // also linger in the document until we accept the revision.
 Assert.assertEquals("This does not count as a revision. This is revision #1.", doc.getText().trim());

 // Accepting the delete revision will remove its parent node from the paragraph text
 // and then remove the collection's revision itself.
 doc.getRevisions().get(0).accept();

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1.", doc.getText().trim());

 builder.writeln("");
 builder.write("This is revision #2.");

 // Now move the node to create a moving revision type.
 Node node = doc.getFirstSection().getBody().getParagraphs().get(1);
 Node endNode = doc.getFirstSection().getBody().getParagraphs().get(1).getNextSibling();
 Node referenceNode = doc.getFirstSection().getBody().getParagraphs().get(0);

 while (node != endNode)
 {
     Node nextNode = node.getNextSibling();
     doc.getFirstSection().getBody().insertBefore(node, referenceNode);
     node = nextNode;
 }

 Assert.assertEquals(RevisionType.MOVING, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(8, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.getText().trim());

 // The moving revision is now at index 1. Reject the revision to discard its contents.
 doc.getRevisions().get(1).reject();

 Assert.assertEquals(6, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1. \rThis is revision #2.", doc.getText().trim());
 
```

**Returns:**
boolean -  true  if the document has any tracked changes.
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Imports a node from another document to the current document.

Imports a node from another document to the current document.

 **Remarks:** 

This method uses the [ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using **M:Aspose.Words.CompositeNode.InsertBefore1(0,Aspose.Words.Node)** or **M:Aspose.Words.CompositeNode.InsertAfter1(0,Aspose.Words.Node)**.

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

 **Examples:** 

Shows how to import a node from one document to another.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 srcDoc.getFirstSection().getBody().getFirstParagraph().appendChild(
         new Run(srcDoc, "Source document first paragraph text."));
 dstDoc.getFirstSection().getBody().getFirstParagraph().appendChild(
         new Run(dstDoc, "Destination document first paragraph text."));

 // Every node has a parent document, which is the document that contains the node.
 // Inserting a node into a document that the node does not belong to will throw an exception.
 Assert.assertNotEquals(dstDoc, srcDoc.getFirstSection().getDocument());
 Assert.assertThrows(IllegalArgumentException.class, () -> dstDoc.appendChild(srcDoc.getFirstSection()));

 // Use the ImportNode method to create a copy of a node, which will have the document
 // that called the ImportNode method set as its new owner document.
 Section importedSection = (Section) dstDoc.importNode(srcDoc.getFirstSection(), true);

 Assert.assertEquals(dstDoc, importedSection.getDocument());

 // We can now insert the node into the document.
 dstDoc.appendChild(importedSection);

 Assert.assertEquals("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
         dstDoc.toString(SaveFormat.TEXT));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | The node being imported. |
| isImportChildren | boolean |  true  to import all child nodes recursively; otherwise,  false . |

**Returns:**
[Node](../../com.aspose.words/node/) - The cloned node that belongs to the current document.
### importNode(Node srcNode, boolean isImportChildren, int importFormatMode) {#importNode-com.aspose.words.Node-boolean-int}
```
public Node importNode(Node srcNode, boolean isImportChildren, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) |  |
| isImportChildren | boolean |  |
| importFormatMode | int |  |

**Returns:**
[Node](../../com.aspose.words/node/)
### indexOf(Node child) {#indexOf-com.aspose.words.Node}
```
public int indexOf(Node child)
```


Returns the index of the specified child node in the child node array.

 **Remarks:** 

Returns -1 if the node is not found in the child nodes.

 **Examples:** 

Shows how to get the index of a given child node from its parent.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 Body body = doc.getFirstSection().getBody();

 // Retrieve the index of the last paragraph in the body of the first section.
 Assert.assertEquals(24, body.getChildNodes(NodeType.ANY, false).indexOf(body.getLastParagraph()));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

 **Examples:** 

Shows how to traverse a composite node's tree of child nodes.

```

 public void recurseChildren() throws Exception {
     Document doc = new Document(getMyDir() + "Paragraphs.docx");

     // Any node that can contain child nodes, such as the document itself, is composite.
     Assert.assertTrue(doc.isComposite());

     // Invoke the recursive function that will go through and print all the child nodes of a composite node.
     traverseAllNodes(doc, 0);
 }

 /// 
 /// Recursively traverses a node tree while printing the type of each node
 /// with an indent depending on depth as well as the contents of all inline nodes.
 /// 
 public void traverseAllNodes(CompositeNode parentNode, int depth) {
     for (Node childNode = parentNode.getFirstChild(); childNode != null; childNode = childNode.getNextSibling()) {
         System.out.println(MessageFormat.format("{0}{1}", String.format("    ", depth), Node.nodeTypeToString(childNode.getNodeType())));

         // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
         if (childNode.isComposite()) {
             System.out.println();
             traverseAllNodes((CompositeNode) childNode, depth + 1);
         } else if (childNode instanceof Inline) {
             System.out.println(MessageFormat.format(" - \"{0}\"", childNode.getText().trim()));
         } else {
             System.out.println();
         }
     }
 }
 
```

**Returns:**
boolean -  true  as this node can have child nodes.
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

 **Examples:** 

Shows how to print all of a document's comments and their replies.

```

 Document doc = new Document(getMyDir() + "Comments.docx");

 NodeCollection comments = doc.getChildNodes(NodeType.COMMENT, true);
 // If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
 // Print all top-level comments along with any replies they may have.
 for (Comment comment : (Iterable) comments) {
     if (comment.getAncestor() == null) {
         System.out.println("Top-level comment:");
         System.out.println("\t\"{comment.GetText().Trim()}\", by {comment.Author}");
         System.out.println("Has {comment.Replies.Count} replies");
         for (Comment commentReply : comment.getReplies()) {
             System.out.println("\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
         }
         System.out.println();
     }
 }
 
```

**Returns:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting}
```
public int joinRunsWithSameFormatting()
```


Joins runs with same formatting in all paragraphs of the document.

 **Remarks:** 

This is an optimization method. Some documents contain adjacent runs with same formatting. Usually this occurs if a document was intensively edited manually. You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../com.aspose.words/paragraph/) node in the document for adjacent [Run](../../com.aspose.words/run/) nodes having identical properties. It ignores unique identifiers used to track editing sessions of run creation and modification. First run in every joining sequence accumulates all text. Remaining runs are deleted from the document.

 **Examples:** 

Shows how to join runs in a document to reduce unneeded runs.

```

 // Open a document that contains adjacent runs of text with identical formatting,
 // which commonly occurs if we edit the same paragraph multiple times in Microsoft Word.
 Document doc = new Document(getMyDir() + "Rendering.docx");

 // If any number of these runs are adjacent with identical formatting,
 // then the document may be simplified.
 Assert.assertEquals(317, doc.getChildNodes(NodeType.RUN, true).getCount());

 // Combine such runs with this method and verify the number of run joins that will take place.
 Assert.assertEquals(121, doc.joinRunsWithSameFormatting());

 // The number of joins and the number of runs we have after the join
 // should add up the number of runs we had initially.
 Assert.assertEquals(196, doc.getChildNodes(NodeType.RUN, true).getCount());
 
```

**Returns:**
int - Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Next node in pre-order order. Null if reached the  rootNode .
### nodeTypeToString(int nodeType) {#nodeTypeToString-int}
```
public static String nodeTypeToString(int nodeType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### normalizeFieldTypes() {#normalizeFieldTypes}
```
public void normalizeFieldTypes()
```


Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar/\#getFieldType) of [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/) in the whole document so that they correspond to the field types contained in the field codes.

 **Remarks:** 

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [Range.normalizeFieldTypes()](../../com.aspose.words/range/\#normalizeFieldTypes).

 **Examples:** 

Shows how to get the keep a field's type up to date with its field code.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field field = builder.insertField("DATE", null);

 // Aspose.Words automatically detects field types based on field codes.
 Assert.assertEquals(FieldType.FIELD_DATE, field.getType());

 // Manually change the raw text of the field, which determines the field code.
 Run fieldText = (Run) doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.RUN, true).get(0);
 fieldText.setText("PAGE");

 // Changing the field code has changed this field to one of a different type,
 // but the field's type properties still display the old type.
 Assert.assertEquals("PAGE", field.getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getType());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getStart().getFieldType());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getSeparator().getFieldType());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getEnd().getFieldType());

 // Update those properties with this method to display current value.
 doc.normalizeFieldTypes();

 Assert.assertEquals(FieldType.FIELD_PAGE, field.getType());
 Assert.assertEquals(FieldType.FIELD_PAGE, field.getStart().getFieldType());
 Assert.assertEquals(FieldType.FIELD_PAGE, field.getSeparator().getFieldType());
 Assert.assertEquals(FieldType.FIELD_PAGE, field.getEnd().getFieldType());
 
```

### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

 **Examples:** 

Shows how to traverse the document's node tree using the pre-order traversal algorithm, and delete any encountered shape with an image.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 Node curNode = doc;
 while (curNode != null) {
     Node nextNode = curNode.nextPreOrder(doc);

     if (curNode.previousPreOrder(doc) != null && nextNode != null)
         Assert.assertEquals(curNode, nextNode.previousPreOrder(doc));

     if (curNode.getNodeType() == NodeType.SHAPE && ((Shape) curNode).hasImage())
         curNode.remove();

     curNode = nextNode;
 }

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| rootNode | [Node](../../com.aspose.words/node/) | The top node (limit) of traversal. |

**Returns:**
[Node](../../com.aspose.words/node/) - Previous node in pre-order order. Null if reached the  rootNode .
### print() {#print}
```
public void print()
```


Prints the document without bringing up any user interface forms.  Prints the whole document to the default printer.

### print(String printerName) {#print-java.lang.String}
```
public void print(String printerName)
```


Print the whole document to the specified printer, using the standard (no User Interface) print controller.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| printerName | java.lang.String | The name of the printer. |

### print(AttributeSet printerSettings) {#print-javax.print.attribute.AttributeSet}
```
public void print(AttributeSet printerSettings)
```


Prints the document according to the specified printer settings, using the standard (no User Interface) print controller.

 **Remarks:** 

The javax.print.attribute.AttributeSet object allows you to specify the printer to print on, the range of pages of to print and other options.

The **javax.print.attribute.AttributeSet** can contain both **javax.print.attribute.PrintRequestAttribute** to configure PrintJob request and **javax.print.attribute.PrintServiceAttribute** to configure PrintService lookup.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | The printer settings to use. |

### print(AttributeSet printerSettings, String documentName) {#print-javax.print.attribute.AttributeSet-java.lang.String}
```
public void print(AttributeSet printerSettings, String documentName)
```


Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name.

 **Remarks:** 

The javax.print.attribute.AttributeSet object allows you to specify the printer to print on, the range of pages of to print and other options.

The **javax.print.attribute.AttributeSet** can contain both **javax.print.attribute.PrintRequestAttribute** to configure PrintJob request and **javax.print.attribute.PrintServiceAttribute** to configure PrintService lookup.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | The printer settings to use. |
| documentName | java.lang.String | The document name to display (for example, in a print status dialog box or printer queue) while printing the document. |

### protect(int type) {#protect-int}
```
public void protect(int type)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | int |  |

### protect(int type, String password) {#protect-int-java.lang.String}
```
public void protect(int type, String password)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | int |  |
| password | java.lang.String |  |

### remove() {#remove}
```
public void remove()
```


Removes itself from the parent.

 **Examples:** 

Shows how to remove all child nodes of a specific type from a composite node.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 Node curNode = doc.getFirstSection().getBody().getFirstChild();

 while (curNode != null) {
     // Save the next sibling node as a variable in case we want to move to it after deleting this node.
     Node nextNode = curNode.getNextSibling();

     // A section body can contain Paragraph and Table nodes.
     // If the node is a Table, remove it from the parent.
     if (curNode.getNodeType() == NodeType.TABLE) {
         curNode.remove();
     }

     curNode = nextNode;
 }

 Assert.assertEquals(0, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```

Shows how to delete all shapes with images from a document.

```

 Document doc = new Document(getMyDir() + "Images.docx");
 ArrayList shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(9, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));

 for (Shape shape : shapes)
     if (shape.hasImage())
         shape.remove();

 shapes = (ArrayList) IterableUtils.toList(doc.getChildNodes(NodeType.SHAPE, true));

 Assert.assertEquals(0, IterableUtils.countMatches(shapes, s -> {
     try {
         return s.hasImage();
     } catch (Exception e) {
         e.printStackTrace();
     }
     return false;
 }));
 
```

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```

### removeBlankPages() {#removeBlankPages}
```
public ArrayList removeBlankPages()
```


Removes blank pages from the document.

 **Remarks:** 

The resulting document will not contain pages considered to be blank while other content, including numbering, headers/footers and overall layout should remain unchanged. Page is considered to be blank when body of the page have no visible content, for example, empty table having no borders will be considered as invisible and therefore page will be detected as blank.

**Returns:**
java.util.ArrayList - List of page numbers has been considered as blank and removed.
### removeExternalSchemaReferences() {#removeExternalSchemaReferences}
```
public void removeExternalSchemaReferences()
```


Removes external XML schema references from this document.

 **Examples:** 

Shows how to remove all external XML schema references from a document.

```

 Document doc = new Document(getMyDir() + "External XML schema.docx");

 doc.removeExternalSchemaReferences();
 
```

### removeMacros() {#removeMacros}
```
public void removeMacros()
```


Removes all macros (the VBA project) as well as toolbars and command customizations from the document.

 **Remarks:** 

By removing all macros from a document you can ensure the document contains no macro viruses.

 **Examples:** 

Shows how to remove all macros from a document.

```

 Document doc = new Document(getMyDir() + "Macro.docm");

 Assert.assertTrue(doc.hasMacros());
 Assert.assertEquals("Project", doc.getVbaProject().getName());

 // Remove the document's VBA project, along with all its macros.
 doc.removeMacros();

 Assert.assertFalse(doc.hasMacros());
 Assert.assertNull(doc.getVbaProject());
 
```

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node.

 **Remarks:** 

This method does not remove the content of the smart tags.

 **Examples:** 

Removes all smart tags from descendant nodes of a composite node.

```

 Document doc = new Document(getMyDir() + "Smart tags.doc");

 Assert.assertEquals(8, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

 doc.removeSmartTags();

 Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 
```

Shows how to create smart tags.

```

 public void create() throws Exception {
     Document doc = new Document();

     // A smart tag appears in a document with Microsoft Word recognizes a part of its text as some form of data,
     // such as a name, date, or address, and converts it to a hyperlink that displays a purple dotted underline.
     SmartTag smartTag = new SmartTag(doc);

     // Smart tags are composite nodes that contain their recognized text in its entirety.
     // Add contents to this smart tag manually.
     smartTag.appendChild(new Run(doc, "May 29, 2019"));

     // Microsoft Word may recognize the above contents as being a date.
     // Smart tags use the "Element" property to reflect the type of data they contain.
     smartTag.setElement("date");

     // Some smart tag types process their contents further into custom XML properties.
     smartTag.getProperties().add(new CustomXmlProperty("Day", "", "29"));
     smartTag.getProperties().add(new CustomXmlProperty("Month", "", "5"));
     smartTag.getProperties().add(new CustomXmlProperty("Year", "", "2019"));

     // Set the smart tag's URI to the default value.
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a date. "));

     // Create another smart tag for a stock ticker.
     smartTag = new SmartTag(doc);
     smartTag.setElement("stockticker");
     smartTag.setUri("urn:schemas-microsoft-com:office:smarttags");

     smartTag.appendChild(new Run(doc, "MSFT"));

     doc.getFirstSection().getBody().getFirstParagraph().appendChild(smartTag);
     doc.getFirstSection().getBody().getFirstParagraph().appendChild(new Run(doc, " is a stock ticker."));

     // Print all the smart tags in our document using a document visitor.
     doc.accept(new SmartTagPrinter());

     // Older versions of Microsoft Word support smart tags.
     doc.save(getArtifactsDir() + "SmartTag.Create.doc");

     // Use the "RemoveSmartTags" method to remove all smart tags from a document.
     Assert.assertEquals(2, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());

     doc.removeSmartTags();

     Assert.assertEquals(0, doc.getChildNodes(NodeType.SMART_TAG, true).getCount());
 }

 /// 
 /// Prints visited smart tags and their contents.
 /// 
 private static class SmartTagPrinter extends DocumentVisitor {
     /// 
     /// Called when a SmartTag node is encountered in the document.
     /// 
     public int visitSmartTagStart(SmartTag smartTag) {
         System.out.println("Smart tag type: {smartTag.Element}");
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when the visiting of a SmartTag node is ended.
     /// 
     public int visitSmartTagEnd(SmartTag smartTag) {
         System.out.println("\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

         if (smartTag.getProperties().getCount() == 0) {
             System.out.println("\tContains no properties");
         } else {
             System.out.println("\tProperties: ");
             String[] properties = new String[smartTag.getProperties().getCount()];
             int index = 0;

             for (CustomXmlProperty cxp : smartTag.getProperties())
                 properties[index++] = MessageFormat.format("\"{0}\" = \"{1}\"", cxp.getName(), cxp.getValue());

             System.out.println(StringUtils.join(properties, ", "));
         }

         return VisitorAction.CONTINUE;
     }
 }
 
```

### renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale) {#renderToScale-int-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)
```


Renders a document page into a java.awt.Graphics2D object to a specified scale.

 **Examples:** 

Shows how to the individual pages of a document to graphics to create one image with thumbnails of all pages.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Calculate the number of rows and columns that we will fill with thumbnails.
 final int thumbColumns = 2;
 int thumbRows = doc.getPageCount() / thumbColumns;
 int remainder = doc.getPageCount() % thumbColumns;

 if (remainder > 0) thumbRows++;

 // Scale the thumbnails relative to the size of the first page.
 float scale = 0.25f;
 Dimension thumbSize = doc.getPageInfo(0).getSizeInPixels(scale, 96);

 // Calculate the size of the image that will contain all the thumbnails.
 int imgWidth = (int) (thumbSize.getWidth() * thumbColumns);
 int imgHeight = (int) (thumbSize.getHeight() * thumbRows);

 BufferedImage img = new BufferedImage(imgWidth, imgHeight, BufferedImage.TYPE_INT_ARGB);
 Graphics2D gr = img.createGraphics();
 try {
     gr.setRenderingHint(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON);

     gr.setColor(Color.white);
     // Fill the background, which is transparent by default, in white.
     gr.fillRect(0, 0, imgWidth, imgHeight);

     for (int pageIndex = 0; pageIndex < doc.getPageCount(); pageIndex++) {
         int rowIdx = pageIndex / thumbColumns;
         int columnIdx = pageIndex % thumbColumns;

         // Specify where we want the thumbnail to appear.
         float thumbLeft = (float) (columnIdx * thumbSize.getWidth());
         float thumbTop = (float) (rowIdx * thumbSize.getHeight());

         Point2D.Float size = doc.renderToScale(pageIndex, gr, thumbLeft, thumbTop, scale);

         gr.setColor(Color.black);

         // Render a page as a thumbnail, and then frame it in a rectangle of the same size.
         gr.drawRect((int) thumbLeft, (int) thumbTop, (int) size.getX(), (int) size.getY());
     }

     ImageIO.write(img, "PNG", new File(getArtifactsDir() + "Rendering.Thumbnails.png"));
 } finally {
     if (gr != null) {
         gr.dispose();
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |
| graphics | java.awt.Graphics2D | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered page. |
| scale | float | The scale for rendering the page (1.0 is 100%). |

**Returns:**
java.awt.geom.Point2D.Float - The width and height (in world units) of the rendered page.
### renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-int-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)
```


Renders a document page into a java.awt.Graphics2D object to a specified size.

 **Examples:** 

Shows how to render a document to a bitmap at a specified location and size.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 BufferedImage img = new BufferedImage(700, 700, BufferedImage.TYPE_INT_ARGB);
 // User has some sort of a Graphics object
 // In this case created from a bitmap
 Graphics2D gr = img.createGraphics();
 try {
     // The user can specify any options on the Graphics object including
     // transform, antialiasing, page units, etc
     gr.setRenderingHint(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON);

     // Offset the output 0.5" from the edge.
     gr.translate(ConvertUtil.inchToPoint(0.5f), ConvertUtil.inchToPoint(0.5f));

     // Rotate the output by 10 degrees.
     gr.rotate(10.0 * Math.PI / 180.0, img.getWidth() / 2.0, img.getHeight() / 2.0);

     gr.setColor(Color.RED);

     // Draw a 3"x3" rectangle.
     gr.drawRect(0, 0, (int) ConvertUtil.inchToPoint(3), (int) ConvertUtil.inchToPoint(3));

     // Draw the first page of our document with the same dimensions and transformation as the rectangle.
     // The rectangle will frame the first page.
     float returnedScale = doc.renderToSize(0, gr, 0f, 0f, (float) ConvertUtil.inchToPoint(3), (float) ConvertUtil.inchToPoint(3));

     ImageIO.write(img, "PNG", new File(getArtifactsDir() + "Rendering.RenderToSize.png"));
 } finally {
     if (gr != null) {
         gr.dispose();
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |
| graphics | java.awt.Graphics2D | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered page. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered page. |
| width | float | The maximum width (in world units) that can be occupied by the rendered page. |
| height | float | The maximum height (in world units) that can be occupied by the rendered page. |

**Returns:**
float - The scale that was automatically calculated for the rendered page to fit the specified size.
### save(OutputStream stream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public SaveOutputParameters save(OutputStream stream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters/)
### save(OutputStream stream, int saveFormat) {#save-java.io.OutputStream-int}
```
public SaveOutputParameters save(OutputStream stream, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters/)
### save(String fileName) {#save-java.lang.String}
```
public SaveOutputParameters save(String fileName)
```


Saves the document.  Saves the document to a file. Automatically determines the save format from the extension.

 **Examples:** 

Shows how to open a document and convert it to .PDF.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 doc.save(getArtifactsDir() + "Document.ConvertToPdf.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters/) - Additional information that you can optionally use.
### save(String fileName, SaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SaveOptions}
```
public SaveOutputParameters save(String fileName, SaveOptions saveOptions)
```


Saves the document to a file using the specified save options.

 **Examples:** 

Shows how to improve the quality of a rendered document with SaveOptions.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setSize(60.0);
 builder.writeln("Some text.");

 SaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.Default.jpg", options);

 options.setUseAntiAliasing(true);
 options.setUseHighQualityRendering(true);

 doc.save(getArtifactsDir() + "Document.ImageSaveOptions.HighQuality.jpg", options);
 
```

Shows how to render one page from a document to a JPEG image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set the "PageSet" to "1" to select the second page via
 // the zero-based index to start rendering the document from.
 options.setPageSet(new PageSet(1));

 // When we save the document to the JPEG format, Aspose.Words only renders one page.
 // This image will contain one page starting from page two,
 // which will just be the second page of the original document.
 doc.save(getArtifactsDir() + "ImageSaveOptions.OnePage.jpg", options);
 
```

Shows how to render every page of a document to a separate TIFF image.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);

 for (int i = 0; i < doc.getPageCount(); i++) {
     // Set the "PageSet" property to the number of the first page from
     // which to start rendering the document from.
     options.setPageSet(new PageSet(i));
     // Export page at 2325x5325 pixels and 600 dpi.
     options.setResolution(600f);
     options.setImageSize(new Dimension(2325, 5325));

     doc.save(getArtifactsDir() + MessageFormat.format("ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
 }
 
```

Shows how to configure compression while saving a document as a JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertImage(getImageDir() + "Logo.jpg");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.JPEG);

 // Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
 // This will reduce the file size of the document, but the image will display more prominent compression artifacts.
 imageOptions.setJpegQuality(10);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighCompression.jpg").length() <= 20000);

 // Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
 // This will improve the quality of the image at the cost of an increased file size.
 imageOptions.setJpegQuality(100);

 doc.save(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);

 Assert.assertTrue(new File(getArtifactsDir() + "ImageSaveOptions.JpegQuality.HighQuality.jpg").length() < 60000);
 
```

Shows how to convert a whole document to PDF with three levels in the document outline.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert headings of levels 1 to 5.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);

 Assert.assertTrue(builder.getParagraphFormat().isHeading());

 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);

 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);

 builder.writeln("Heading 1.2.1");
 builder.writeln("Heading 1.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);

 builder.writeln("Heading 1.2.2.1");
 builder.writeln("Heading 1.2.2.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_5);

 builder.writeln("Heading 1.2.2.2.1");
 builder.writeln("Heading 1.2.2.2.2");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // The output PDF document will contain an outline, which is a table of contents that lists headings in the document body.
 // Clicking on an entry in this outline will take us to the location of its respective heading.
 // Set the "HeadingsOutlineLevels" property to "4" to exclude all headings whose levels are above 4 from the outline.
 options.getOutlineOptions().setHeadingsOutlineLevels(4);

 // If an outline entry has subsequent entries of a higher level inbetween itself and the next entry of the same or lower level,
 // an arrow will appear to the left of the entry. This entry is the "owner" of several such "sub-entries".
 // In our document, the outline entries from the 5th heading level are sub-entries of the second 4th level outline entry,
 // the 4th and 5th heading level entries are sub-entries of the second 3rd level entry, and so on.
 // In the outline, we can click on the arrow of the "owner" entry to collapse/expand all its sub-entries.
 // Set the "ExpandedOutlineLevels" property to "2" to automatically expand all heading level 2 and lower outline entries
 // and collapse all level and 3 and higher entries when we open the document.
 options.getOutlineOptions().setExpandedOutlineLevels(2);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the document is saved. Can be  null . |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters/) - Additional information that you can optionally use.
### save(String fileName, int saveFormat) {#save-java.lang.String-int}
```
public SaveOutputParameters save(String fileName, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters/)
### selectNodes(String xpath) {#selectNodes-java.lang.String}
```
public NodeList selectNodes(String xpath)
```


Selects a list of nodes matching the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to use an XPath expression to test whether a node is inside a field.

```

 Document doc = new Document(getMyDir() + "Mail merge destination - Northwind employees.docx");

 // The NodeList that results from this XPath expression will contain all nodes we find inside a field.
 // However, FieldStart and FieldEnd nodes can be on the list if there are nested fields in the path.
 // Currently does not find rare fields in which the FieldCode or FieldResult spans across multiple paragraphs.
 NodeList resultList =
         doc.selectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");
 Run[] runs = Arrays.stream(resultList.toArray()).filter(n -> n.getNodeType() == NodeType.RUN).toArray(Run[]::new);
 Run run = runs[0];

 // Check if the specified run is one of the nodes that are inside the field.
 System.out.println(MessageFormat.format("Contents of the first Run node that''s part of a field: {0}", run.getText().trim()));
 
```

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[NodeList](../../com.aspose.words/nodelist/) - A list of nodes matching the XPath query.
### selectSingleNode(String xpath) {#selectSingleNode-java.lang.String}
```
public Node selectSingleNode(String xpath)
```


Selects the first [Node](../../com.aspose.words/node/) that matches the XPath expression.

 **Remarks:** 

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

 **Examples:** 

Shows how to select certain nodes by using an XPath expression.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 // This expression will extract all paragraph nodes,
 // which are descendants of any table node in the document.
 NodeList nodeList = doc.selectNodes("//Table//Paragraph");

 // Iterate through the list with an enumerator and print the contents of every paragraph in each cell of the table.
 int index = 0;

 Iterator e = nodeList.iterator();
 while (e.hasNext()) {
     Node currentNode = e.next();
     System.out.println(MessageFormat.format("Table paragraph index {0}, contents: \"{1}\"", index++, currentNode.getText().trim()));
 }

 // This expression will select any paragraphs that are direct children of any Body node in the document.
 nodeList = doc.selectNodes("//Body/Paragraph");

 // We can treat the list as an array.
 Assert.assertEquals(nodeList.toArray().length, 4);

 // Use SelectSingleNode to select the first result of the same expression as above.
 Node node = doc.selectSingleNode("//Body/Paragraph");

 Assert.assertEquals(Paragraph.class, node.getClass());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xpath | java.lang.String | The XPath expression. |

**Returns:**
[Node](../../com.aspose.words/node/) - The first [Node](../../com.aspose.words/node/) that matches the XPath query or  null  if no matching node is found.
### setAttachedTemplate(String value) {#setAttachedTemplate-java.lang.String}
```
public void setAttachedTemplate(String value)
```


Sets the full path of the template attached to the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The full path of the template attached to the document. |

### setAutomaticallyUpdateStyles(boolean value) {#setAutomaticallyUpdateStyles-boolean}
```
public void setAutomaticallyUpdateStyles(boolean value)
```


Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

 **Examples:** 

Shows how to attach a template to a document.

```

 Document doc = new Document();

 // Microsoft Word documents by default come with an attached template called "Normal.dotm".
 // There is no default template for blank Aspose.Words documents.
 Assert.assertEquals("", doc.getAttachedTemplate());

 // Attach a template, then set the flag to apply style changes
 // within the template to styles in our document.
 doc.setAttachedTemplate(getMyDir() + "Business brochure.dotx");
 doc.setAutomaticallyUpdateStyles(true);

 doc.save(getArtifactsDir() + "Document.AutomaticallyUpdateStyles.docx");
 
```

Shows how to set a default template for documents that do not have attached templates.

```

 Document doc = new Document();

 // Enable automatic style updating, but do not attach a template document.
 doc.setAutomaticallyUpdateStyles(true);

 Assert.assertEquals("", doc.getAttachedTemplate());

 // Since there is no template document, the document had nowhere to track style changes.
 // Use a SaveOptions object to automatically set a template
 // if a document that we are saving does not have one.
 SaveOptions options = SaveOptions.createSaveOptions("Document.DefaultTemplate.docx");
 options.setDefaultTemplate(getMyDir() + "Business brochure.dotx");

 doc.save(getArtifactsDir() + "Document.DefaultTemplate.docx", options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |

### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape}
```
public void setBackgroundShape(Shape value)
```


Sets the background shape of the document. Can be  null .

 **Remarks:** 

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype/\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions/\#getDisplayBackgroundShape) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions/\#setDisplayBackgroundShape-boolean) to  true .

 **Examples:** 

Shows how to set a background shape for every page of a document.

```

 Document doc = new Document();

 Assert.assertNull(doc.getBackgroundShape());

 // The only shape type that we can use as a background is a rectangle.
 Shape shapeRectangle = new Shape(doc, ShapeType.RECTANGLE);

 // There are two ways of using this shape as a page background.
 // 1 -  A flat color:
 shapeRectangle.setFillColor(Color.BLUE);
 doc.setBackgroundShape(shapeRectangle);

 doc.save(getArtifactsDir() + "DocumentBase.BackgroundShape.FlatColor.docx");

 // 2 -  An image:
 shapeRectangle = new Shape(doc, ShapeType.RECTANGLE);
 shapeRectangle.getImageData().setImage(getImageDir() + "Transparent background logo.png");

 // Adjust the image's appearance to make it more suitable as a watermark.
 shapeRectangle.getImageData().setContrast(0.2);
 shapeRectangle.getImageData().setBrightness(0.7);

 doc.setBackgroundShape(shapeRectangle);

 Assert.assertTrue(doc.getBackgroundShape().hasImage());

 PdfSaveOptions saveOptions = new PdfSaveOptions();
 saveOptions.setCacheBackgroundGraphics(false);

 // Microsoft Word does not support shapes with images as backgrounds,
 // but we can still see these backgrounds in other save formats such as .pdf.
 doc.save(getArtifactsDir() + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | The background shape of the document. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

 **Remarks:** 

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

 **Examples:** 

Shows how to traverse through a composite node's collection of child nodes.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setCustomXmlParts(CustomXmlPartCollection value) {#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection}
```
public void setCustomXmlParts(CustomXmlPartCollection value)
```


Sets the collection of Custom XML Data Storage Parts.

 **Remarks:** 

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

 **Examples:** 

Shows how to create a structured document tag with custom XML data.

```

 Document doc = new Document();

 // Construct an XML part that contains data and add it to the document's collection.
 // If we enable the "Developer" tab in Microsoft Word,
 // we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 Assert.assertEquals(xmlPart.getData(), xmlPartContent.getBytes());
 Assert.assertEquals(xmlPart.getId(), xmlPartId);

 // Below are two ways to refer to XML parts.
 // 1 -  By an index in the custom XML part collection:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().get(0));

 // 2 -  By GUID:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().getById(xmlPartId));

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone a part, and then insert it into the collection.
 CustomXmlPart xmlPartClone = xmlPart.deepClone();
 xmlPartClone.setId(UUID.randomUUID().toString());
 doc.getCustomXmlParts().add(xmlPartClone);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 2);

 // Iterate through the collection and print the contents of each part.
 Iterator enumerator = doc.getCustomXmlParts().iterator();
 int index = 0;
 while (enumerator.hasNext()) {
     CustomXmlPart customXmlPart = enumerator.next();
     System.out.println(MessageFormat.format("XML part index {0}, ID: {1}", index, customXmlPart.getId()));
     System.out.println(MessageFormat.format("\tContent: {0}", customXmlPart.getData()));
     index++;
 }

 // Use the "RemoveAt" method to remove the cloned part by index.
 doc.getCustomXmlParts().removeAt(1);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 1);

 // Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
 CustomXmlPartCollection customXmlParts = doc.getCustomXmlParts().deepClone();
 customXmlParts.clear();

 // Create a structured document tag that will display our part's contents and insert it into the document body.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[1]", "");

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CustomXml.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection/) | The collection of Custom XML Data Storage Parts. |

### setDefaultTabStop(double value) {#setDefaultTabStop-double}
```
public void setDefaultTabStop(double value)
```


Sets the interval (in points) between the default tab stops.

 **Examples:** 

Shows how to set a custom interval for tab stop positions.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Set tab stops to appear every 72 points (1 inch).
 builder.getDocument().setDefaultTabStop(72.0);

 // Each tab character snaps the text after it to the next closest tab stop position.
 builder.writeln("Hello" + ControlChar.TAB + "World!");
 builder.writeln("Hello" + ControlChar.TAB_CHAR + "World!");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The interval (in points) between the default tab stops. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Sets document font settings.

 **Remarks:** 

This property allows to specify font settings per document. If set to  null , default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) will be used.

The default value is  null .

 **Examples:** 

Shows how set font substitution rules.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getFont().setName("Arial");
 builder.writeln("Hello world!");
 builder.getFont().setName("Amethysta");
 builder.writeln("The quick brown fox jumps over the lazy dog.");

 FontSourceBase[] fontSources = FontSettings.getDefaultInstance().getFontsSources();

 // The default font sources contain the first font that the document uses.
 Assert.assertEquals(1, fontSources.length);
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arial")));

 // The second font, "Amethysta", is unavailable.
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Amethysta")));

 // We can configure a font substitution table which determines
 // which fonts Aspose.Words will use as substitutes for unavailable fonts.
 // Set two substitution fonts for "Amethysta": "Arvo", and "Courier New".
 // If the first substitute is unavailable, Aspose.Words attempts to use the second substitute, and so on.
 doc.setFontSettings(new FontSettings());
 doc.getFontSettings().getSubstitutionSettings().getTableSubstitution().setSubstitutes(
         "Amethysta", "Arvo", "Courier New");

 // "Amethysta" is unavailable, and the substitution rule states that the first font to use as a substitute is "Arvo".
 Assert.assertFalse(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Arvo")));

 // "Arvo" is also unavailable, but "Courier New" is.
 Assert.assertTrue(IterableUtils.matchesAny(fontSources[0].getAvailableFonts(), f -> f.getFullFontName().contains("Courier New")));

 // The output document will display the text that uses the "Amethysta" font formatted with "Courier New".
 doc.save(getArtifactsDir() + "FontSettings.TableSubstitution.pdf");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Document font settings. |

### setGlossaryDocument(GlossaryDocument value) {#setGlossaryDocument-com.aspose.words.GlossaryDocument}
```
public void setGlossaryDocument(GlossaryDocument value)
```


Sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

 **Remarks:** 

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument/) object and assigning to this property.

 **Examples:** 

Shows how to add a custom building block to a document.

```

 public void createAndInsert() throws Exception {
     // A document's glossary document stores building blocks.
     Document doc = new Document();
     GlossaryDocument glossaryDoc = new GlossaryDocument();
     doc.setGlossaryDocument(glossaryDoc);

     // Create a building block, name it, and then add it to the glossary document.
     BuildingBlock block = new BuildingBlock(glossaryDoc);
     block.setName("Custom Block");

     glossaryDoc.appendChild(block);

     // All new building block GUIDs have the same zero value by default, and we can give them a new unique value.
     Assert.assertEquals(block.getGuid().toString(), "00000000-0000-0000-0000-000000000000");

     block.setGuid(UUID.randomUUID());

     // The following properties categorize building blocks
     // in the menu we can access in Microsoft Word via "Insert" -> "Quick Parts" -> "Building Blocks Organizer".
     Assert.assertEquals(block.getCategory(), "(Empty Category)");
     Assert.assertEquals(block.getType(), BuildingBlockType.NONE);
     Assert.assertEquals(block.getGallery(), BuildingBlockGallery.ALL);
     Assert.assertEquals(block.getBehavior(), BuildingBlockBehavior.CONTENT);

     // Before we can add this building block to our document, we will need to give it some contents,
     // which we will do using a document visitor. This visitor will also set a category, gallery, and behavior.
     BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
     // Visit start/end of the BuildingBlock.
     block.accept(visitor);
     // Visit only start of the BuildingBlock.
     block.acceptStart(visitor);
     // Visit only end of the BuildingBlock.
     block.acceptEnd(visitor);

     // We can access the block that we just made from the glossary document.
     BuildingBlock customBlock = glossaryDoc.getBuildingBlock(BuildingBlockGallery.QUICK_PARTS,
             "My custom building blocks", "Custom Block");

     // The block itself is a section that contains the text.
     Assert.assertEquals(MessageFormat.format("Text inside {0}\f", customBlock.getName()), customBlock.getFirstSection().getBody().getFirstParagraph().getText());
     Assert.assertEquals(customBlock.getFirstSection(), customBlock.getLastSection());
     // Now, we can insert it into the document as a new section.
     doc.appendChild(doc.importNode(customBlock.getFirstSection(), true));

     // We can also find it in Microsoft Word's Building Blocks Organizer and place it manually.
     doc.save(getArtifactsDir() + "BuildingBlocks.CreateAndInsert.dotx");
 }

 /// 
 /// Sets up a visited building block to be inserted into the document as a quick part and adds text to its contents.
 /// 
 public static class BuildingBlockVisitor extends DocumentVisitor {
     public BuildingBlockVisitor(final GlossaryDocument ownerGlossaryDoc) {
         mBuilder = new StringBuilder();
         mGlossaryDoc = ownerGlossaryDoc;
     }

     public int visitBuildingBlockStart(final BuildingBlock block) {
         // Configure the building block as a quick part, and add properties used by Building Blocks Organizer.
         block.setBehavior(BuildingBlockBehavior.PARAGRAPH);
         block.setCategory("My custom building blocks");
         block.setDescription("Using this block in the Quick Parts section of word will place its contents at the cursor.");
         block.setGallery(BuildingBlockGallery.QUICK_PARTS);

         // Add a section with text.
         // Inserting the block into the document will append this section with its child nodes at the location.
         Section section = new Section(mGlossaryDoc);
         block.appendChild(section);
         block.getFirstSection().ensureMinimum();

         Run run = new Run(mGlossaryDoc, "Text inside " + block.getName());
         block.getFirstSection().getBody().getFirstParagraph().appendChild(run);

         return VisitorAction.CONTINUE;
     }

     public int visitBuildingBlockEnd(final BuildingBlock block) {
         mBuilder.append("Visited " + block.getName() + "\r\n");
         return VisitorAction.CONTINUE;
     }

     private final StringBuilder mBuilder;
     private final GlossaryDocument mGlossaryDoc;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [GlossaryDocument](../../com.aspose.words/glossarydocument/) | The glossary document within this document or template. |

### setGrammarChecked(boolean value) {#setGrammarChecked-boolean}
```
public void setGrammarChecked(boolean value)
```


Returns  true  if the document has been checked for grammar.

 **Remarks:** 

To recheck the grammar in the document, set this property to  false .

 **Examples:** 

Shows how to set spelling or grammar verifying.

```

 Document doc = new Document();

 // The string with spelling errors.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().add(new Run(doc, "The speeling in this documentz is all broked."));

 // Spelling/Grammar check start if we set properties to false.
 // We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
 // Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
 doc.setSpellingChecked(checkSpellingGrammar);
 doc.setGrammarChecked(checkSpellingGrammar);

 doc.save(getArtifactsDir() + "Document.SpellingOrGrammar.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  true  if the document has been checked for grammar. |

### setIncludeTextboxesFootnotesEndnotesInStat(boolean value) {#setIncludeTextboxesFootnotesEndnotesInStat-boolean}
```
public void setIncludeTextboxesFootnotesEndnotesInStat(boolean value)
```


Specifies whether to include textboxes, footnotes and endnotes in word count statistics.

 **Examples:** 

Shows how to include or exclude textboxes, footnotes and endnotes from word count statistics.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Lorem ipsum");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "sit amet");

 // By default option is set to 'false'.
 doc.updateWordCount();
 // Words count without textboxes, footnotes and endnotes.
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getWords());

 doc.setIncludeTextboxesFootnotesEndnotesInStat(true);
 doc.updateWordCount();
 // Words count with textboxes, footnotes and endnotes.
 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getWords());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setJustificationMode(int value) {#setJustificationMode-int}
```
public void setJustificationMode(int value)
```


Sets the character spacing adjustment of a document.

 **Examples:** 

Shows how to manage character spacing control.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The character spacing adjustment of a document. The value must be one of [JustificationMode](../../com.aspose.words/justificationmode/) constants. |

### setMailMergeSettings(MailMergeSettings value) {#setMailMergeSettings-com.aspose.words.MailMergeSettings}
```
public void setMailMergeSettings(MailMergeSettings value)
```


Sets the object that contains all of the mail merge information for a document.

 **Remarks:** 

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

This object is never  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MailMergeSettings](../../com.aspose.words/mailmergesettings/) | The object that contains all of the mail merge information for a document. |

### setNodeChangingCallback(INodeChangingCallback value) {#setNodeChangingCallback-com.aspose.words.INodeChangingCallback}
```
public void setNodeChangingCallback(INodeChangingCallback value)
```


Called when a node is inserted or removed in the document.

 **Examples:** 

Shows how customize node changing with a callback.

```

 public void fontChangeViaCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Set the node changing callback to custom implementation,
     // then add/remove nodes to get it to generate a log.
     HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
     doc.setNodeChangingCallback(callback);

     builder.writeln("Hello world!");
     builder.writeln("Hello again!");
     builder.insertField(" HYPERLINK \"https://www.google.com/\" ");
     builder.insertShape(ShapeType.RECTANGLE, 300.0, 300.0);

     doc.getRange().getFields().get(0).remove();

     System.out.println(callback.getLog());
 }

 /// 
 /// Logs the date and time of each node insertion and removal.
 /// Sets a custom font name/size for the text contents of Run nodes.
 /// 
 public static class HandleNodeChangingFontChanger implements INodeChangingCallback {
     public void nodeInserted(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash:\t{0}", args.getNode().hashCode()));

         if (args.getNode().getNodeType() == NodeType.RUN) {
             Font font = ((Run) args.getNode()).getFont();
             mLog.append(MessageFormat.format("\tFont:\tChanged from \"{0}\" {1}pt", font.getName(), font.getSize()));

             font.setSize(24.0);
             font.setName("Arial");

             mLog.append(MessageFormat.format(" to \"{0}\" {1}pt", font.getName(), font.getSize()));
             mLog.append(MessageFormat.format("\tContents:\n\t\t\"{0}\"", args.getNode().getText()));
         }
     }

     public void nodeInserting(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode insertion:", new Date()));
     }

     public void nodeRemoved(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash code:\t{0}", args.getNode().hashCode()));
     }

     public void nodeRemoving(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode removal:", new Date()));
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) | The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) value. |

### setPackageCustomParts(CustomPartCollection value) {#setPackageCustomParts-com.aspose.words.CustomPartCollection}
```
public void setPackageCustomParts(CustomPartCollection value)
```


Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

 **Remarks:** 

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document/\#getCustomXmlParts) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document/\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

 **Examples:** 

Shows how to access a document's arbitrary custom parts collection.

```

 Document doc = new Document(getMyDir() + "Custom parts OOXML package.docx");

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 // Clone the second part, then add the clone to the collection.
 CustomPart clonedPart = doc.getPackageCustomParts().get(1).deepClone();
 doc.getPackageCustomParts().add(clonedPart);
 Assert.assertEquals(3, doc.getPackageCustomParts().getCount());

 // Enumerate over the collection and print every part.
 Iterator enumerator = doc.getPackageCustomParts().iterator();

 int index = 0;
 while (enumerator.hasNext()) {
     CustomPart customPart = enumerator.next();
     System.out.println(MessageFormat.format("Part index {0}:", index));
     System.out.println(MessageFormat.format("\tName: {0}", customPart.getName()));
     System.out.println(MessageFormat.format("\tContentType: {0}", customPart.getContentType()));
     System.out.println(MessageFormat.format("\tRelationshipType: {0}", customPart.getRelationshipType()));
     if (customPart.isExternal()) {
         System.out.println("\tSourced from outside the document");
     } else {
         System.out.println(MessageFormat.format("\tSourced from within the document, length: {0} bytes", customPart.getData().length));
     }
     index++;
 }

 // We can remove elements from this collection individually, or all at once.
 doc.getPackageCustomParts().removeAt(2);

 Assert.assertEquals(2, doc.getPackageCustomParts().getCount());

 doc.getPackageCustomParts().clear();

 Assert.assertEquals(0, doc.getPackageCustomParts().getCount());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CustomPartCollection](../../com.aspose.words/custompartcollection/) | The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |

### setPageColor(Color value) {#setPageColor-java.awt.Color}
```
public void setPageColor(Color value)
```


Sets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

 **Remarks:** 

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

 **Examples:** 

Shows how to set the background color for all pages of a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 doc.setPageColor(Color.lightGray);

 doc.save(getArtifactsDir() + "DocumentBase.SetPageColor.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The page color of the document. |

### setPunctuationKerning(boolean value) {#setPunctuationKerning-boolean}
```
public void setPunctuationKerning(boolean value)
```


Specifies whether kerning applies to both Latin text and punctuation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setRemovePersonalInformation(boolean value) {#setRemovePersonalInformation-boolean}
```
public void setRemovePersonalInformation(boolean value)
```


Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

 **Examples:** 

Shows how to enable the removal of personal information during a manual save.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some content with personal information.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 doc.getBuiltInDocumentProperties().setCompany("Placeholder Inc.");

 doc.startTrackRevisions(doc.getBuiltInDocumentProperties().getAuthor(), new Date());
 builder.write("Hello world!");
 doc.stopTrackRevisions();

 // This flag is equivalent to File -> Options -> Trust Center -> Trust Center Settings... ->
 // Privacy Options -> "Remove personal information from file properties on save" in Microsoft Word.
 doc.setRemovePersonalInformation(saveWithoutPersonalInfo);

 // This option will not take effect during a save operation made using Aspose.Words.
 // Personal data will be removed from our document with the flag set when we save it manually using Microsoft Word.
 doc.save(getArtifactsDir() + "Document.RemovePersonalInformation.docx");
 doc = new Document(getArtifactsDir() + "Document.RemovePersonalInformation.docx");

 Assert.assertEquals(saveWithoutPersonalInfo, doc.getRemovePersonalInformation());
 Assert.assertEquals("John Doe", doc.getBuiltInDocumentProperties().getAuthor());
 Assert.assertEquals("Placeholder Inc.", doc.getBuiltInDocumentProperties().getCompany());
 Assert.assertEquals("John Doe", doc.getRevisions().get(0).getAuthor());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources are loaded.

 **Examples:** 

Shows how to customize the process of loading external resources into a document.

```

 public void resourceLoadingCallback() throws Exception {
     Document doc = new Document();
     doc.setResourceLoadingCallback(new ImageNameHandler());

     DocumentBuilder builder = new DocumentBuilder(doc);

     // Images usually are inserted using a URI, or a byte array.
     // Every instance of a resource load will call our callback's ResourceLoading method.
     builder.insertImage("Google logo");
     builder.insertImage("Aspose logo");
     builder.insertImage("Watermark");

     Assert.assertEquals(3, doc.getChildNodes(NodeType.SHAPE, true).getCount());

     doc.save(getArtifactsDir() + "DocumentBase.ResourceLoadingCallback.docx");
 }

 /// 
 /// Allows us to load images into a document using predefined shorthands, as opposed to URIs.
 /// This will separate image loading logic from the rest of the document construction.
 /// 
 private static class ImageNameHandler implements IResourceLoadingCallback {
     public int resourceLoading(final ResourceLoadingArgs args) throws URISyntaxException, IOException {
         if (args.getResourceType() == ResourceType.IMAGE) {
             // If this callback encounters one of the image shorthands while loading an image,
             // it will apply unique logic for each defined shorthand instead of treating it as a URI.
             if ("Google logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(new URI("http://www.google.com/images/logos/ps_logo2.png").toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Aspose logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getAsposelogoUri().toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Watermark".equals(args.getOriginalUri())) {
                 InputStream imageStream = new FileInputStream(getImageDir() + "Transparent background logo.png");
                 args.setData(DocumentHelper.getBytesFromStream(imageStream));

                 return ResourceLoadingAction.USER_PROVIDED;
             }
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value. |

### setRevisionsView(int value) {#setRevisionsView-int}
```
public void setRevisionsView(int value)
```


Sets a value indicating whether to work with the original or revised version of a document.

 **Remarks:** 

The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview/\#ORIGINAL)** .

 **Examples:** 

Shows how to switch between the revised and the original view of a document.

```

 Document doc = new Document(getMyDir() + "Revisions at list levels.docx");
 doc.updateListLabels();

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("1.", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("", paragraphs.get(2).getListLabel().getLabelString());

 // View the document object as if all the revisions are accepted. Currently supports list labels.
 doc.setRevisionsView(RevisionsView.FINAL);

 Assert.assertEquals("", paragraphs.get(0).getListLabel().getLabelString());
 Assert.assertEquals("1.", paragraphs.get(1).getListLabel().getLabelString());
 Assert.assertEquals("a.", paragraphs.get(2).getListLabel().getLabelString());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value indicating whether to work with the original or revised version of a document. The value must be one of [RevisionsView](../../com.aspose.words/revisionsview/) constants. |

### setSectionAttr(int key, Object value) {#setSectionAttr-int-java.lang.Object}
```
public void setSectionAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setShadeFormData(boolean value) {#setShadeFormData-boolean}
```
public void setShadeFormData(boolean value)
```


Specifies whether to turn on the gray shading on form fields.

 **Examples:** 

Shows how to apply gray shading to form fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.write("Hello world! ");
 builder.insertTextInput("My form field", TextFormFieldType.REGULAR, "",
         "Text contents of form field, which are shaded in grey by default.", 0);

 // We can turn the grey shading off, so the bookmarked text will blend in with the other text.
 doc.setShadeFormData(useGreyShading);
 doc.save(getArtifactsDir() + "Document.ShadeFormData.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowGrammaticalErrors(boolean value) {#setShowGrammaticalErrors-boolean}
```
public void setShowGrammaticalErrors(boolean value)
```


Specifies whether to display grammar errors in this document.

 **Examples:** 

Shows how to show/hide errors in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two sentences with mistakes that would be picked up
 // by the spelling and grammar checkers in Microsoft Word.
 builder.writeln("There is a speling error in this sentence.");
 builder.writeln("Their is a grammatical error in this sentence.");

 // If these options are enabled, then spelling errors will be underlined
 // in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
 doc.setShowGrammaticalErrors(showErrors);
 doc.setShowSpellingErrors(showErrors);

 doc.save(getArtifactsDir() + "Document.SpellingAndGrammarErrors.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowSpellingErrors(boolean value) {#setShowSpellingErrors-boolean}
```
public void setShowSpellingErrors(boolean value)
```


Specifies whether to display spelling errors in this document.

 **Examples:** 

Shows how to show/hide errors in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two sentences with mistakes that would be picked up
 // by the spelling and grammar checkers in Microsoft Word.
 builder.writeln("There is a speling error in this sentence.");
 builder.writeln("Their is a grammatical error in this sentence.");

 // If these options are enabled, then spelling errors will be underlined
 // in the output document by a jagged red line, and a double blue line will highlight grammatical mistakes.
 doc.setShowGrammaticalErrors(showErrors);
 doc.setShowSpellingErrors(showErrors);

 doc.save(getArtifactsDir() + "Document.SpellingAndGrammarErrors.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpellingChecked(boolean value) {#setSpellingChecked-boolean}
```
public void setSpellingChecked(boolean value)
```


Returns  true  if the document has been checked for spelling.

 **Remarks:** 

To recheck the spelling in the document, set this property to  false .

 **Examples:** 

Shows how to set spelling or grammar verifying.

```

 Document doc = new Document();

 // The string with spelling errors.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().add(new Run(doc, "The speeling in this documentz is all broked."));

 // Spelling/Grammar check start if we set properties to false.
 // We can see all errors in Microsoft Word via Review -> Spelling & Grammar.
 // Note that Microsoft Word does not start grammar/spell check automatically for DOC and RTF document format.
 doc.setSpellingChecked(checkSpellingGrammar);
 doc.setGrammarChecked(checkSpellingGrammar);

 doc.save(getArtifactsDir() + "Document.SpellingOrGrammar.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  true  if the document has been checked for spelling. |

### setTrackRevisions(boolean value) {#setTrackRevisions-boolean}
```
public void setTrackRevisions(boolean value)
```


True if changes are tracked when this document is edited in Microsoft Word.

 **Remarks:** 

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document/\#startTrackRevisions-java.lang.String--java.util.Date) method.

 **Examples:** 

Shows how to work with revisions in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Normal editing of the document does not count as a revision.
 builder.write("This does not count as a revision. ");

 Assert.assertFalse(doc.hasRevisions());

 // To register our edits as revisions, we need to declare an author, and then start tracking them.
 doc.startTrackRevisions("John Doe", new Date());

 builder.write("This is revision #1. ");

 Assert.assertTrue(doc.hasRevisions());
 Assert.assertEquals(1, doc.getRevisions().getCount());

 // This flag corresponds to the "Review" -> "Tracking" -> "Track Changes" option in Microsoft Word.
 // The "StartTrackRevisions" method does not affect its value,
 // and the document is tracking revisions programmatically despite it having a value of "false".
 // If we open this document using Microsoft Word, it will not be tracking revisions.
 Assert.assertFalse(doc.getTrackRevisions());

 // We have added text using the document builder, so the first revision is an insertion-type revision.
 Revision revision = doc.getRevisions().get(0);
 Assert.assertEquals("John Doe", revision.getAuthor());
 Assert.assertEquals("This is revision #1. ", revision.getParentNode().getText());
 Assert.assertEquals(RevisionType.INSERTION, revision.getRevisionType());
 Assert.assertEquals(revision.getDateTime().getDate(), new Date().getDate());
 Assert.assertEquals(doc.getRevisions().getGroups().get(0), revision.getGroup());

 // Remove a run to create a deletion-type revision.
 doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0).remove();

 // Adding a new revision places it at the beginning of the revision collection.
 Assert.assertEquals(RevisionType.DELETION, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(2, doc.getRevisions().getCount());

 // Insert revisions show up in the document body even before we accept/reject the revision.
 // Rejecting the revision will remove its nodes from the body. Conversely, nodes that make up delete revisions
 // also linger in the document until we accept the revision.
 Assert.assertEquals("This does not count as a revision. This is revision #1.", doc.getText().trim());

 // Accepting the delete revision will remove its parent node from the paragraph text
 // and then remove the collection's revision itself.
 doc.getRevisions().get(0).accept();

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1.", doc.getText().trim());

 builder.writeln("");
 builder.write("This is revision #2.");

 // Now move the node to create a moving revision type.
 Node node = doc.getFirstSection().getBody().getParagraphs().get(1);
 Node endNode = doc.getFirstSection().getBody().getParagraphs().get(1).getNextSibling();
 Node referenceNode = doc.getFirstSection().getBody().getParagraphs().get(0);

 while (node != endNode)
 {
     Node nextNode = node.getNextSibling();
     doc.getFirstSection().getBody().insertBefore(node, referenceNode);
     node = nextNode;
 }

 Assert.assertEquals(RevisionType.MOVING, doc.getRevisions().get(0).getRevisionType());
 Assert.assertEquals(8, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.getText().trim());

 // The moving revision is now at index 1. Reject the revision to discard its contents.
 doc.getRevisions().get(1).reject();

 Assert.assertEquals(6, doc.getRevisions().getCount());
 Assert.assertEquals("This is revision #1. \rThis is revision #2.", doc.getText().trim());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setVbaProject(VbaProject value) {#setVbaProject-com.aspose.words.VbaProject}
```
public void setVbaProject(VbaProject value)
```


Sets a [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject).

 **Examples:** 

Shows how to access a document's VBA project information.

```

 Document doc = new Document(getMyDir() + "VBA project.docm");

 // A VBA project contains a collection of VBA modules.
 VbaProject vbaProject = doc.getVbaProject();
 System.out.println(vbaProject.isSigned()
         ? MessageFormat.format("Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount())
         : MessageFormat.format("Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject.getName(), vbaProject.getCodePage(), vbaProject.getModules().getCount()));

 VbaModuleCollection vbaModules = doc.getVbaProject().getModules();

 Assert.assertEquals(vbaModules.getCount(), 3);

 for (VbaModule module : vbaModules) {
     System.out.println(MessageFormat.format("Module name: {0};\nModule code:\n{1}\n", module.getName(), module.getSourceCode()));
 }

 // Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
 vbaModules.get(0).setSourceCode("Your VBA code...");
 vbaModules.get("Module1").setSourceCode("Your VBA code...");

 // Remove a module from the collection.
 vbaModules.remove(vbaModules.get(2));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [VbaProject](../../com.aspose.words/vbaproject/) | A [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss.

 **Remarks:** 

Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document/\#getPageCount) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

 **Examples:** 

Shows how to use the IWarningCallback interface to monitor font substitution warnings.

```

 public void substitutionWarning() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.getFont().setName("Times New Roman");
     builder.writeln("Hello world!");

     FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
     doc.setWarningCallback(callback);

     // Store the current collection of font sources, which will be the default font source for every document
     // for which we do not specify a different font source.
     FontSourceBase[] originalFontSources = FontSettings.getDefaultInstance().getFontsSources();

     // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
     FontSettings.getDefaultInstance().setFontsFolder("", false);

     // When rendering the document, there will be no place to find the "Times New Roman" font.
     // This will cause a font substitution warning, which our callback will detect.
     doc.save(getArtifactsDir() + "FontSettings.SubstitutionWarning.pdf");

     FontSettings.getDefaultInstance().setFontsSources(originalFontSources);

     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getWarningType() == WarningType.FONT_SUBSTITUTION);
     Assert.assertTrue(callback.FontSubstitutionWarnings.get(0).getDescription()
             .equals("Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
 }

 private static class FontSubstitutionWarningCollector implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontSubstitutionWarnings.warning(info);
     }

     public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
 }
 
```

Shows how to set the property for finding the closest match for a missing font from the available font sources.

```

 public void enableFontSubstitution() throws Exception {
     // Open a document that contains text formatted with a font that does not exist in any of our font sources.
     Document doc = new Document(getMyDir() + "Missing font.docx");

     // Assign a callback for handling font substitution warnings.
     HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
     doc.setWarningCallback(substitutionWarningHandler);

     // Set a default font name and enable font substitution.
     FontSettings fontSettings = new FontSettings();
     fontSettings.getSubstitutionSettings().getDefaultFontSubstitution().setDefaultFontName("Arial");
     fontSettings.getSubstitutionSettings().getFontInfoSubstitution().setEnabled(true);

     // Original font metrics should be used after font substitution.
     doc.getLayoutOptions().setKeepOriginalFontMetrics(true);

     // We will get a font substitution warning if we save a document with a missing font.
     doc.setFontSettings(fontSettings);
     doc.save(getArtifactsDir() + "FontSettings.EnableFontSubstitution.pdf");

     Iterator warnings = substitutionWarningHandler.FontWarnings.iterator();

     while (warnings.hasNext())
         System.out.println(warnings.next().getDescription());

     // We can also verify warnings in the collection and clear them.
     Assert.assertEquals(WarningSource.LAYOUT, substitutionWarningHandler.FontWarnings.get(0).getSource());
     Assert.assertEquals("Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
             substitutionWarningHandler.FontWarnings.get(0).getDescription());

     substitutionWarningHandler.FontWarnings.clear();

     Assert.assertTrue(substitutionWarningHandler.FontWarnings.getCount() == 0);
 }

 public static class HandleDocumentSubstitutionWarnings implements IWarningCallback {
     /// 
     /// Called every time a warning occurs during loading/saving.
     /// 
     public void warning(WarningInfo info) {
         if (info.getWarningType() == WarningType.FONT_SUBSTITUTION)
             FontWarnings.warning(info);
     }

     public WarningInfoCollection FontWarnings = new WarningInfoCollection();
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

### startTrackRevisions(String author) {#startTrackRevisions-java.lang.String}
```
public void startTrackRevisions(String author)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

 **Remarks:** 

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder/)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document/\#getTrackRevisions) / [setTrackRevisions(boolean)](../../com.aspose.words/document/\#setTrackRevisions-boolean) option and does not use its value for the purposes of revision tracking.

 **Examples:** 

Shows how to track revisions while editing a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Editing a document usually does not count as a revision until we begin tracking them.
 builder.write("Hello world! ");

 Assert.assertEquals(0, doc.getRevisions().getCount());
 Assert.assertFalse(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).isInsertRevision());

 doc.startTrackRevisions("John Doe");

 builder.write("Hello again! ");

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(1).isInsertRevision());
 Assert.assertEquals("John Doe", doc.getRevisions().get(0).getAuthor());

 // Stop tracking revisions to not count any future edits as revisions.
 doc.stopTrackRevisions();
 builder.write("Hello again! ");

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertFalse(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(2).isInsertRevision());

 // Creating revisions gives them a date and time of the operation.
 // We can disable this by passing DateTime.MinValue when we start tracking revisions.
 doc.startTrackRevisions("John Doe", new Date());
 builder.write("Hello again! ");

 Assert.assertEquals(2, doc.getRevisions().getCount());
 Assert.assertEquals("John Doe", doc.getRevisions().get(1).getAuthor());
 Assert.assertEquals(new Date(), doc.getRevisions().get(1).getDateTime());

 // We can accept/reject these revisions programmatically
 // by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
 // In Microsoft Word, we can process them manually via "Review" -> "Changes".
 doc.save(getArtifactsDir() + "Document.StartTrackRevisions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |

### startTrackRevisions(String author, Date dateTime) {#startTrackRevisions-java.lang.String-java.util.Date}
```
public void startTrackRevisions(String author, Date dateTime)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

 **Remarks:** 

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder/)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document/\#getTrackRevisions) / [setTrackRevisions(boolean)](../../com.aspose.words/document/\#setTrackRevisions-boolean) option and does not use its value for the purposes of revision tracking.

 **Examples:** 

Shows how to track revisions while editing a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Editing a document usually does not count as a revision until we begin tracking them.
 builder.write("Hello world! ");

 Assert.assertEquals(0, doc.getRevisions().getCount());
 Assert.assertFalse(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).isInsertRevision());

 doc.startTrackRevisions("John Doe");

 builder.write("Hello again! ");

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(1).isInsertRevision());
 Assert.assertEquals("John Doe", doc.getRevisions().get(0).getAuthor());

 // Stop tracking revisions to not count any future edits as revisions.
 doc.stopTrackRevisions();
 builder.write("Hello again! ");

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertFalse(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(2).isInsertRevision());

 // Creating revisions gives them a date and time of the operation.
 // We can disable this by passing DateTime.MinValue when we start tracking revisions.
 doc.startTrackRevisions("John Doe", new Date());
 builder.write("Hello again! ");

 Assert.assertEquals(2, doc.getRevisions().getCount());
 Assert.assertEquals("John Doe", doc.getRevisions().get(1).getAuthor());
 Assert.assertEquals(new Date(), doc.getRevisions().get(1).getDateTime());

 // We can accept/reject these revisions programmatically
 // by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
 // In Microsoft Word, we can process them manually via "Review" -> "Changes".
 doc.save(getArtifactsDir() + "Document.StartTrackRevisions.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. |

### stopTrackRevisions() {#stopTrackRevisions}
```
public void stopTrackRevisions()
```


Stops automatic marking of document changes as revisions.

 **Examples:** 

Shows how to track revisions while editing a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Editing a document usually does not count as a revision until we begin tracking them.
 builder.write("Hello world! ");

 Assert.assertEquals(0, doc.getRevisions().getCount());
 Assert.assertFalse(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(0).isInsertRevision());

 doc.startTrackRevisions("John Doe");

 builder.write("Hello again! ");

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertTrue(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(1).isInsertRevision());
 Assert.assertEquals("John Doe", doc.getRevisions().get(0).getAuthor());

 // Stop tracking revisions to not count any future edits as revisions.
 doc.stopTrackRevisions();
 builder.write("Hello again! ");

 Assert.assertEquals(1, doc.getRevisions().getCount());
 Assert.assertFalse(doc.getFirstSection().getBody().getParagraphs().get(0).getRuns().get(2).isInsertRevision());

 // Creating revisions gives them a date and time of the operation.
 // We can disable this by passing DateTime.MinValue when we start tracking revisions.
 doc.startTrackRevisions("John Doe", new Date());
 builder.write("Hello again! ");

 Assert.assertEquals(2, doc.getRevisions().getCount());
 Assert.assertEquals("John Doe", doc.getRevisions().get(1).getAuthor());
 Assert.assertEquals(new Date(), doc.getRevisions().get(1).getDateTime());

 // We can accept/reject these revisions programmatically
 // by calling methods such as Document.AcceptAllRevisions, or each revision's Accept method.
 // In Microsoft Word, we can process them manually via "Review" -> "Changes".
 doc.save(getArtifactsDir() + "Document.StartTrackRevisions.docx");
 
```

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(SaveOptions saveOptions) {#toString-com.aspose.words.SaveOptions}
```
public String toString(SaveOptions saveOptions)
```


Exports the content of the node into a string using the specified save options.

 **Examples:** 

Exports the content of a node to String in HTML format.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 Node node = doc.getLastSection().getBody().getLastParagraph();

 // When we call the ToString method using the html SaveFormat overload,
 // it converts the node's contents to their raw html representation.
 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(SaveFormat.HTML));

 // We can also modify the result of this conversion using a SaveOptions object.
 HtmlSaveOptions saveOptions = new HtmlSaveOptions();
 saveOptions.setExportRelativeFontSize(true);

 Assert.assertEquals(" " +
         "Hello World!" +
         "", node.toString(saveOptions));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Specifies the options that control how the node is saved. |

**Returns:**
java.lang.String - The content of the node in the specified format.
### toString(int saveFormat) {#toString-int}
```
public String toString(int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | int |  |

**Returns:**
java.lang.String
### unlinkFields() {#unlinkFields}
```
public void unlinkFields()
```


Unlinks fields in the whole document.

 **Remarks:** 

Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [Range.unlinkFields()](../../com.aspose.words/range/\#unlinkFields).

 **Examples:** 

Shows how to unlink all fields in the document.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");

 doc.unlinkFields();
 
```

### unprotect() {#unprotect}
```
public void unprotect()
```


Removes protection from the document.  Removes protection from the document regardless of the password.

 **Remarks:** 

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

 **Examples:** 

Shows how to protect and unprotect a document.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "password");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 // If we open this document with Microsoft Word intending to edit it,
 // we will need to apply the password to get through the protection.
 doc.save(getArtifactsDir() + "Document.Protect.docx");

 // Note that the protection only applies to Microsoft Word users opening our document.
 // We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
 Document protectedDoc = new Document(getArtifactsDir() + "Document.Protect.docx");

 Assert.assertEquals(ProtectionType.READ_ONLY, protectedDoc.getProtectionType());

 DocumentBuilder builder = new DocumentBuilder(protectedDoc);
 builder.writeln("Text added to a protected document.");
 // There are two ways of removing protection from a document.
 // 1 - With no password:
 doc.unprotect();

 Assert.assertEquals(ProtectionType.NO_PROTECTION, doc.getProtectionType());

 doc.protect(ProtectionType.READ_ONLY, "NewPassword");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 doc.unprotect("WrongPassword");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 // 2 - With the correct password:
 doc.unprotect("NewPassword");

 Assert.assertEquals(ProtectionType.NO_PROTECTION, doc.getProtectionType());
 
```

### unprotect(String password) {#unprotect-java.lang.String}
```
public boolean unprotect(String password)
```


Removes protection from the document if a correct password is specified.

 **Remarks:** 

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

 **Examples:** 

Shows how to protect and unprotect a document.

```

 Document doc = new Document();
 doc.protect(ProtectionType.READ_ONLY, "password");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 // If we open this document with Microsoft Word intending to edit it,
 // we will need to apply the password to get through the protection.
 doc.save(getArtifactsDir() + "Document.Protect.docx");

 // Note that the protection only applies to Microsoft Word users opening our document.
 // We have not encrypted the document in any way, and we do not need the password to open and edit it programmatically.
 Document protectedDoc = new Document(getArtifactsDir() + "Document.Protect.docx");

 Assert.assertEquals(ProtectionType.READ_ONLY, protectedDoc.getProtectionType());

 DocumentBuilder builder = new DocumentBuilder(protectedDoc);
 builder.writeln("Text added to a protected document.");
 // There are two ways of removing protection from a document.
 // 1 - With no password:
 doc.unprotect();

 Assert.assertEquals(ProtectionType.NO_PROTECTION, doc.getProtectionType());

 doc.protect(ProtectionType.READ_ONLY, "NewPassword");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 doc.unprotect("WrongPassword");

 Assert.assertEquals(ProtectionType.READ_ONLY, doc.getProtectionType());

 // 2 - With the correct password:
 doc.unprotect("NewPassword");

 Assert.assertEquals(ProtectionType.NO_PROTECTION, doc.getProtectionType());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to unprotect the document with. |

**Returns:**
boolean -  true  if a correct password was specified and the document was unprotected.
### updateActualReferenceMarks() {#updateActualReferenceMarks}
```
public void updateActualReferenceMarks()
```


Updates the [Footnote.getActualReferenceMark()](../../com.aspose.words/footnote/\#getActualReferenceMark) property of all footnotes and endnotes in the document.

 **Remarks:** 

Updating fields ( [updateFields()](../../com.aspose.words/document/\#updateFields)) may be necessary to get the correct result.

 **Examples:** 

Shows how to get actual footnote reference mark.

```

 Document doc = new Document(getMyDir() + "Footnotes and endnotes.docx");

 Footnote footnote = (Footnote)doc.getChild(NodeType.FOOTNOTE, 1, true);
 doc.updateFields();
 doc.updateActualReferenceMarks();

 Assert.assertEquals("1", footnote.getActualReferenceMark());
 
```

### updateFields() {#updateFields}
```
public void updateFields()
```


Updates the values of fields in the whole document.

 **Remarks:** 

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

Use the [normalizeFieldTypes()](../../com.aspose.words/document/\#normalizeFieldTypes) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.updateFields()](../../com.aspose.words/range/\#updateFields).

 **Examples:** 

Shows to use the QUOTE field.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a QUOTE field, which will display the value of its Text property.
 FieldQuote field = (FieldQuote) builder.insertField(FieldType.FIELD_QUOTE, true);
 field.setText("\"Quoted text\"");

 Assert.assertEquals(" QUOTE  \"\\\"Quoted text\\\"\"", field.getFieldCode());

 // Insert a QUOTE field and nest a DATE field inside it.
 // DATE fields update their value to the current date every time we open the document using Microsoft Word.
 // Nesting the DATE field inside the QUOTE field like this will freeze its value
 // to the date when we created the document.
 builder.write("\nDocument creation date: ");
 field = (FieldQuote) builder.insertField(FieldType.FIELD_QUOTE, true);
 builder.moveTo(field.getSeparator());
 builder.insertField(FieldType.FIELD_DATE, true);

 Assert.assertEquals(" QUOTE  DATE " + LocalDate.now().format(DateTimeFormatter.ofPattern("M/d/YYYY")) + "", field.getFieldCode());

 // Update all the fields to display their correct results.
 doc.updateFields();

 Assert.assertEquals("\"Quoted text\"", doc.getRange().getFields().get(0).getResult());

 doc.save(getArtifactsDir() + "Field.QUOTE.docx");
 
```

Shows how to set user details, and display them using fields.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a UserInformation object and set it as the data source for fields that display user information.
 UserInformation userInformation = new UserInformation();
 userInformation.setName("John Doe");
 userInformation.setInitials("J. D.");
 userInformation.setAddress("123 Main Street");
 doc.getFieldOptions().setCurrentUser(userInformation);

 // Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
 // the respective properties of the UserInformation object that we have created above.
 Assert.assertEquals(userInformation.getName(), builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals(userInformation.getInitials(), builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals(userInformation.getAddress(), builder.insertField(" USERADDRESS ").getResult());

 // The field options object also has a static default user that fields from all documents can refer to.
 UserInformation.getDefaultUser().setName("Default User");
 UserInformation.getDefaultUser().setInitials("D. U.");
 UserInformation.getDefaultUser().setAddress("One Microsoft Way");
 doc.getFieldOptions().setCurrentUser(UserInformation.getDefaultUser());

 Assert.assertEquals("Default User", builder.insertField(" USERNAME ").getResult());
 Assert.assertEquals("D. U.", builder.insertField(" USERINITIALS ").getResult());
 Assert.assertEquals("One Microsoft Way", builder.insertField(" USERADDRESS ").getResult());

 doc.updateFields();
 doc.save(getArtifactsDir() + "FieldOptions.CurrentUser.docx");
 
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```

### updateListLabels() {#updateListLabels}
```
public void updateListLabels()
```


Updates list labels for all list items in the document.

 **Remarks:** 

This method updates list label properties such as [ListLabel.getLabelValue()](../../com.aspose.words/listlabel/\#getLabelValue) and [ListLabel.getLabelString()](../../com.aspose.words/listlabel/\#getLabelString) for each [Paragraph.getListLabel()](../../com.aspose.words/paragraph/\#getListLabel) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.

 **Examples:** 

Shows how to extract the list labels of all paragraphs that are list items.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");
 doc.updateListLabels();
 int listParaCount = 1;

 for (Paragraph paragraph : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     // Find if we have the paragraph list. In our document, our list uses plain Arabic numbers,
     // which start at three and ends at six.
     if (paragraph.getListFormat().isListItem()) {
         System.out.println(MessageFormat.format("List item paragraph #{0}", listParaCount));

         // This is the text we get when getting when we output this node to text format.
         // This text output will omit list labels. Trim any paragraph formatting characters.
         String paragraphText = paragraph.toString(SaveFormat.TEXT).trim();
         System.out.println("Exported Text: " + paragraphText);

         ListLabel label = paragraph.getListLabel();

         // This gets the position of the paragraph in the current level of the list. If we have a list with multiple levels,
         // this will tell us what position it is on that level.
         System.out.println("\tNumerical Id: {label.LabelValue}");

         // Combine them together to include the list label with the text in the output.
         System.out.println("\tList label combined with text: {label.LabelString} {paragraphText}");
     }

 }
 
```

### updatePageLayout() {#updatePageLayout}
```
public void updatePageLayout()
```


Rebuilds the page layout of the document.

 **Remarks:** 

This method formats a document into pages and updates the page number related fields in the document such as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it. However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not update the page layout automatically. In this case you should call [updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) before rendering again.

 **Examples:** 

Shows when to recalculate the page layout of the document.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Saving a document to PDF, to an image, or printing for the first time will automatically
 // cache the layout of the document within its pages.
 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.1.pdf");

 // Modify the document in some way.
 doc.getStyles().get("Normal").getFont().setSize(6.0);
 doc.getSections().get(0).getPageSetup().setOrientation(Orientation.LANDSCAPE);
 doc.getSections().get(0).getPageSetup().setMargins(Margins.MIRRORED);

 // In the current version of Aspose.Words, modifying the document does not automatically rebuild
 // the cached page layout. If we wish for the cached layout
 // to stay up to date, we will need to update it manually.
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.UpdatePageLayout.2.pdf");
 
```

### updateTableLayout() {#updateTableLayout}
```
public void updateTableLayout()
```


Implements an earlier approach to table column widths re-calculation that has known issues.

 **Remarks:** 

The method is deprecated and it will be removed in a few releases.

### updateThumbnail() {#updateThumbnail}
```
public void updateThumbnail()
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document using default options.

 **Examples:** 

Shows how to update a document's thumbnail.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

### updateThumbnail(ThumbnailGeneratingOptions options) {#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions}
```
public void updateThumbnail(ThumbnailGeneratingOptions options)
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document according to the specified options.

 **Remarks:** 

The [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions/) allows you to specify the source of thumbnail, size and other options. If attempt to generate thumbnail fails, doesn't change one.

 **Examples:** 

Shows how to update a document's thumbnail.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // There are two ways of setting a thumbnail image when saving a document to .epub.
 // 1 -  Use the document's first page:
 doc.updateThumbnail();
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstPage.epub");

 // 2 -  Use the first image found in the document:
 ThumbnailGeneratingOptions options = new ThumbnailGeneratingOptions();
 options.setThumbnailSize(new Dimension(400, 400));
 options.setGenerateFromFirstPage(false);

 doc.updateThumbnail(options);
 doc.save(getArtifactsDir() + "Document.UpdateThumbnail.FirstImage.epub");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions/) | The generating options to use. |

### updateWordCount() {#updateWordCount}
```
public void updateWordCount()
```


Updates word count properties of the document.

 **Remarks:** 

[updateWordCount()](../../com.aspose.words/document/\#updateWordCount) recalculates and updates Characters, Words and Paragraphs properties in the [getBuiltInDocumentProperties()](../../com.aspose.words/document/\#getBuiltInDocumentProperties) collection of the [Document](../../com.aspose.words/document/).

Note that [updateWordCount()](../../com.aspose.words/document/\#updateWordCount) does not update number of lines and pages properties. Use the [updateWordCount()](../../com.aspose.words/document/\#updateWordCount) overload and pass  true  value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included in the word count.

 **Examples:** 

Shows how to update all list labels in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

### updateWordCount(boolean updateLinesCount) {#updateWordCount-boolean}
```
public void updateWordCount(boolean updateLinesCount)
```


Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties/\#getLines) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties/\#setLines-int) property.

 **Remarks:** 

This method will rebuild page layout of the document.

 **Examples:** 

Shows how to update all list labels in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
         "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
 builder.write("Ut enim ad minim veniam, " +
         "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

 // Aspose.Words does not track document metrics like these in real time.
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(0, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getParagraphs());
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 // To get accurate values for three of these properties, we will need to update them manually.
 doc.updateWordCount();

 Assert.assertEquals(196, doc.getBuiltInDocumentProperties().getCharacters());
 Assert.assertEquals(36, doc.getBuiltInDocumentProperties().getWords());
 Assert.assertEquals(2, doc.getBuiltInDocumentProperties().getParagraphs());

 // For the line count, we will need to call a specific overload of the updating method.
 Assert.assertEquals(1, doc.getBuiltInDocumentProperties().getLines());

 doc.updateWordCount(true);

 Assert.assertEquals(4, doc.getBuiltInDocumentProperties().getLines());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| updateLinesCount | boolean |  true  if number of lines in the document shall be calculated. |

