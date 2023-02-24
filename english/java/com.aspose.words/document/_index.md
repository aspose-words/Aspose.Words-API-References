---
title: Document
linktitle: Document
second_title: Aspose.Words for Java API Reference
description: Represents a Word document in Java.
type: docs
weight: 121
url: /java/com.aspose.words/document/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node/), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode/), [com.aspose.words.DocumentBase](../../com.aspose.words/documentbase/)
```
public class Document extends DocumentBase
```

Represents a Word document.

To learn more, visit the [ Working with Document ][Working with Document] documentation article.

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
 *  Content nodes can be added or removed from anywhere in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node), [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node), [CompositeNode.removeChild(com.aspose.words.Node)](../../com.aspose.words/compositenode/\#removeChild-com.aspose.words.Node) and other methods provided by the base class [CompositeNode](../../com.aspose.words/compositenode/).
 *  The formatting attributes of each node can be changed via the properties of that node.

Consider using [DocumentBuilder](../../com.aspose.words/documentbuilder/) that simplifies the task of programmatically creating or populating the document tree.

The [Document](../../com.aspose.words/document/) can contain only [Section](../../com.aspose.words/section/) objects.

In Microsoft Word, a valid document needs to have at least one section.


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
| [add(Shape watermark)](#add-com.aspose.words.Shape) |  |
| [appendChild(Node newChild)](#appendChild-com.aspose.words.Node) | Adds the specified node to the end of the list of child nodes for this node. |
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
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
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties) | Returns a collection that represents all the built-in document properties of the document. |
| [getChild(int nodeType, int index, boolean isDeep)](#getChild-int-int-boolean) |  |
| [getChildNodes()](#getChildNodes) | Gets all immediate child nodes of this node. |
| [getChildNodes(int nodeType, boolean isDeep)](#getChildNodes-int-boolean) |  |
| [getClass()](#getClass) |  |
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
| [getDocument()](#getDocument) |  |
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
| [hashCode()](#hashCode) |  |
| [importNode(Node srcNode, boolean isImportChildren)](#importNode-com.aspose.words.Node-boolean) | Imports a node from another document to the current document. |
| [importNode(Node srcNode, boolean isImportChildren, int importFormatMode)](#importNode-com.aspose.words.Node-boolean-int) |  |
| [indexOf(Node child)](#indexOf-com.aspose.words.Node) | Returns the index of the specified child node in the child node array. |
| [insertAfter(Node newChild, Node refChild)](#insertAfter-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately after the specified reference node. |
| [insertBefore(Node newChild, Node refChild)](#insertBefore-com.aspose.words.Node-com.aspose.words.Node) | Inserts the specified node immediately before the specified reference node. |
| [isComposite()](#isComposite) | Returns  true  as this node can have child nodes. |
| [iterator()](#iterator) | Provides support for the for each style iteration over the child nodes of this node. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting) | Joins runs with same formatting in all paragraphs of the document. |
| [nextPreOrder(Node rootNode)](#nextPreOrder-com.aspose.words.Node) | Gets next node according to the pre-order tree traversal algorithm. |
| [nodeTypeToString(int nodeType)](#nodeTypeToString-int) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes) | Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar/\#getFieldType) of [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/) in the whole document so that they correspond to the field types contained in the field codes. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [prependChild(Node newChild)](#prependChild-com.aspose.words.Node) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [previousPreOrder(Node rootNode)](#previousPreOrder-com.aspose.words.Node) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [print()](#print) | Prints the document without bringing up any user interface forms. |
| [print(String printerName)](#print-java.lang.String) | Print the whole document to the specified printer, using the standard (no User Interface) print controller. |
| [print(AttributeSet printerSettings)](#print-javax.print.attribute.AttributeSet) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller. |
| [print(AttributeSet printerSettings, String documentName)](#print-javax.print.attribute.AttributeSet-java.lang.String) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name. |
| [protect(int type)](#protect-int) |  |
| [protect(int type, String password)](#protect-int-java.lang.String) |  |
| [remove()](#remove) |  |
| [removeAllChildren()](#removeAllChildren) | Removes all the child nodes of the current node. |
| [removeChild(Node oldChild)](#removeChild-com.aspose.words.Node) | Removes the specified child node. |
| [removeExternalSchemaReferences()](#removeExternalSchemaReferences) | Removes external XML schema references from this document. |
| [removeMacros()](#removeMacros) | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
| [removeSmartTags()](#removeSmartTags) | Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. |
| [renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)](#renderToScale-int-java.awt.Graphics2D-float-float-float) | Renders a document page into a  object to a specified scale. |
| [renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-int-java.awt.Graphics2D-float-float-float-float) | Renders a document page into a  object to a specified size. |
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
| [updateFields()](#updateFields) | Updates the values of fields in the whole document. |
| [updateListLabels()](#updateListLabels) | Updates list labels for all list items in the document. |
| [updatePageLayout()](#updatePageLayout) | Rebuilds the page layout of the document. |
| [updateTableLayout()](#updateTableLayout) | Implements an earlier approach to table column widths re-calculation that has known issues. |
| [updateThumbnail()](#updateThumbnail) | Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document using default options. |
| [updateThumbnail(ThumbnailGeneratingOptions options)](#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions) | Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document according to the specified options. |
| [updateWordCount()](#updateWordCount) | Updates word count properties of the document. |
| [updateWordCount(boolean updateLinesCount)](#updateWordCount-boolean) | Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties/\#getLines) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties/\#setLines-int) property. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### Document() {#Document}
```
public Document()
```


Creates or loads a document.  Creates a blank Word document.

The document paper size is Letter by default. If you want to change page setup, use [Section.getPageSetup()](../../com.aspose.words/section/\#getPageSetup).

After creation, you can use [DocumentBuilder](../../com.aspose.words/documentbuilder/) to add document content easily.

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

Enumerates over this node and all of its children. Each node calls a corresponding method on [DocumentVisitor](../../com.aspose.words/documentvisitor/).

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor/) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if [DocumentVisitor](../../com.aspose.words/documentvisitor/) stopped the operation before visiting all nodes. Calls [DocumentVisitor.visitDocumentStart(com.aspose.words.Document)](../../com.aspose.words/documentvisitor/\#visitDocumentStart-com.aspose.words.Document), then calls [Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node/\#accept-com.aspose.words.DocumentVisitor) for all child nodes of the document and calls [DocumentVisitor.visitDocumentEnd(com.aspose.words.Document)](../../com.aspose.words/documentvisitor/\#visitDocumentEnd-com.aspose.words.Document) at the end.
### acceptAllRevisions() {#acceptAllRevisions}
```
public void acceptAllRevisions()
```


Accepts all tracked changes in the document. This method is a shortcut for [RevisionCollection.acceptAll()](../../com.aspose.words/revisioncollection/\#acceptAll).

### add(Shape watermark) {#add-com.aspose.words.Shape}
```
public void add(Shape watermark)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermark | [Shape](../../com.aspose.words/shape/) |  |

### appendChild(Node newChild) {#appendChild-com.aspose.words.Node}
```
public Node appendChild(Node newChild)
```


Adds the specified node to the end of the list of child nodes for this node.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
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

### cleanup(CleanupOptions options) {#cleanup-com.aspose.words.CleanupOptions}
```
public void cleanup(CleanupOptions options)
```


Cleans unused styles and lists from the document depending on given [CleanupOptions](../../com.aspose.words/cleanupoptions/).

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Document to compare. |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. The following document nodes are not compared at the moment:

 *  [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag/)
 *  Item3

Documents must not have revisions before comparison. |

### compare(Document document, String author, Date dateTime, CompareOptions options) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public void compare(Document document, String author, Date dateTime, CompareOptions options)
```


Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../com.aspose.words/revision/). Allows to specify comparison options using [CompareOptions](../../com.aspose.words/compareoptions/).

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


Copies styles from the specified template to a document. When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| template | [Document](../../com.aspose.words/document/) |  |

### copyStylesFromTemplate(String template) {#copyStylesFromTemplate-java.lang.String}
```
public void copyStylesFromTemplate(String template)
```


Copies styles from the specified template to a document. When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

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

**Returns:**
[Document](../../com.aspose.words/document/) - The cloned document.
### deepClone(boolean isCloneChildren) {#deepClone-boolean}
```
public Node deepClone(boolean isCloneChildren)
```


Creates a duplicate of the node.

This method serves as a copy constructor for nodes. The cloned node has no parent, but belongs to the same document as the original node.

This method always performs a deep copy of the node. The  isCloneChildren  parameter specifies whether to perform copy all child nodes as well.

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

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### expandTableStylesToDirectFormatting() {#expandTableStylesToDirectFormatting}
```
public void expandTableStylesToDirectFormatting()
```


Converts formatting specified in table styles into direct formatting on tables in the document.

This method exists because this version of Aspose.Words provides only limited support for table styles (see below). This method might be useful when you load a DOCX or WordprocessingML document that contains tables formatted with table styles and you need to query formatting of tables, cells, paragraphs or text.

This version of Aspose.Words provides limited support for table styles as follows:

 *  Table styles defined in DOCX or WordprocessingML documents are preserved as table styles when saving the document as DOCX or WordprocessingML.
 *  Table styles defined in DOCX or WordprocessingML documents are automatically converted to direct formatting on tables when saving the document into any other format, rendering or printing.
 *  Table styles defined in DOC documents are preserved as table styles when saving the document as DOC only.

### extractPages(int index, int count) {#extractPages-int-int}
```
public Document extractPages(int index, int count)
```


Returns the [Document](../../com.aspose.words/document/) object representing specified range of pages. The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' \\u2013 the numbering, headers/footers and cross tables layout will be preserved. But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort. Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document. Any feedback would be greatly appreciated.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ancestorType | java.lang.Class | The object type of the ancestor to retrieve. |

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The ancestor of the specified type or  null  if no ancestor of this type was found.

The ancestor type matches if it is equal to  ancestorType  or derived from  ancestorType .
### getAttachedTemplate() {#getAttachedTemplate}
```
public String getAttachedTemplate()
```


Gets the full path of the template attached to the document.

Empty string means the document is attached to the Normal template.

**Returns:**
java.lang.String - The full path of the template attached to the document.
### getAutomaticallyUpdateStyles() {#getAutomaticallyUpdateStyles}
```
public boolean getAutomaticallyUpdateStyles()
```


Gets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

**Returns:**
boolean - A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.
### getBackgroundShape() {#getBackgroundShape}
```
public Shape getBackgroundShape()
```


Gets the background shape of the document. Can be  null .

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype/\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions/\#getDisplayBackgroundShape) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions/\#setDisplayBackgroundShape-boolean) to  true .

**Returns:**
[Shape](../../com.aspose.words/shape/) - The background shape of the document.
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
### getChildNodes() {#getChildNodes}
```
public NodeCollection getChildNodes()
```


Gets all immediate child nodes of this node.

Note, [getChildNodes()](../../com.aspose.words/compositenode/\#getChildNodes) is equivalent to calling **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** with arguments ( [NodeType.ANY](../../com.aspose.words/nodetype/\#ANY),  false ) and creates and returns a new collection every time it is accessed.

If there are no child nodes, this property returns an empty collection.

**Returns:**
[NodeCollection](../../com.aspose.words/nodecollection/) - All immediate child nodes of this node.
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCompatibilityOptions() {#getCompatibilityOptions}
```
public CompatibilityOptions getCompatibilityOptions()
```


Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word).

**Returns:**
[CompatibilityOptions](../../com.aspose.words/compatibilityoptions/) - The corresponding [CompatibilityOptions](../../com.aspose.words/compatibilityoptions/) value.
### getCompliance() {#getCompliance}
```
public int getCompliance()
```


Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

If you created a new blank document or load non OOXML document returns the [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance/\#ECMA-376-2006) value.

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

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Returns:**
int - The corresponding  int  value.
### getCustomXmlParts() {#getCustomXmlParts}
```
public CustomXmlPartCollection getCustomXmlParts()
```


Gets the collection of Custom XML Data Storage Parts.

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

**Returns:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection/) - The collection of Custom XML Data Storage Parts.
### getDefaultTabStop() {#getDefaultTabStop}
```
public double getDefaultTabStop()
```


Gets the interval (in points) between the default tab stops.

**Returns:**
double - The interval (in points) between the default tab stops.
### getDigitalSignatures() {#getDigitalSignatures}
```
public DigitalSignatureCollection getDigitalSignatures()
```


Gets the collection of digital signatures for this document and their validation results.

This collection contains digital signatures that were loaded from the original document. These digital signatures will not be saved when you save this [Document](../../com.aspose.words/document/) object into a file or stream because saving or converting will produce a document that is different from the original and the original digital signatures will no longer be valid.

This collection is never  null . If the document is not signed, it will contain zero elements.

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


Gets the document to which this node belongs.

The node always belongs to a document even if it has just been created and not yet added to the tree, or if it has been removed from the tree.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/)
### getEndnoteOptions() {#getEndnoteOptions}
```
public EndnoteOptions getEndnoteOptions()
```


Provides options that control numbering and positioning of endnotes in this document.

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


Gets the first child of the node. If there is no first child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The first child of the node.
### getFirstSection() {#getFirstSection}
```
public Section getFirstSection()
```


Gets the first section in the document. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section/) - The first section in the document.
### getFontInfos() {#getFontInfos}
```
public FontInfoCollection getFontInfos()
```


Provides access to properties of fonts used in this document.

This collection of font definitions is loaded as is from the document. Font definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

**Returns:**
[FontInfoCollection](../../com.aspose.words/fontinfocollection/) - The corresponding [FontInfoCollection](../../com.aspose.words/fontinfocollection/) value.
### getFontSettings() {#getFontSettings}
```
public FontSettings getFontSettings()
```


Gets document font settings.

This property allows to specify font settings per document. If set to  null , default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) will be used.

The default value is  null .

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings/) - Document font settings.
### getFootnoteOptions() {#getFootnoteOptions}
```
public FootnoteOptions getFootnoteOptions()
```


Provides options that control numbering and positioning of footnotes in this document.

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions/) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions/) value.
### getFrameset() {#getFrameset}
```
public Frameset getFrameset()
```


Returns a [getFrameset()](../../com.aspose.words/document/\#getFrameset) instance if this document represents a frames page. If the document is not framed, the property has the  null  value.

**Returns:**
[Frameset](../../com.aspose.words/frameset/) - A [getFrameset()](../../com.aspose.words/document/\#getFrameset) instance if this document represents a frames page.
### getGlossaryDocument() {#getGlossaryDocument}
```
public GlossaryDocument getGlossaryDocument()
```


Gets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument/) object and assigning to this property.

**Returns:**
[GlossaryDocument](../../com.aspose.words/glossarydocument/) - The glossary document within this document or template.
### getGrammarChecked() {#getGrammarChecked}
```
public boolean getGrammarChecked()
```


Returns  true  if the document has been checked for grammar. To recheck the grammar in the document, set this property to  false .

**Returns:**
boolean - \{ true  if the document has been checked for grammar.
### getHyphenationOptions() {#getHyphenationOptions}
```
public HyphenationOptions getHyphenationOptions()
```


Provides access to document hyphenation options.

**Returns:**
[HyphenationOptions](../../com.aspose.words/hyphenationoptions/) - The corresponding [HyphenationOptions](../../com.aspose.words/hyphenationoptions/) value.
### getIncludeTextboxesFootnotesEndnotesInStat() {#getIncludeTextboxesFootnotesEndnotesInStat}
```
public boolean getIncludeTextboxesFootnotesEndnotesInStat()
```


Specifies whether to include textboxes, footnotes and endnotes in word count statistics.

**Returns:**
boolean - The corresponding  boolean  value.
### getJustificationMode() {#getJustificationMode}
```
public int getJustificationMode()
```


Gets the character spacing adjustment of a document.

**Returns:**
int - The character spacing adjustment of a document. The returned value is one of [JustificationMode](../../com.aspose.words/justificationmode/) constants.
### getLastChild() {#getLastChild}
```
public Node getLastChild()
```


Gets the last child of the node. If there is no last child node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The last child of the node.
### getLastSection() {#getLastSection}
```
public Section getLastSection()
```


Gets the last section in the document. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section/) - The last section in the document.
### getLayoutOptions() {#getLayoutOptions}
```
public LayoutOptions getLayoutOptions()
```


Gets a [LayoutOptions](../../com.aspose.words/layoutoptions/) object that represents options to control the layout process of this document.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions/) - A [LayoutOptions](../../com.aspose.words/layoutoptions/) object that represents options to control the layout process of this document.
### getLists() {#getLists}
```
public ListCollection getLists()
```


Provides access to the list formatting used in the document.

For more information see the description of the [ListCollection](../../com.aspose.words/listcollection/) class.

**Returns:**
[ListCollection](../../com.aspose.words/listcollection/) - The corresponding [ListCollection](../../com.aspose.words/listcollection/) value.
### getMailMerge() {#getMailMerge}
```
public MailMerge getMailMerge()
```


Returns a [MailMerge](../../com.aspose.words/mailmerge/) object that represents the mail merge functionality for the document.

**Returns:**
[MailMerge](../../com.aspose.words/mailmerge/) - A [MailMerge](../../com.aspose.words/mailmerge/) object that represents the mail merge functionality for the document.
### getMailMergeSettings() {#getMailMergeSettings}
```
public MailMergeSettings getMailMergeSettings()
```


Gets the object that contains all of the mail merge information for a document.

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


Gets the node immediately following this node. If there is no next node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately following this node.
### getNodeChangingCallback() {#getNodeChangingCallback}
```
public INodeChangingCallback getNodeChangingCallback()
```


Called when a node is inserted or removed in the document.

**Returns:**
[INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) - The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) value.
### getNodeType() {#getNodeType}
```
public int getNodeType()
```


Returns [NodeType.DOCUMENT](../../com.aspose.words/nodetype/\#DOCUMENT).

**Returns:**
int - \{[NodeType.DOCUMENT](../../com.aspose.words/nodetype/\#DOCUMENT). The returned value is one of [NodeType](../../com.aspose.words/nodetype/) constants.
### getOriginalFileName() {#getOriginalFileName}
```
public String getOriginalFileName()
```


Gets the original file name of the document.

Returns  null  if the document was loaded from a stream or created blank.

**Returns:**
java.lang.String - The original file name of the document.
### getOriginalLoadFormat() {#getOriginalLoadFormat}
```
public int getOriginalLoadFormat()
```


Gets the format of the original document that was loaded into this object.

If you created a new blank document, returns the [LoadFormat.DOC](../../com.aspose.words/loadformat/\#DOC) value.

**Returns:**
int - The format of the original document that was loaded into this object. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat/) constants.
### getPackageCustomParts() {#getPackageCustomParts}
```
public CustomPartCollection getPackageCustomParts()
```


Gets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document/\#getCustomXmlParts) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document/\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

**Returns:**
[CustomPartCollection](../../com.aspose.words/custompartcollection/) - The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".
### getPageColor() {#getPageColor}
```
public Color getPageColor()
```


Gets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**Returns:**
java.awt.Color - The page color of the document.
### getPageCount() {#getPageCount}
```
public int getPageCount()
```


Gets the number of pages in the document as calculated by the most recent page layout operation.

**Returns:**
int - The number of pages in the document as calculated by the most recent page layout operation.
### getPageInfo(int pageIndex) {#getPageInfo-int}
```
public PageInfo getPageInfo(int pageIndex)
```


Gets the page size, orientation and other information about a page that might be useful for printing or rendering.

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

If a node has just been created and not yet added to the tree, or if it has been removed from the tree, the parent is  null .

**Returns:**
[CompositeNode](../../com.aspose.words/compositenode/) - The immediate parent of this node.
### getPreviousSibling() {#getPreviousSibling}
```
public Node getPreviousSibling()
```


Gets the node immediately preceding this node. If there is no preceding node, a  null  is returned.

**Returns:**
[Node](../../com.aspose.words/node/) - The node immediately preceding this node.
### getProtectionType() {#getProtectionType}
```
public int getProtectionType()
```


Gets the currently active document protection type.

This property allows to retrieve the currently set document protection type. To change the document protection type use the **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** and [unprotect()](../../com.aspose.words/document/\#unprotect) methods.

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection)

**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**

**Returns:**
int - The currently active document protection type. The returned value is one of [ProtectionType](../../com.aspose.words/protectiontype/) constants.
### getRange() {#getRange}
```
public Range getRange()
```


Returns a [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.

**Returns:**
[Range](../../com.aspose.words/range/) - A [Range](../../com.aspose.words/range/) object that represents the portion of a document that is contained in this node.
### getRemovePersonalInformation() {#getRemovePersonalInformation}
```
public boolean getRemovePersonalInformation()
```


Gets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

**Returns:**
boolean - A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.
### getResourceLoadingCallback() {#getResourceLoadingCallback}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Allows to control how external resources are loaded.

**Returns:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) - The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value.
### getRevisions() {#getRevisions}
```
public RevisionCollection getRevisions()
```


Gets a collection of revisions (tracked changes) that exist in this document.

The returned collection is a "live" collection, which means if you remove parts of a document that contain revisions, the deleted revisions will automatically disappear from this collection.

**Returns:**
[RevisionCollection](../../com.aspose.words/revisioncollection/) - A collection of revisions (tracked changes) that exist in this document.
### getRevisionsView() {#getRevisionsView}
```
public int getRevisionsView()
```


Gets a value indicating whether to work with the original or revised version of a document. The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview/\#ORIGINAL)** .

**Returns:**
int - A value indicating whether to work with the original or revised version of a document. The returned value is one of [RevisionsView](../../com.aspose.words/revisionsview/) constants.
### getSections() {#getSections}
```
public SectionCollection getSections()
```


Returns a collection that represents all sections in the document.

**Returns:**
[SectionCollection](../../com.aspose.words/sectioncollection/) - A collection that represents all sections in the document.
### getShadeFormData() {#getShadeFormData}
```
public boolean getShadeFormData()
```


Specifies whether to turn on the gray shading on form fields.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowGrammaticalErrors() {#getShowGrammaticalErrors}
```
public boolean getShowGrammaticalErrors()
```


Specifies whether to display grammar errors in this document.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowSpellingErrors() {#getShowSpellingErrors}
```
public boolean getShowSpellingErrors()
```


Specifies whether to display spelling errors in this document.

**Returns:**
boolean - The corresponding  boolean  value.
### getSpellingChecked() {#getSpellingChecked}
```
public boolean getSpellingChecked()
```


Returns  true  if the document has been checked for spelling. To recheck the spelling in the document, set this property to  false .

**Returns:**
boolean - \{ true  if the document has been checked for spelling.
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Returns a collection of styles defined in the document.

For more information see the description of the [StyleCollection](../../com.aspose.words/stylecollection/) class.

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - A collection of styles defined in the document.
### getText() {#getText}
```
public String getText()
```


Gets the text of this node and of all its children.

The returned string includes all control and special characters as described in [ControlChar](../../com.aspose.words/controlchar/).

**Returns:**
java.lang.String
### getTheme() {#getTheme}
```
public Theme getTheme()
```


Gets the [getTheme()](../../com.aspose.words/document/\#getTheme) object for this document.

**Returns:**
[Theme](../../com.aspose.words/theme/) - The [getTheme()](../../com.aspose.words/document/\#getTheme) object for this document.
### getTrackRevisions() {#getTrackRevisions}
```
public boolean getTrackRevisions()
```


True if changes are tracked when this document is edited in Microsoft Word.

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document/\#startTrackRevisions-java.lang.String--java.util.Date) method.

**Returns:**
boolean - The corresponding  boolean  value.
### getVariables() {#getVariables}
```
public VariableCollection getVariables()
```


Returns the collection of variables added to a document or template.

**Returns:**
[VariableCollection](../../com.aspose.words/variablecollection/) - The collection of variables added to a document or template.
### getVbaProject() {#getVbaProject}
```
public VbaProject getVbaProject()
```


Gets a [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject).

**Returns:**
[VbaProject](../../com.aspose.words/vbaproject/) - A [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject).
### getVersionsCount() {#getVersionsCount}
```
public int getVersionsCount()
```


Gets the number of document versions that was stored in the DOC document.

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports versions only for DOC files.

This property allows to detect if there were document versions stored in this document before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions. If you save this document using Aspose.Words, the document will be saved without versions.

**Returns:**
int - The number of document versions that was stored in the DOC document.
### getViewOptions() {#getViewOptions}
```
public ViewOptions getViewOptions()
```


Provides options to control how the document is displayed in Microsoft Word.

**Returns:**
[ViewOptions](../../com.aspose.words/viewoptions/) - The corresponding [ViewOptions](../../com.aspose.words/viewoptions/) value.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document/\#getPageCount) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
### getWatermark() {#getWatermark}
```
public Watermark getWatermark()
```


Provides access to the document watermark.

**Returns:**
[Watermark](../../com.aspose.words/watermark/) - The corresponding [Watermark](../../com.aspose.words/watermark/) value.
### getWebExtensionTaskPanes() {#getWebExtensionTaskPanes}
```
public TaskPaneCollection getWebExtensionTaskPanes()
```


Returns a collection that represents a list of task pane add-ins.

**Returns:**
[TaskPaneCollection](../../com.aspose.words/taskpanecollection/) - A collection that represents a list of task pane add-ins.
### getWriteProtection() {#getWriteProtection}
```
public WriteProtection getWriteProtection()
```


Provides access to the document write protection options.

**Returns:**
[WriteProtection](../../com.aspose.words/writeprotection/) - The corresponding [WriteProtection](../../com.aspose.words/writeprotection/) value.
### hasChildNodes() {#hasChildNodes}
```
public boolean hasChildNodes()
```


Returns  true  if this node has any child nodes.

**Returns:**
boolean - \{ true  if this node has any child nodes.
### hasMacros() {#hasMacros}
```
public boolean hasMacros()
```


Returns  true  if the document has a VBA project (macros).

**Returns:**
boolean - \{ true  if the document has a VBA project (macros).
### hasRevisions() {#hasRevisions}
```
public boolean hasRevisions()
```


Returns  true  if the document has any tracked changes. This property is a shortcut for comparing [RevisionCollection.getCount()](../../com.aspose.words/revisioncollection/\#getCount) to zero.

**Returns:**
boolean - \{ true  if the document has any tracked changes.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### importNode(Node srcNode, boolean isImportChildren) {#importNode-com.aspose.words.Node-boolean}
```
public Node importNode(Node srcNode, boolean isImportChildren)
```


Imports a node from another document to the current document.

Imports a node from another document to the current document.

This method uses the [ImportFormatMode.USE\_DESTINATION\_STYLES](../../com.aspose.words/importformatmode/\#USE-DESTINATION-STYLES) option to resolve formatting.

Importing a node creates a copy of the source node belonging to the importing document. The returned node has no parent. The source node is not altered or removed from the original document.

Before a node from another document can be inserted into this document, it must be imported. During import, document-specific properties such as references to styles and lists are translated from the original to the importing document. After the node was imported, it can be inserted into the appropriate place in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertBefore-com.aspose.words.Node--com.aspose.words.Node) or [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode/\#insertAfter-com.aspose.words.Node--com.aspose.words.Node).

If the source node already belongs to the destination document, then simply a deep clone of the source node is created.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcNode | [Node](../../com.aspose.words/node/) | The node being imported. |
| isImportChildren | boolean | \{ true  to import all child nodes recursively; otherwise,  false . |

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


Returns the index of the specified child node in the child node array. Returns -1 if the node is not found in the child nodes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| child | [Node](../../com.aspose.words/node/) |  |

**Returns:**
int
### insertAfter(Node newChild, Node refChild) {#insertAfter-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertAfter(Node newChild, Node refChild)
```


Inserts the specified node immediately after the specified reference node.

If  refChild  is  null , inserts  newChild  at the beginning of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed after the  refChild . |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### insertBefore(Node newChild, Node refChild) {#insertBefore-com.aspose.words.Node-com.aspose.words.Node}
```
public Node insertBefore(Node newChild, Node refChild)
```


Inserts the specified node immediately before the specified reference node.

If  refChild  is  null , inserts  newChild  at the end of the list of child nodes.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) to insert. |
| refChild | [Node](../../com.aspose.words/node/) | The [Node](../../com.aspose.words/node/) that is the reference node. The  newChild  is placed before this node. |

**Returns:**
[Node](../../com.aspose.words/node/) - The inserted node.
### isComposite() {#isComposite}
```
public boolean isComposite()
```


Returns  true  as this node can have child nodes.

**Returns:**
boolean - \{ true  as this node can have child nodes.
### iterator() {#iterator}
```
public Iterator iterator()
```


Provides support for the for each style iteration over the child nodes of this node.

**Returns:**
java.util.Iterator
### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting}
```
public int joinRunsWithSameFormatting()
```


Joins runs with same formatting in all paragraphs of the document.

This is an optimization method. Some documents contain adjacent runs with same formatting. Usually this occurs if a document was intensively edited manually. You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../com.aspose.words/paragraph/) node in the document for adjacent [Run](../../com.aspose.words/run/) nodes having identical properties. It ignores unique identifiers used to track editing sessions of run creation and modification. First run in every joining sequence accumulates all text. Remaining runs are deleted from the document.

**Returns:**
int - Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
### nextPreOrder(Node rootNode) {#nextPreOrder-com.aspose.words.Node}
```
public Node nextPreOrder(Node rootNode)
```


Gets next node according to the pre-order tree traversal algorithm.

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

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [Range.normalizeFieldTypes()](../../com.aspose.words/range/\#normalizeFieldTypes).

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### prependChild(Node newChild) {#prependChild-com.aspose.words.Node}
```
public Node prependChild(Node newChild)
```


Adds the specified node to the beginning of the list of child nodes for this node.

If the  newChild  is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use **M:Aspose.Words.DocumentBase.ImportNode(Aspose.Words.Node,System.Boolean,Aspose.Words.ImportFormatMode)** to import the node to the current document. The imported node can then be inserted into the current document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| newChild | [Node](../../com.aspose.words/node/) | The node to add. |

**Returns:**
[Node](../../com.aspose.words/node/) - The node added.
### previousPreOrder(Node rootNode) {#previousPreOrder-com.aspose.words.Node}
```
public Node previousPreOrder(Node rootNode)
```


Gets the previous node according to the pre-order tree traversal algorithm.

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

The  object allows you to specify the printer to print on, the range of pages of to print and other options.

The  can contain both  to configure PrintJob request and  to configure PrintService lookup.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| printerSettings | javax.print.attribute.AttributeSet | The printer settings to use. |

### print(AttributeSet printerSettings, String documentName) {#print-javax.print.attribute.AttributeSet-java.lang.String}
```
public void print(AttributeSet printerSettings, String documentName)
```


Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name.

The  object allows you to specify the printer to print on, the range of pages of to print and other options.

The  can contain both  to configure PrintJob request and  to configure PrintService lookup.

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

### removeAllChildren() {#removeAllChildren}
```
public void removeAllChildren()
```


Removes all the child nodes of the current node.

### removeChild(Node oldChild) {#removeChild-com.aspose.words.Node}
```
public Node removeChild(Node oldChild)
```


Removes the specified child node.

The parent of  oldChild  is set to  null  after the node is removed.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| oldChild | [Node](../../com.aspose.words/node/) | The node to remove. |

**Returns:**
[Node](../../com.aspose.words/node/) - The removed node.
### removeExternalSchemaReferences() {#removeExternalSchemaReferences}
```
public void removeExternalSchemaReferences()
```


Removes external XML schema references from this document.

### removeMacros() {#removeMacros}
```
public void removeMacros()
```


Removes all macros (the VBA project) as well as toolbars and command customizations from the document.

By removing all macros from a document you can ensure the document contains no macro viruses.

### removeSmartTags() {#removeSmartTags}
```
public void removeSmartTags()
```


Removes all [SmartTag](../../com.aspose.words/smarttag/) descendant nodes of the current node. This method does not remove the content of the smart tags.

### renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale) {#renderToScale-int-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)
```


Renders a document page into a  object to a specified scale.

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


Renders a document page into a  object to a specified size.

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

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

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

Only expressions with element names are supported at the moment. Expressions that use attribute names are not supported.

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

Empty string means the document is attached to the Normal template.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The full path of the template attached to the document. |

### setAutomaticallyUpdateStyles(boolean value) {#setAutomaticallyUpdateStyles-boolean}
```
public void setAutomaticallyUpdateStyles(boolean value)
```


Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |

### setBackgroundShape(Shape value) {#setBackgroundShape-com.aspose.words.Shape}
```
public void setBackgroundShape(Shape value)
```


Sets the background shape of the document. Can be  null .

Microsoft Word allows only a shape that has its [ShapeBase.getShapeType()](../../com.aspose.words/shapebase/\#getShapeType) property equal to [ShapeType.RECTANGLE](../../com.aspose.words/shapetype/\#RECTANGLE) to be used as a background shape for a document.

Microsoft Word supports only the fill properties of a background shape. All other properties are ignored.

Setting this property to a non-null value will also set the [ViewOptions.getDisplayBackgroundShape()](../../com.aspose.words/viewoptions/\#getDisplayBackgroundShape) / [ViewOptions.setDisplayBackgroundShape(boolean)](../../com.aspose.words/viewoptions/\#setDisplayBackgroundShape-boolean) to  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape/) | The background shape of the document. |

### setCustomNodeId(int value) {#setCustomNodeId-int}
```
public void setCustomNodeId(int value)
```


Specifies custom node identifier.

Default is zero.

This identifier can be set and used arbitrarily. For example, as a key to get external data.

Important note, specified value is not saved to an output file and exists only during the node lifetime.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setCustomXmlParts(CustomXmlPartCollection value) {#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection}
```
public void setCustomXmlParts(CustomXmlPartCollection value)
```


Sets the collection of Custom XML Data Storage Parts.

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection/) | The collection of Custom XML Data Storage Parts. |

### setDefaultTabStop(double value) {#setDefaultTabStop-double}
```
public void setDefaultTabStop(double value)
```


Sets the interval (in points) between the default tab stops.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The interval (in points) between the default tab stops. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings}
```
public void setFontSettings(FontSettings value)
```


Sets document font settings.

This property allows to specify font settings per document. If set to  null , default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings/\#getDefaultInstance) will be used.

The default value is  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings/) | Document font settings. |

### setGlossaryDocument(GlossaryDocument value) {#setGlossaryDocument-com.aspose.words.GlossaryDocument}
```
public void setGlossaryDocument(GlossaryDocument value)
```


Sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument/) object and assigning to this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [GlossaryDocument](../../com.aspose.words/glossarydocument/) | The glossary document within this document or template. |

### setGrammarChecked(boolean value) {#setGrammarChecked-boolean}
```
public void setGrammarChecked(boolean value)
```


Returns  true  if the document has been checked for grammar. To recheck the grammar in the document, set this property to  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | \{ true  if the document has been checked for grammar. |

### setIncludeTextboxesFootnotesEndnotesInStat(boolean value) {#setIncludeTextboxesFootnotesEndnotesInStat-boolean}
```
public void setIncludeTextboxesFootnotesEndnotesInStat(boolean value)
```


Specifies whether to include textboxes, footnotes and endnotes in word count statistics.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setJustificationMode(int value) {#setJustificationMode-int}
```
public void setJustificationMode(int value)
```


Sets the character spacing adjustment of a document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The character spacing adjustment of a document. The value must be one of [JustificationMode](../../com.aspose.words/justificationmode/) constants. |

### setMailMergeSettings(MailMergeSettings value) {#setMailMergeSettings-com.aspose.words.MailMergeSettings}
```
public void setMailMergeSettings(MailMergeSettings value)
```


Sets the object that contains all of the mail merge information for a document.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) | The corresponding [INodeChangingCallback](../../com.aspose.words/inodechangingcallback/) value. |

### setPackageCustomParts(CustomPartCollection value) {#setPackageCustomParts-com.aspose.words.CustomPartCollection}
```
public void setPackageCustomParts(CustomPartCollection value)
```


Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document/\#getCustomXmlParts) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document/\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart/).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CustomPartCollection](../../com.aspose.words/custompartcollection/) | The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |

### setPageColor(Color value) {#setPageColor-java.awt.Color}
```
public void setPageColor(Color value)
```


Sets the page color of the document. This property is a simpler version of [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [getBackgroundShape()](../../com.aspose.words/documentbase/\#getBackgroundShape) / [setBackgroundShape(com.aspose.words.Shape)](../../com.aspose.words/documentbase/\#setBackgroundShape-com.aspose.words.Shape).

If the page color is not set (e.g. there is no background shape in the document) returns a zero color.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | The page color of the document. |

### setRemovePersonalInformation(boolean value) {#setRemovePersonalInformation-boolean}
```
public void setRemovePersonalInformation(boolean value)
```


Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Allows to control how external resources are loaded.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) | The corresponding [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback/) value. |

### setRevisionsView(int value) {#setRevisionsView-int}
```
public void setRevisionsView(int value)
```


Sets a value indicating whether to work with the original or revised version of a document. The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview/\#ORIGINAL)** .

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowGrammaticalErrors(boolean value) {#setShowGrammaticalErrors-boolean}
```
public void setShowGrammaticalErrors(boolean value)
```


Specifies whether to display grammar errors in this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowSpellingErrors(boolean value) {#setShowSpellingErrors-boolean}
```
public void setShowSpellingErrors(boolean value)
```


Specifies whether to display spelling errors in this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSpellingChecked(boolean value) {#setSpellingChecked-boolean}
```
public void setSpellingChecked(boolean value)
```


Returns  true  if the document has been checked for spelling. To recheck the spelling in the document, set this property to  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | \{ true  if the document has been checked for spelling. |

### setTrackRevisions(boolean value) {#setTrackRevisions-boolean}
```
public void setTrackRevisions(boolean value)
```


True if changes are tracked when this document is edited in Microsoft Word.

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document/\#startTrackRevisions-java.lang.String--java.util.Date) method.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setVbaProject(VbaProject value) {#setVbaProject-com.aspose.words.VbaProject}
```
public void setVbaProject(VbaProject value)
```


Sets a [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [VbaProject](../../com.aspose.words/vbaproject/) | A [getVbaProject()](../../com.aspose.words/document/\#getVbaProject) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document/\#setVbaProject-com.aspose.words.VbaProject). |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. Document may generate warnings at any stage of its existence, so it's important to setup warning callback as early as possible to avoid the warnings loss. E.g. such properties as [Document.getPageCount()](../../com.aspose.words/document/\#getPageCount) actually build the document layout which is used later for rendering, and the layout warnings may be lost if warning callback is specified just for the rendering calls later.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

### startTrackRevisions(String author) {#startTrackRevisions-java.lang.String}
```
public void startTrackRevisions(String author)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder/)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document/\#getTrackRevisions) / [setTrackRevisions(boolean)](../../com.aspose.words/document/\#setTrackRevisions-boolean) option and does not use its value for the purposes of revision tracking.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |

### startTrackRevisions(String author, Date dateTime) {#startTrackRevisions-java.lang.String-java.util.Date}
```
public void startTrackRevisions(String author, Date dateTime)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder/)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document/\#getTrackRevisions) / [setTrackRevisions(boolean)](../../com.aspose.words/document/\#setTrackRevisions-boolean) option and does not use its value for the purposes of revision tracking.

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

Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [Range.unlinkFields()](../../com.aspose.words/range/\#unlinkFields).

### unprotect() {#unprotect}
```
public void unprotect()
```


Removes protection from the document.  Removes protection from the document regardless of the password.

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

### unprotect(String password) {#unprotect-java.lang.String}
```
public boolean unprotect(String password)
```


Removes protection from the document if a correct password is specified.

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document/\#getWriteProtection).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to unprotect the document with. |

**Returns:**
boolean - \{ true  if a correct password was specified and the document was unprotected.
### updateFields() {#updateFields}
```
public void updateFields()
```


Updates the values of fields in the whole document.

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

Use the [normalizeFieldTypes()](../../com.aspose.words/document/\#normalizeFieldTypes) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.updateFields()](../../com.aspose.words/range/\#updateFields).

### updateListLabels() {#updateListLabels}
```
public void updateListLabels()
```


Updates list labels for all list items in the document.

This method updates list label properties such as [ListLabel.getLabelValue()](../../com.aspose.words/listlabel/\#getLabelValue) and [ListLabel.getLabelString()](../../com.aspose.words/listlabel/\#getLabelString) for each [Paragraph.getListLabel()](../../com.aspose.words/paragraph/\#getListLabel) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.

### updatePageLayout() {#updatePageLayout}
```
public void updatePageLayout()
```


Rebuilds the page layout of the document.

This method formats a document into pages and updates the page number related fields in the document such as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it. However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not update the page layout automatically. In this case you should call [updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout) before rendering again.

### updateTableLayout() {#updateTableLayout}
```
public void updateTableLayout()
```


Implements an earlier approach to table column widths re-calculation that has known issues. The method is deprecated and it will be removed in a few releases.

### updateThumbnail() {#updateThumbnail}
```
public void updateThumbnail()
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document using default options.

### updateThumbnail(ThumbnailGeneratingOptions options) {#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions}
```
public void updateThumbnail(ThumbnailGeneratingOptions options)
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties/\#getThumbnail) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties/\#setThumbnail-byte) of the document according to the specified options. The [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions/) allows you to specify the source of thumbnail, size and other options. If attempt to generate thumbnail fails, doesn't change one.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions/) | The generating options to use. |

### updateWordCount() {#updateWordCount}
```
public void updateWordCount()
```


Updates word count properties of the document.

[updateWordCount()](../../com.aspose.words/document/\#updateWordCount) recalculates and updates Characters, Words and Paragraphs properties in the [getBuiltInDocumentProperties()](../../com.aspose.words/document/\#getBuiltInDocumentProperties) collection of the [Document](../../com.aspose.words/document/).

Note that [updateWordCount()](../../com.aspose.words/document/\#updateWordCount) does not update number of lines and pages properties. Use the [updateWordCount()](../../com.aspose.words/document/\#updateWordCount) overload and pass  true  value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included in the word count.

### updateWordCount(boolean updateLinesCount) {#updateWordCount-boolean}
```
public void updateWordCount(boolean updateLinesCount)
```


Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties/\#getLines) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties/\#setLines-int) property. This method will rebuild page layout of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| updateLinesCount | boolean | \{ true  if number of lines in the document shall be calculated. |

### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

