---
title: Document
second_title: Aspose.Words for Java API Reference
description: Represents a Word document.
type: docs
weight: 120
url: /java/com.aspose.words/document/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Node](../../com.aspose.words/node), [com.aspose.words.CompositeNode](../../com.aspose.words/compositenode), [com.aspose.words.DocumentBase](../../com.aspose.words/documentbase)
```
public class Document extends DocumentBase
```

Represents a Word document.

To learn more, visit the **Working with Document** documentation article.

The **Document** is a central object in the Aspose.Words library.

To load an existing document in any of the [LoadFormat](../../com.aspose.words/loadformat) formats, pass a file name or a stream into one of the **Document** constructors. To create a blank document, call the constructor without parameters.

Use one of the Save method overloads to save the document in any of the [SaveFormat](../../com.aspose.words/saveformat) formats.

To draw document pages directly onto a **Graphics** object use [renderToScale(int, java.awt.Graphics2D, float, float, float)](../../com.aspose.words/document\#renderToScale-int--java.awt.Graphics2D--float--float--float-) or [renderToSize(int, java.awt.Graphics2D, float, float, float, float)](../../com.aspose.words/document\#renderToSize-int--java.awt.Graphics2D--float--float--float--float-) method.

To print the document, use one of the [print(java.lang.String)](../../com.aspose.words/document\#print-java.lang.String-) methods.

[getMailMerge()](../../com.aspose.words/document\#getMailMerge--) is the Aspose.Words's reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a java.sql.ResultSet or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

**Document** stores document-wide information such as [DocumentBase.getStyles()](../../com.aspose.words/documentbase\#getStyles--), [getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--), [getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--), lists and macros. Most of these objects are accessible via the corresponding properties of the **Document**.

The **Document** is a root node of a tree that contains all other nodes of the document. The tree is a Composite design pattern and in many ways similar to XmlDocument. The content of the document can be manipulated freely programmatically:

 *  The nodes of the document can be accessed via typed collections, for example [getSections()](../../com.aspose.words/document\#getSections--), [ParagraphCollection](../../com.aspose.words/paragraphcollection) etc.
 *  The nodes of the document can be selected by their node type using **M:Aspose.Words.CompositeNode.GetChildNodes(Aspose.Words.NodeType,System.Boolean)** or using an XPath query with [CompositeNode.selectNodes(java.lang.String)](../../com.aspose.words/compositenode\#selectNodes-java.lang.String-) or [CompositeNode.selectSingleNode(java.lang.String)](../../com.aspose.words/compositenode\#selectSingleNode-java.lang.String-).
 *  Content nodes can be added or removed from anywhere in the document using [CompositeNode.insertBefore(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertBefore-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.insertAfter(com.aspose.words.Node, com.aspose.words.Node)](../../com.aspose.words/compositenode\#insertAfter-com.aspose.words.Node--com.aspose.words.Node-), [CompositeNode.removeChild(com.aspose.words.Node)](../../com.aspose.words/compositenode\#removeChild-com.aspose.words.Node-) and other methods provided by the base class [CompositeNode](../../com.aspose.words/compositenode).
 *  The formatting attributes of each node can be changed via the properties of that node.

Consider using [DocumentBuilder](../../com.aspose.words/documentbuilder) that simplifies the task of programmatically creating or populating the document tree.

The **Document** can contain only [Section](../../com.aspose.words/section) objects.

In Microsoft Word, a valid document needs to have at least one section.
## Constructors

| Constructor | Description |
| --- | --- |
| [Document()](#Document--) | Creates or loads a document. |
| [Document(String fileName)](#Document-java.lang.String-) | Opens an existing document from a file. |
| [Document(String fileName, LoadOptions loadOptions)](#Document-java.lang.String-com.aspose.words.LoadOptions-) | Opens an existing document from a file. |
| [Document(InputStream stream)](#Document-java.io.InputStream-) | Initializes a new instance of this class. |
| [Document(InputStream stream, LoadOptions loadOptions)](#Document-java.io.InputStream-com.aspose.words.LoadOptions-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [getAttachedTemplate()](#getAttachedTemplate--) | Gets the full path of the template attached to the document. |
| [setAttachedTemplate(String value)](#setAttachedTemplate-java.lang.String-) | Sets the full path of the template attached to the document. |
| [getAutomaticallyUpdateStyles()](#getAutomaticallyUpdateStyles--) | Gets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [setAutomaticallyUpdateStyles(boolean value)](#setAutomaticallyUpdateStyles-boolean-) | Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [getShadeFormData()](#getShadeFormData--) | Specifies whether to turn on the gray shading on form fields. |
| [setShadeFormData(boolean value)](#setShadeFormData-boolean-) | Specifies whether to turn on the gray shading on form fields. |
| [getTrackRevisions()](#getTrackRevisions--) | **True** if changes are tracked when this document is edited in Microsoft Word. |
| [setTrackRevisions(boolean value)](#setTrackRevisions-boolean-) | **True** if changes are tracked when this document is edited in Microsoft Word. |
| [getShowGrammaticalErrors()](#getShowGrammaticalErrors--) | Specifies whether to display grammar errors in this document. |
| [setShowGrammaticalErrors(boolean value)](#setShowGrammaticalErrors-boolean-) | Specifies whether to display grammar errors in this document. |
| [getShowSpellingErrors()](#getShowSpellingErrors--) | Specifies whether to display spelling errors in this document. |
| [setShowSpellingErrors(boolean value)](#setShowSpellingErrors-boolean-) | Specifies whether to display spelling errors in this document. |
| [getSpellingChecked()](#getSpellingChecked--) | Returns **true** if the document has been checked for spelling. |
| [setSpellingChecked(boolean value)](#setSpellingChecked-boolean-) | Returns **true** if the document has been checked for spelling. |
| [getGrammarChecked()](#getGrammarChecked--) | Returns **true** if the document has been checked for grammar. |
| [setGrammarChecked(boolean value)](#setGrammarChecked-boolean-) | Returns **true** if the document has been checked for grammar. |
| [getNodeType()](#getNodeType--) | Returns **NodeType.Document**. |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties--) | Returns a collection that represents all the built-in document properties of the document. |
| [getWebExtensionTaskPanes()](#getWebExtensionTaskPanes--) | Returns a collection that represents a list of task pane add-ins. |
| [getCustomDocumentProperties()](#getCustomDocumentProperties--) | Returns a collection that represents all the custom document properties of the document. |
| [getMailMerge()](#getMailMerge--) | Returns a **MailMerge** object that represents the mail merge functionality for the document. |
| [getProtectionType()](#getProtectionType--) | Gets the currently active document protection type. |
| [getSections()](#getSections--) | Returns a collection that represents all sections in the document. |
| [getFirstSection()](#getFirstSection--) | Gets the first section in the document. |
| [getLastSection()](#getLastSection--) | Gets the last section in the document. |
| [getViewOptions()](#getViewOptions--) | Provides options to control how the document is displayed in Microsoft Word. |
| [getWriteProtection()](#getWriteProtection--) | Provides access to the document write protection options. |
| [getCompatibilityOptions()](#getCompatibilityOptions--) | Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word). |
| [getMailMergeSettings()](#getMailMergeSettings--) | Gets the object that contains all of the mail merge information for a document. |
| [setMailMergeSettings(MailMergeSettings value)](#setMailMergeSettings-com.aspose.words.MailMergeSettings-) | Sets the object that contains all of the mail merge information for a document. |
| [getHyphenationOptions()](#getHyphenationOptions--) | Provides access to document hyphenation options. |
| [hasRevisions()](#hasRevisions--) | Returns **true** if the document has any tracked changes. |
| [hasMacros()](#hasMacros--) | Returns **true** if the document has a VBA project (macros). |
| [getWatermark()](#getWatermark--) | Provides access to the document watermark. |
| [getVersionsCount()](#getVersionsCount--) | Gets the number of document versions that was stored in the DOC document. |
| [getDefaultTabStop()](#getDefaultTabStop--) | Gets the interval (in points) between the default tab stops. |
| [setDefaultTabStop(double value)](#setDefaultTabStop-double-) | Sets the interval (in points) between the default tab stops. |
| [getTheme()](#getTheme--) | Gets the [getTheme()](../../com.aspose.words/document\#getTheme--) object for this document. |
| [getCustomXmlParts()](#getCustomXmlParts--) | Gets the collection of Custom XML Data Storage Parts. |
| [setCustomXmlParts(CustomXmlPartCollection value)](#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) | Sets the collection of Custom XML Data Storage Parts. |
| [getPackageCustomParts()](#getPackageCustomParts--) | Gets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [setPackageCustomParts(CustomPartCollection value)](#setPackageCustomParts-com.aspose.words.CustomPartCollection-) | Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [getVariables()](#getVariables--) | Returns the collection of variables added to a document or template. |
| [getGlossaryDocument()](#getGlossaryDocument--) | Gets the glossary document within this document or template. |
| [setGlossaryDocument(GlossaryDocument value)](#setGlossaryDocument-com.aspose.words.GlossaryDocument-) | Sets the glossary document within this document or template. |
| [getOriginalFileName()](#getOriginalFileName--) | Gets the original file name of the document. |
| [getOriginalLoadFormat()](#getOriginalLoadFormat--) | Gets the format of the original document that was loaded into this object. |
| [getCompliance()](#getCompliance--) | Gets the OOXML compliance version determined from the loaded document content. |
| [getDigitalSignatures()](#getDigitalSignatures--) | Gets the collection of digital signatures for this document and their validation results. |
| [getFontSettings()](#getFontSettings--) | Gets document font settings. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | Sets document font settings. |
| [getFrameset()](#getFrameset--) | Returns a [getFrameset()](../../com.aspose.words/document\#getFrameset--) instance if this document represents a frames page. |
| [deepClone()](#deepClone--) | Performs a deep copy of the [Document](../../com.aspose.words/document). |
| [accept(DocumentVisitor visitor)](#accept-com.aspose.words.DocumentVisitor-) | Accepts a visitor. |
| [appendDocument(Document srcDoc, int importFormatMode)](#appendDocument-com.aspose.words.Document-int-) |  |
| [appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-) |  |
| [save(String fileName)](#save-java.lang.String-) | Saves the document. |
| [save(String fileName, int saveFormat)](#save-java.lang.String-int-) |  |
| [save(String fileName, SaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SaveOptions-) | Saves the document to a file using the specified save options. |
| [save(OutputStream stream, int saveFormat)](#save-java.io.OutputStream-int-) |  |
| [save(OutputStream stream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions-) |  |
| [ensureMinimum()](#ensureMinimum--) | If the document contains no sections, creates one section with one paragraph. |
| [acceptAllRevisions()](#acceptAllRevisions--) | Accepts all tracked changes in the document. |
| [protect(int type)](#protect-int-) |  |
| [protect(int type, String password)](#protect-int-java.lang.String-) |  |
| [unprotect()](#unprotect--) | Removes protection from the document. |
| [unprotect(String password)](#unprotect-java.lang.String-) | Removes protection from the document if a correct password is specified. |
| [updateWordCount()](#updateWordCount--) | Updates word count properties of the document. |
| [updateWordCount(boolean updateLinesCount)](#updateWordCount-boolean-) | Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-) property. |
| [updateTableLayout()](#updateTableLayout--) | Implements an earlier approach to table column widths re-calculation that has known issues. |
| [updateListLabels()](#updateListLabels--) | Updates list labels for all list items in the document. |
| [removeMacros()](#removeMacros--) | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
| [updateFields()](#updateFields--) | Updates the values of fields in the whole document. |
| [unlinkFields()](#unlinkFields--) | Unlinks fields in the whole document. |
| [normalizeFieldTypes()](#normalizeFieldTypes--) | Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) of [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) in the whole document so that they correspond to the field types contained in the field codes. |
| [joinRunsWithSameFormatting()](#joinRunsWithSameFormatting--) | Joins runs with same formatting in all paragraphs of the document. |
| [expandTableStylesToDirectFormatting()](#expandTableStylesToDirectFormatting--) | Converts formatting specified in table styles into direct formatting on tables in the document. |
| [cleanup()](#cleanup--) | Cleans unused styles and lists from the document. |
| [cleanup(CleanupOptions options)](#cleanup-com.aspose.words.CleanupOptions-) | Cleans unused styles and lists from the document depending on given [CleanupOptions](../../com.aspose.words/cleanupoptions). |
| [removeExternalSchemaReferences()](#removeExternalSchemaReferences--) | Removes external XML schema references from this document. |
| [startTrackRevisions(String author, Date dateTime)](#startTrackRevisions-java.lang.String-java.util.Date-) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [startTrackRevisions(String author)](#startTrackRevisions-java.lang.String-) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [stopTrackRevisions()](#stopTrackRevisions--) | Stops automatic marking of document changes as revisions. |
| [compare(Document document, String author, Date dateTime)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-) | Compares this document with another document producing changes as number of edit and format revisions [Revision](../../com.aspose.words/revision). |
| [compare(Document document, String author, Date dateTime, CompareOptions options)](#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-) | Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../com.aspose.words/revision). |
| [copyStylesFromTemplate(String template)](#copyStylesFromTemplate-java.lang.String-) | Copies styles from the specified template to a document. |
| [copyStylesFromTemplate(Document template)](#copyStylesFromTemplate-com.aspose.words.Document-) | Copies styles from the specified template to a document. |
| [getPageCount()](#getPageCount--) | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [getRevisions()](#getRevisions--) | Gets a collection of revisions (tracked changes) that exist in this document. |
| [getLayoutOptions()](#getLayoutOptions--) | Gets a **LayoutOptions** object that represents options to control the layout process of this document. |
| [getRevisionsView()](#getRevisionsView--) | Gets a value indicating whether to work with the original or revised version of a document. |
| [setRevisionsView(int value)](#setRevisionsView-int-) | Sets a value indicating whether to work with the original or revised version of a document. |
| [updatePageLayout()](#updatePageLayout--) | Rebuilds the page layout of the document. |
| [renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale)](#renderToScale-int-java.awt.Graphics2D-float-float-float-) | Renders a document page into a  object to a specified scale. |
| [renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-int-java.awt.Graphics2D-float-float-float-float-) | Renders a document page into a  object to a specified size. |
| [add(Shape watermark)](#add-com.aspose.words.Shape-) |  |
| [get()](#get--) |  |
| [remove()](#remove--) |  |
| [getPageInfo(int pageIndex)](#getPageInfo-int-) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
| [print()](#print--) | Prints the document without bringing up any user interface forms. |
| [print(String printerName)](#print-java.lang.String-) | Print the whole document to the specified printer, using the standard (no User Interface) print controller. |
| [print(AttributeSet printerSettings)](#print-javax.print.attribute.AttributeSet-) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller. |
| [print(AttributeSet printerSettings, String documentName)](#print-javax.print.attribute.AttributeSet-java.lang.String-) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name. |
| [updateThumbnail(ThumbnailGeneratingOptions options)](#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-) | Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) of the document according to the specified options. |
| [updateThumbnail()](#updateThumbnail--) | Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) of the document using default options. |
| [extractPages(int index, int count)](#extractPages-int-int-) | Returns the [Document](../../com.aspose.words/document) object representing specified range of pages. |
| [getFootnoteOptions()](#getFootnoteOptions--) | Provides options that control numbering and positioning of footnotes in this document. |
| [getEndnoteOptions()](#getEndnoteOptions--) | Provides options that control numbering and positioning of endnotes in this document. |
| [getDirectSectionAttr(int key)](#getDirectSectionAttr-int-) |  |
| [fetchInheritedSectionAttr(int key)](#fetchInheritedSectionAttr-int-) |  |
| [fetchSectionAttr(int key)](#fetchSectionAttr-int-) |  |
| [setSectionAttr(int key, Object value)](#setSectionAttr-int-java.lang.Object-) |  |
| [clearSectionAttrs()](#clearSectionAttrs--) |  |
| [getFieldOptions()](#getFieldOptions--) | Gets a **FieldOptions** object that represents options to control field handling in the document. |
| [getRemovePersonalInformation()](#getRemovePersonalInformation--) | Gets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [setRemovePersonalInformation(boolean value)](#setRemovePersonalInformation-boolean-) | Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [getVbaProject()](#getVbaProject--) | Gets a [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
| [setVbaProject(VbaProject value)](#setVbaProject-com.aspose.words.VbaProject-) | Sets a [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |
### Document() {#Document--}
```
public Document()
```


Creates or loads a document.  Creates a blank Word document.

The document paper size is Letter by default. If you want to change page setup, use [Section.getPageSetup()](../../com.aspose.words/section\#getPageSetup--).

After creation, you can use [DocumentBuilder](../../com.aspose.words/documentbuilder) to add document content easily.

### Document(String fileName) {#Document-java.lang.String-}
```
public Document(String fileName)
```


Opens an existing document from a file. Automatically detects the file format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | File name of the document to open. |

### Document(String fileName, LoadOptions loadOptions) {#Document-java.lang.String-com.aspose.words.LoadOptions-}
```
public Document(String fileName, LoadOptions loadOptions)
```


Opens an existing document from a file. Allows to specify additional options such as an encryption password.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | File name of the document to open. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) | Additional options to use when loading a document. Can be null. |

### Document(InputStream stream) {#Document-java.io.InputStream-}
```
public Document(InputStream stream)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### Document(InputStream stream, LoadOptions loadOptions) {#Document-java.io.InputStream-com.aspose.words.LoadOptions-}
```
public Document(InputStream stream, LoadOptions loadOptions)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |

### getAttachedTemplate() {#getAttachedTemplate--}
```
public String getAttachedTemplate()
```


Gets the full path of the template attached to the document.

Empty string means the document is attached to the Normal template.

**Returns:**
java.lang.String - The full path of the template attached to the document.
### setAttachedTemplate(String value) {#setAttachedTemplate-java.lang.String-}
```
public void setAttachedTemplate(String value)
```


Sets the full path of the template attached to the document.

Empty string means the document is attached to the Normal template.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The full path of the template attached to the document. |

### getAutomaticallyUpdateStyles() {#getAutomaticallyUpdateStyles--}
```
public boolean getAutomaticallyUpdateStyles()
```


Gets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

**Returns:**
boolean - A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.
### setAutomaticallyUpdateStyles(boolean value) {#setAutomaticallyUpdateStyles-boolean-}
```
public void setAutomaticallyUpdateStyles(boolean value)
```


Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |

### getShadeFormData() {#getShadeFormData--}
```
public boolean getShadeFormData()
```


Specifies whether to turn on the gray shading on form fields.

**Returns:**
boolean - The corresponding  boolean  value.
### setShadeFormData(boolean value) {#setShadeFormData-boolean-}
```
public void setShadeFormData(boolean value)
```


Specifies whether to turn on the gray shading on form fields.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTrackRevisions() {#getTrackRevisions--}
```
public boolean getTrackRevisions()
```


**True** if changes are tracked when this document is edited in Microsoft Word.

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-) method.

**Returns:**
boolean - The corresponding  boolean  value.
### setTrackRevisions(boolean value) {#setTrackRevisions-boolean-}
```
public void setTrackRevisions(boolean value)
```


**True** if changes are tracked when this document is edited in Microsoft Word.

Setting this option only instructs Microsoft Word whether the track changes is turned on or off. This property has no effect on changes to the document that you make programmatically via Aspose.Words.

If you want to automatically track changes as they are made programmatically by Aspose.Words to this document use the [startTrackRevisions(java.lang.String, java.util.Date)](../../com.aspose.words/document\#startTrackRevisions-java.lang.String--java.util.Date-) method.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShowGrammaticalErrors() {#getShowGrammaticalErrors--}
```
public boolean getShowGrammaticalErrors()
```


Specifies whether to display grammar errors in this document.

**Returns:**
boolean - The corresponding  boolean  value.
### setShowGrammaticalErrors(boolean value) {#setShowGrammaticalErrors-boolean-}
```
public void setShowGrammaticalErrors(boolean value)
```


Specifies whether to display grammar errors in this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShowSpellingErrors() {#getShowSpellingErrors--}
```
public boolean getShowSpellingErrors()
```


Specifies whether to display spelling errors in this document.

**Returns:**
boolean - The corresponding  boolean  value.
### setShowSpellingErrors(boolean value) {#setShowSpellingErrors-boolean-}
```
public void setShowSpellingErrors(boolean value)
```


Specifies whether to display spelling errors in this document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSpellingChecked() {#getSpellingChecked--}
```
public boolean getSpellingChecked()
```


Returns **true** if the document has been checked for spelling. To recheck the spelling in the document, set this property to **false**.

**Returns:**
boolean - **true** if the document has been checked for spelling.
### setSpellingChecked(boolean value) {#setSpellingChecked-boolean-}
```
public void setSpellingChecked(boolean value)
```


Returns **true** if the document has been checked for spelling. To recheck the spelling in the document, set this property to **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | **true** if the document has been checked for spelling. |

### getGrammarChecked() {#getGrammarChecked--}
```
public boolean getGrammarChecked()
```


Returns **true** if the document has been checked for grammar. To recheck the grammar in the document, set this property to **false**.

**Returns:**
boolean - **true** if the document has been checked for grammar.
### setGrammarChecked(boolean value) {#setGrammarChecked-boolean-}
```
public void setGrammarChecked(boolean value)
```


Returns **true** if the document has been checked for grammar. To recheck the grammar in the document, set this property to **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | **true** if the document has been checked for grammar. |

### getNodeType() {#getNodeType--}
```
public int getNodeType()
```


Returns **NodeType.Document**.

**Returns:**
int - **NodeType.Document**. The returned value is one of [NodeType](../../com.aspose.words/nodetype) constants.
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties--}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


Returns a collection that represents all the built-in document properties of the document.

**Returns:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) - A collection that represents all the built-in document properties of the document.
### getWebExtensionTaskPanes() {#getWebExtensionTaskPanes--}
```
public TaskPaneCollection getWebExtensionTaskPanes()
```


Returns a collection that represents a list of task pane add-ins.

**Returns:**
[TaskPaneCollection](../../com.aspose.words/taskpanecollection) - A collection that represents a list of task pane add-ins.
### getCustomDocumentProperties() {#getCustomDocumentProperties--}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


Returns a collection that represents all the custom document properties of the document.

**Returns:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) - A collection that represents all the custom document properties of the document.
### getMailMerge() {#getMailMerge--}
```
public MailMerge getMailMerge()
```


Returns a **MailMerge** object that represents the mail merge functionality for the document.

**Returns:**
[MailMerge](../../com.aspose.words/mailmerge) - A **MailMerge** object that represents the mail merge functionality for the document.
### getProtectionType() {#getProtectionType--}
```
public int getProtectionType()
```


Gets the currently active document protection type.

This property allows to retrieve the currently set document protection type. To change the document protection type use the **M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** and [unprotect()](../../com.aspose.words/document\#unprotect--) methods.

When a document is protected, the user can make only limited changes, such as adding annotations, making revisions, or completing a form.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--)

**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**

**Returns:**
int - The currently active document protection type. The returned value is one of [ProtectionType](../../com.aspose.words/protectiontype) constants.
### getSections() {#getSections--}
```
public SectionCollection getSections()
```


Returns a collection that represents all sections in the document.

**Returns:**
[SectionCollection](../../com.aspose.words/sectioncollection) - A collection that represents all sections in the document.
### getFirstSection() {#getFirstSection--}
```
public Section getFirstSection()
```


Gets the first section in the document. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section) - The first section in the document.
### getLastSection() {#getLastSection--}
```
public Section getLastSection()
```


Gets the last section in the document. Returns  null  if there are no sections.

**Returns:**
[Section](../../com.aspose.words/section) - The last section in the document.
### getViewOptions() {#getViewOptions--}
```
public ViewOptions getViewOptions()
```


Provides options to control how the document is displayed in Microsoft Word.

**Returns:**
[ViewOptions](../../com.aspose.words/viewoptions) - The corresponding [ViewOptions](../../com.aspose.words/viewoptions) value.
### getWriteProtection() {#getWriteProtection--}
```
public WriteProtection getWriteProtection()
```


Provides access to the document write protection options.

**Returns:**
[WriteProtection](../../com.aspose.words/writeprotection) - The corresponding [WriteProtection](../../com.aspose.words/writeprotection) value.
### getCompatibilityOptions() {#getCompatibilityOptions--}
```
public CompatibilityOptions getCompatibilityOptions()
```


Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word).

**Returns:**
[CompatibilityOptions](../../com.aspose.words/compatibilityoptions) - The corresponding [CompatibilityOptions](../../com.aspose.words/compatibilityoptions) value.
### getMailMergeSettings() {#getMailMergeSettings--}
```
public MailMergeSettings getMailMergeSettings()
```


Gets the object that contains all of the mail merge information for a document.

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

This object is never null.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings) - The object that contains all of the mail merge information for a document.
### setMailMergeSettings(MailMergeSettings value) {#setMailMergeSettings-com.aspose.words.MailMergeSettings-}
```
public void setMailMergeSettings(MailMergeSettings value)
```


Sets the object that contains all of the mail merge information for a document.

You can use this object to specify a mail merge data source for a document and this information (along with the available data fields) will appear in Microsoft Word when the user opens this document. Or you can use this object to query mail merge settings that the user has specified in Microsoft Word for this document.

This object is never null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [MailMergeSettings](../../com.aspose.words/mailmergesettings) | The object that contains all of the mail merge information for a document. |

### getHyphenationOptions() {#getHyphenationOptions--}
```
public HyphenationOptions getHyphenationOptions()
```


Provides access to document hyphenation options.

**Returns:**
[HyphenationOptions](../../com.aspose.words/hyphenationoptions) - The corresponding [HyphenationOptions](../../com.aspose.words/hyphenationoptions) value.
### hasRevisions() {#hasRevisions--}
```
public boolean hasRevisions()
```


Returns **true** if the document has any tracked changes. This property is a shortcut for comparing [RevisionCollection.getCount()](../../com.aspose.words/revisioncollection\#getCount--) to zero.

**Returns:**
boolean - **true** if the document has any tracked changes.
### hasMacros() {#hasMacros--}
```
public boolean hasMacros()
```


Returns **true** if the document has a VBA project (macros).

**Returns:**
boolean - **true** if the document has a VBA project (macros).
### getWatermark() {#getWatermark--}
```
public Watermark getWatermark()
```


Provides access to the document watermark.

**Returns:**
[Watermark](../../com.aspose.words/watermark) - The corresponding [Watermark](../../com.aspose.words/watermark) value.
### getVersionsCount() {#getVersionsCount--}
```
public int getVersionsCount()
```


Gets the number of document versions that was stored in the DOC document.

Versions in Microsoft Word are accessed via the File/Versions menu. Microsoft Word supports versions only for DOC files.

This property allows to detect if there were document versions stored in this document before it was opened in Aspose.Words. Aspose.Words provides no other support for document versions. If you save this document using Aspose.Words, the document will be saved without versions.

**Returns:**
int - The number of document versions that was stored in the DOC document.
### getDefaultTabStop() {#getDefaultTabStop--}
```
public double getDefaultTabStop()
```


Gets the interval (in points) between the default tab stops.

**Returns:**
double - The interval (in points) between the default tab stops.
### setDefaultTabStop(double value) {#setDefaultTabStop-double-}
```
public void setDefaultTabStop(double value)
```


Sets the interval (in points) between the default tab stops.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The interval (in points) between the default tab stops. |

### getTheme() {#getTheme--}
```
public Theme getTheme()
```


Gets the [getTheme()](../../com.aspose.words/document\#getTheme--) object for this document.

**Returns:**
[Theme](../../com.aspose.words/theme) - The [getTheme()](../../com.aspose.words/document\#getTheme--) object for this document.
### getCustomXmlParts() {#getCustomXmlParts--}
```
public CustomXmlPartCollection getCustomXmlParts()
```


Gets the collection of Custom XML Data Storage Parts.

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

**Returns:**
[CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) - The collection of Custom XML Data Storage Parts.
### setCustomXmlParts(CustomXmlPartCollection value) {#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-}
```
public void setCustomXmlParts(CustomXmlPartCollection value)
```


Sets the collection of Custom XML Data Storage Parts.

Aspose.Words loads and saves Custom XML Parts into OOXML and DOC documents only.

This property cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CustomXmlPartCollection](../../com.aspose.words/customxmlpartcollection) | The collection of Custom XML Data Storage Parts. |

### getPackageCustomParts() {#getPackageCustomParts--}
```
public CustomPartCollection getPackageCustomParts()
```


Gets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

**Returns:**
[CustomPartCollection](../../com.aspose.words/custompartcollection) - The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".
### setPackageCustomParts(CustomPartCollection value) {#setPackageCustomParts-com.aspose.words.CustomPartCollection-}
```
public void setPackageCustomParts(CustomPartCollection value)
```


Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships".

Do not confuse these custom parts with Custom XML Data. If you need to access Custom XML parts, use the [getCustomXmlParts()](../../com.aspose.words/document\#getCustomXmlParts--) / [setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection-) property.

This collection contains OOXML parts whose parent is the OOXML package and they targets are of an "unknown relationship". For more information see [CustomPart](../../com.aspose.words/custompart).

Aspose.Words loads and saves custom parts into OOXML documents only.

This property cannot be  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [CustomPartCollection](../../com.aspose.words/custompartcollection) | The collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |

### getVariables() {#getVariables--}
```
public VariableCollection getVariables()
```


Returns the collection of variables added to a document or template.

**Returns:**
[VariableCollection](../../com.aspose.words/variablecollection) - The collection of variables added to a document or template.
### getGlossaryDocument() {#getGlossaryDocument--}
```
public GlossaryDocument getGlossaryDocument()
```


Gets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument) object and assigning to this property.

**Returns:**
[GlossaryDocument](../../com.aspose.words/glossarydocument) - The glossary document within this document or template.
### setGlossaryDocument(GlossaryDocument value) {#setGlossaryDocument-com.aspose.words.GlossaryDocument-}
```
public void setGlossaryDocument(GlossaryDocument value)
```


Sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document.

This property returns  null  if the document does not have a glossary document.

You can add a glossary document to a document by creating a [GlossaryDocument](../../com.aspose.words/glossarydocument) object and assigning to this property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [GlossaryDocument](../../com.aspose.words/glossarydocument) | The glossary document within this document or template. |

### getOriginalFileName() {#getOriginalFileName--}
```
public String getOriginalFileName()
```


Gets the original file name of the document.

Returns null if the document was loaded from a stream or created blank.

**Returns:**
java.lang.String - The original file name of the document.
### getOriginalLoadFormat() {#getOriginalLoadFormat--}
```
public int getOriginalLoadFormat()
```


Gets the format of the original document that was loaded into this object.

If you created a new blank document, returns the [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) value.

**Returns:**
int - The format of the original document that was loaded into this object. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat) constants.
### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents.

If you created a new blank document or load non OOXML document returns the [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006) value.

**Returns:**
int - The OOXML compliance version determined from the loaded document content. The returned value is one of [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) constants.
### getDigitalSignatures() {#getDigitalSignatures--}
```
public DigitalSignatureCollection getDigitalSignatures()
```


Gets the collection of digital signatures for this document and their validation results.

This collection contains digital signatures that were loaded from the original document. These digital signatures will not be saved when you save this [Document](../../com.aspose.words/document) object into a file or stream because saving or converting will produce a document that is different from the original and the original digital signatures will no longer be valid.

This collection is never null. If the document is not signed, it will contain zero elements.

**Returns:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - The collection of digital signatures for this document and their validation results.
### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


Gets document font settings.

This property allows to specify font settings per document. If set to null, default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) will be used.

The default value is null.

**Returns:**
[FontSettings](../../com.aspose.words/fontsettings) - Document font settings.
### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


Sets document font settings.

This property allows to specify font settings per document. If set to null, default static font settings [FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) will be used.

The default value is null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) | Document font settings. |

### getFrameset() {#getFrameset--}
```
public Frameset getFrameset()
```


Returns a [getFrameset()](../../com.aspose.words/document\#getFrameset--) instance if this document represents a frames page. If the document is not framed, the property has the **null** value.

**Returns:**
[Frameset](../../com.aspose.words/frameset) - A [getFrameset()](../../com.aspose.words/document\#getFrameset--) instance if this document represents a frames page.
### deepClone() {#deepClone--}
```
public Document deepClone()
```


Performs a deep copy of the [Document](../../com.aspose.words/document).

**Returns:**
[Document](../../com.aspose.words/document) - The cloned document.
### accept(DocumentVisitor visitor) {#accept-com.aspose.words.DocumentVisitor-}
```
public boolean accept(DocumentVisitor visitor)
```


Accepts a visitor.

Enumerates over this node and all of its children. Each node calls a corresponding method on DocumentVisitor.

For more info see the Visitor design pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitor | [DocumentVisitor](../../com.aspose.words/documentvisitor) | The visitor that will visit the nodes. |

**Returns:**
boolean - True if all nodes were visited; false if DocumentVisitor stopped the operation before visiting all nodes. Calls DocumentVisitor.VisitDocumentStart, then calls Accept for all child nodes of the document and calls DocumentVisitor.VisitDocumentEnd at the end.
### appendDocument(Document srcDoc, int importFormatMode) {#appendDocument-com.aspose.words.Document-int-}
```
public void appendDocument(Document srcDoc, int importFormatMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |

### appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#appendDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-}
```
public void appendDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

### save(String fileName) {#save-java.lang.String-}
```
public SaveOutputParameters save(String fileName)
```


Saves the document.  Saves the document to a file. Automatically determines the save format from the extension.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters) - Additional information that you can optionally use.
### save(String fileName, int saveFormat) {#save-java.lang.String-int-}
```
public SaveOutputParameters save(String fileName, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters)
### save(String fileName, SaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SaveOptions-}
```
public SaveOutputParameters save(String fileName, SaveOptions saveOptions)
```


Saves the document to a file using the specified save options.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) | Specifies the options that control how the document is saved. Can be null. |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters) - Additional information that you can optionally use.
### save(OutputStream stream, int saveFormat) {#save-java.io.OutputStream-int-}
```
public SaveOutputParameters save(OutputStream stream, int saveFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters)
### save(OutputStream stream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions-}
```
public SaveOutputParameters save(OutputStream stream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions) |  |

**Returns:**
[SaveOutputParameters](../../com.aspose.words/saveoutputparameters)
### ensureMinimum() {#ensureMinimum--}
```
public void ensureMinimum()
```


If the document contains no sections, creates one section with one paragraph.

### acceptAllRevisions() {#acceptAllRevisions--}
```
public void acceptAllRevisions()
```


Accepts all tracked changes in the document. This method is a shortcut for [RevisionCollection.acceptAll()](../../com.aspose.words/revisioncollection\#acceptAll--).

### protect(int type) {#protect-int-}
```
public void protect(int type)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | int |  |

### protect(int type, String password) {#protect-int-java.lang.String-}
```
public void protect(int type, String password)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | int |  |
| password | java.lang.String |  |

### unprotect() {#unprotect--}
```
public void unprotect()
```


Removes protection from the document.  Removes protection from the document regardless of the password.

This method unprotects the document even if it has a protection password.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

### unprotect(String password) {#unprotect-java.lang.String-}
```
public boolean unprotect(String password)
```


Removes protection from the document if a correct password is specified.

This method unprotects the document only if a correct password is specified.

Note that document protection is different from write protection. Write protection is specified using the [getWriteProtection()](../../com.aspose.words/document\#getWriteProtection--).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| password | java.lang.String | The password to unprotect the document with. |

**Returns:**
boolean - True if a correct password was specified and the document was unprotected.
### updateWordCount() {#updateWordCount--}
```
public void updateWordCount()
```


Updates word count properties of the document.

**UpdateWordCount** recalculates and updates Characters, Words and Paragraphs properties in the [getBuiltInDocumentProperties()](../../com.aspose.words/document\#getBuiltInDocumentProperties--) collection of the **Document**.

Note that **UpdateWordCount** does not update number of lines and pages properties. Use the [updateWordCount()](../../com.aspose.words/document\#updateWordCount--) overload and pass True value as a parameter to do that.

When you use an evaluation version, the evaluation watermark will also be included in the word count.

### updateWordCount(boolean updateLinesCount) {#updateWordCount-boolean-}
```
public void updateWordCount(boolean updateLinesCount)
```


Updates word count properties of the document, optionally updates [BuiltInDocumentProperties.getLines()](../../com.aspose.words/builtindocumentproperties\#getLines--) / [BuiltInDocumentProperties.setLines(int)](../../com.aspose.words/builtindocumentproperties\#setLines-int-) property. This method will rebuild page layout of the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| updateLinesCount | boolean | True if number of lines in the document shall be calculated. |

### updateTableLayout() {#updateTableLayout--}
```
public void updateTableLayout()
```


Implements an earlier approach to table column widths re-calculation that has known issues. The method is deprecated and it will be removed in a few releases.

### updateListLabels() {#updateListLabels--}
```
public void updateListLabels()
```


Updates list labels for all list items in the document.

This method updates list label properties such as [ListLabel.getLabelValue()](../../com.aspose.words/listlabel\#getLabelValue--) and [ListLabel.getLabelString()](../../com.aspose.words/listlabel\#getLabelString--) for each [Paragraph.getListLabel()](../../com.aspose.words/paragraph\#getListLabel--) object in the document.

Also, this method is sometimes implicitly called when updating fields in the document. This is required because some fields that may reference list numbers (such as TOC or REF) need them be up-to-date.

### removeMacros() {#removeMacros--}
```
public void removeMacros()
```


Removes all macros (the VBA project) as well as toolbars and command customizations from the document.

By removing all macros from a document you can ensure the document contains no macro viruses.

### updateFields() {#updateFields--}
```
public void updateFields()
```


Updates the values of fields in the whole document.

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

Use the [normalizeFieldTypes()](../../com.aspose.words/document\#normalizeFieldTypes--) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.updateFields()](../../com.aspose.words/range\#updateFields--).

### unlinkFields() {#unlinkFields--}
```
public void unlinkFields()
```


Unlinks fields in the whole document.

Replaces all the fields in the whole document with their most recent results.

To unlink fields in a specific part of the document use [Range.unlinkFields()](../../com.aspose.words/range\#unlinkFields--).

### normalizeFieldTypes() {#normalizeFieldTypes--}
```
public void normalizeFieldTypes()
```


Changes field type values [FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) of [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) in the whole document so that they correspond to the field types contained in the field codes.

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [Range.normalizeFieldTypes()](../../com.aspose.words/range\#normalizeFieldTypes--).

### joinRunsWithSameFormatting() {#joinRunsWithSameFormatting--}
```
public int joinRunsWithSameFormatting()
```


Joins runs with same formatting in all paragraphs of the document.

This is an optimization method. Some documents contain adjacent runs with same formatting. Usually this occurs if a document was intensively edited manually. You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../com.aspose.words/paragraph) node in the document for adjacent [Run](../../com.aspose.words/run) nodes having identical properties. It ignores unique identifiers used to track editing sessions of run creation and modification. First run in every joining sequence accumulates all text. Remaining runs are deleted from the document.

**Returns:**
int - Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.
### expandTableStylesToDirectFormatting() {#expandTableStylesToDirectFormatting--}
```
public void expandTableStylesToDirectFormatting()
```


Converts formatting specified in table styles into direct formatting on tables in the document.

This method exists because this version of Aspose.Words provides only limited support for table styles (see below). This method might be useful when you load a DOCX or WordprocessingML document that contains tables formatted with table styles and you need to query formatting of tables, cells, paragraphs or text.

This version of Aspose.Words provides limited support for table styles as follows:

 *  Table styles defined in DOCX or WordprocessingML documents are preserved as table styles when saving the document as DOCX or WordprocessingML.
 *  Table styles defined in DOCX or WordprocessingML documents are automatically converted to direct formatting on tables when saving the document into any other format, rendering or printing.
 *  Table styles defined in DOC documents are preserved as table styles when saving the document as DOC only.

### cleanup() {#cleanup--}
```
public void cleanup()
```


Cleans unused styles and lists from the document.

### cleanup(CleanupOptions options) {#cleanup-com.aspose.words.CleanupOptions-}
```
public void cleanup(CleanupOptions options)
```


Cleans unused styles and lists from the document depending on given [CleanupOptions](../../com.aspose.words/cleanupoptions).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| options | [CleanupOptions](../../com.aspose.words/cleanupoptions) |  |

### removeExternalSchemaReferences() {#removeExternalSchemaReferences--}
```
public void removeExternalSchemaReferences()
```


Removes external XML schema references from this document.

### startTrackRevisions(String author, Date dateTime) {#startTrackRevisions-java.lang.String-java.util.Date-}
```
public void startTrackRevisions(String author, Date dateTime)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-) option and does not use its value for the purposes of revision tracking.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. |

### startTrackRevisions(String author) {#startTrackRevisions-java.lang.String-}
```
public void startTrackRevisions(String author)
```


Starts automatically marking all further changes you make to the document programmatically as revision changes.

If you call this method and then make some changes to the document programmatically, save the document and later open the document in MS Word you will see these changes as revisions.

Currently Aspose.Words supports tracking of node insertions and deletions only. Formatting changes are not recorded as revisions.

Automatic tracking of changes is supported both when modifying this document through node manipulations as well as when using [DocumentBuilder](../../com.aspose.words/documentbuilder)

This method does not change the [getTrackRevisions()](../../com.aspose.words/document\#getTrackRevisions--) / [setTrackRevisions(boolean)](../../com.aspose.words/document\#setTrackRevisions-boolean-) option and does not use its value for the purposes of revision tracking.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| author | java.lang.String | Initials of the author to use for revisions. |

### stopTrackRevisions() {#stopTrackRevisions--}
```
public void stopTrackRevisions()
```


Stops automatic marking of document changes as revisions.

### compare(Document document, String author, Date dateTime) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-}
```
public void compare(Document document, String author, Date dateTime)
```


Compares this document with another document producing changes as number of edit and format revisions [Revision](../../com.aspose.words/revision).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | Document to compare. |
| author | java.lang.String | Initials of the author to use for revisions. |
| dateTime | java.util.Date | The date and time to use for revisions. The following document nodes are not compared at the moment:

 *  [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)
 *  Item3

Documents must not have revisions before comparison. |

### compare(Document document, String author, Date dateTime, CompareOptions options) {#compare-com.aspose.words.Document-java.lang.String-java.util.Date-com.aspose.words.CompareOptions-}
```
public void compare(Document document, String author, Date dateTime, CompareOptions options)
```


Compares this document with another document producing changes as a number of edit and format revisions [Revision](../../com.aspose.words/revision). Allows to specify comparison options using [CompareOptions](../../com.aspose.words/compareoptions).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) |  |
| author | java.lang.String |  |
| dateTime | java.util.Date |  |
| options | [CompareOptions](../../com.aspose.words/compareoptions) |  |

### copyStylesFromTemplate(String template) {#copyStylesFromTemplate-java.lang.String-}
```
public void copyStylesFromTemplate(String template)
```


Copies styles from the specified template to a document. When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| template | java.lang.String |  |

### copyStylesFromTemplate(Document template) {#copyStylesFromTemplate-com.aspose.words.Document-}
```
public void copyStylesFromTemplate(Document template)
```


Copies styles from the specified template to a document. When styles are copied from a template to a document, like-named styles in the document are redefined to match the style descriptions in the template. Unique styles from the template are copied to the document. Unique styles in the document remain intact.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| template | [Document](../../com.aspose.words/document) |  |

### getPageCount() {#getPageCount--}
```
public int getPageCount()
```


Gets the number of pages in the document as calculated by the most recent page layout operation.

**Returns:**
int - The number of pages in the document as calculated by the most recent page layout operation.
### getRevisions() {#getRevisions--}
```
public RevisionCollection getRevisions()
```


Gets a collection of revisions (tracked changes) that exist in this document.

The returned collection is a "live" collection, which means if you remove parts of a document that contain revisions, the deleted revisions will automatically disappear from this collection.

**Returns:**
[RevisionCollection](../../com.aspose.words/revisioncollection) - A collection of revisions (tracked changes) that exist in this document.
### getLayoutOptions() {#getLayoutOptions--}
```
public LayoutOptions getLayoutOptions()
```


Gets a **LayoutOptions** object that represents options to control the layout process of this document.

**Returns:**
[LayoutOptions](../../com.aspose.words/layoutoptions) - A **LayoutOptions** object that represents options to control the layout process of this document.
### getRevisionsView() {#getRevisionsView--}
```
public int getRevisionsView()
```


Gets a value indicating whether to work with the original or revised version of a document. The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**Returns:**
int - A value indicating whether to work with the original or revised version of a document. The returned value is one of [RevisionsView](../../com.aspose.words/revisionsview) constants.
### setRevisionsView(int value) {#setRevisionsView-int-}
```
public void setRevisionsView(int value)
```


Sets a value indicating whether to work with the original or revised version of a document. The default value is  **[RevisionsView.ORIGINAL](../../com.aspose.words/revisionsview\#ORIGINAL)** .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A value indicating whether to work with the original or revised version of a document. The value must be one of [RevisionsView](../../com.aspose.words/revisionsview) constants. |

### updatePageLayout() {#updatePageLayout--}
```
public void updatePageLayout()
```


Rebuilds the page layout of the document.

This method formats a document into pages and updates the page number related fields in the document such as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it. However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not update the page layout automatically. In this case you should call [updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) before rendering again.

### renderToScale(int pageIndex, Graphics2D graphics, float x, float y, float scale) {#renderToScale-int-java.awt.Graphics2D-float-float-float-}
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
### renderToSize(int pageIndex, Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-int-java.awt.Graphics2D-float-float-float-float-}
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
### add(Shape watermark) {#add-com.aspose.words.Shape-}
```
public void add(Shape watermark)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| watermark | [Shape](../../com.aspose.words/shape) |  |

### get() {#get--}
```
public Shape get()
```




**Returns:**
[Shape](../../com.aspose.words/shape)
### remove() {#remove--}
```
public void remove()
```


Removes itself from the parent.

### getPageInfo(int pageIndex) {#getPageInfo-int-}
```
public PageInfo getPageInfo(int pageIndex)
```


Gets the page size, orientation and other information about a page that might be useful for printing or rendering.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pageIndex | int | The 0-based page index. |

**Returns:**
[PageInfo](../../com.aspose.words/pageinfo)
### print() {#print--}
```
public void print()
```


Prints the document without bringing up any user interface forms.  Prints the whole document to the default printer.

### print(String printerName) {#print-java.lang.String-}
```
public void print(String printerName)
```


Print the whole document to the specified printer, using the standard (no User Interface) print controller.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| printerName | java.lang.String | The name of the printer. |

### print(AttributeSet printerSettings) {#print-javax.print.attribute.AttributeSet-}
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

### print(AttributeSet printerSettings, String documentName) {#print-javax.print.attribute.AttributeSet-java.lang.String-}
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

### updateThumbnail(ThumbnailGeneratingOptions options) {#updateThumbnail-com.aspose.words.ThumbnailGeneratingOptions-}
```
public void updateThumbnail(ThumbnailGeneratingOptions options)
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) of the document according to the specified options. The [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) allows you to specify the source of thumbnail, size and other options. If attempt to generate thumbnail fails, doesn't change one.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| options | [ThumbnailGeneratingOptions](../../com.aspose.words/thumbnailgeneratingoptions) | The generating options to use. |

### updateThumbnail() {#updateThumbnail--}
```
public void updateThumbnail()
```


Updates [BuiltInDocumentProperties.getThumbnail()](../../com.aspose.words/builtindocumentproperties\#getThumbnail--) / [BuiltInDocumentProperties.setThumbnail(byte[])](../../com.aspose.words/builtindocumentproperties\#setThumbnail-byte---) of the document using default options.

### extractPages(int index, int count) {#extractPages-int-int-}
```
public Document extractPages(int index, int count)
```


Returns the [Document](../../com.aspose.words/document) object representing specified range of pages. The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' \\u2013 the numbering, headers/footers and cross tables layout will be preserved. But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort. Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document. Any feedback would be greatly appreciated.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the first page to extract. |
| count | int | Number of pages to be extracted. |

**Returns:**
[Document](../../com.aspose.words/document)
### getFootnoteOptions() {#getFootnoteOptions--}
```
public FootnoteOptions getFootnoteOptions()
```


Provides options that control numbering and positioning of footnotes in this document.

**Returns:**
[FootnoteOptions](../../com.aspose.words/footnoteoptions) - The corresponding [FootnoteOptions](../../com.aspose.words/footnoteoptions) value.
### getEndnoteOptions() {#getEndnoteOptions--}
```
public EndnoteOptions getEndnoteOptions()
```


Provides options that control numbering and positioning of endnotes in this document.

**Returns:**
[EndnoteOptions](../../com.aspose.words/endnoteoptions) - The corresponding [EndnoteOptions](../../com.aspose.words/endnoteoptions) value.
### getDirectSectionAttr(int key) {#getDirectSectionAttr-int-}
```
public Object getDirectSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedSectionAttr(int key) {#fetchInheritedSectionAttr-int-}
```
public Object fetchInheritedSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchSectionAttr(int key) {#fetchSectionAttr-int-}
```
public Object fetchSectionAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setSectionAttr(int key, Object value) {#setSectionAttr-int-java.lang.Object-}
```
public void setSectionAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### clearSectionAttrs() {#clearSectionAttrs--}
```
public void clearSectionAttrs()
```




### getFieldOptions() {#getFieldOptions--}
```
public FieldOptions getFieldOptions()
```


Gets a **FieldOptions** object that represents options to control field handling in the document.

**Returns:**
[FieldOptions](../../com.aspose.words/fieldoptions) - A **FieldOptions** object that represents options to control field handling in the document.
### getRemovePersonalInformation() {#getRemovePersonalInformation--}
```
public boolean getRemovePersonalInformation()
```


Gets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

**Returns:**
boolean - A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.
### setRemovePersonalInformation(boolean value) {#setRemovePersonalInformation-boolean-}
```
public void setRemovePersonalInformation(boolean value)
```


Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |

### getVbaProject() {#getVbaProject--}
```
public VbaProject getVbaProject()
```


Gets a [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**Returns:**
[VbaProject](../../com.aspose.words/vbaproject) - A [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).
### setVbaProject(VbaProject value) {#setVbaProject-com.aspose.words.VbaProject-}
```
public void setVbaProject(VbaProject value)
```


Sets a [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [VbaProject](../../com.aspose.words/vbaproject) | A [getVbaProject()](../../com.aspose.words/document\#getVbaProject--) / [setVbaProject(com.aspose.words.VbaProject)](../../com.aspose.words/document\#setVbaProject-com.aspose.words.VbaProject-). |

