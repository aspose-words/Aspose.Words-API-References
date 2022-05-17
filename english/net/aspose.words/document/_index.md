---
title: Document
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 420
url: /net/aspose.words/document/
---
## Document class

Represents a Word document.

```csharp
public class Document : DocumentBase
```

## Constructors

| Name | Description |
| --- | --- |
| [Document](document)() | Creates a blank Word document. |
| [Document](document)(Stream) | Opens an existing document from a stream. Automatically detects the file format. |
| [Document](document)(string) | Opens an existing document from a file. Automatically detects the file format. |
| [Document](document)(Stream, LoadOptions) | Opens an existing document from a stream. Allows to specify additional options such as an encryption password. |
| [Document](document)(string, LoadOptions) | Opens an existing document from a file. Allows to specify additional options such as an encryption password. |

## Properties

| Name | Description |
| --- | --- |
| [AttachedTemplate](attachedtemplate) { get; set; } | Gets or sets the full path of the template attached to the document. |
| [AutomaticallyUpdateStyles](automaticallyupdatestyles) { get; set; } | Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [BuiltInDocumentProperties](builtindocumentproperties) { get; } | Returns a collection that represents all the built-in document properties of the document. |
| [CompatibilityOptions](compatibilityoptions) { get; } | Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word). |
| [Compliance](compliance) { get; } | Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents. |
| [CustomDocumentProperties](customdocumentproperties) { get; } | Returns a collection that represents all the custom document properties of the document. |
| [CustomXmlParts](customxmlparts) { get; set; } | Gets or sets the collection of Custom XML Data Storage Parts. |
| [DefaultTabStop](defaulttabstop) { get; set; } | Gets or sets the interval (in points) between the default tab stops. |
| [DigitalSignatures](digitalsignatures) { get; } | Gets the collection of digital signatures for this document and their validation results. |
| [EndnoteOptions](endnoteoptions) { get; } | Provides options that control numbering and positioning of endnotes in this document. |
| [FieldOptions](fieldoptions) { get; } | Gets a **FieldOptions** object that represents options to control field handling in the document. |
| [FirstSection](firstsection) { get; } | Gets the first section in the document. |
| [FontSettings](fontsettings) { get; set; } | Gets or sets document font settings. |
| [FootnoteOptions](footnoteoptions) { get; } | Provides options that control numbering and positioning of footnotes in this document. |
| [Frameset](frameset) { get; } | Returns a [`Frameset`](./frameset) instance if this document represents a frames page. |
| [GlossaryDocument](glossarydocument) { get; set; } | Gets or sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document. |
| [GrammarChecked](grammarchecked) { get; set; } | Returns **true** if the document has been checked for grammar. |
| [HasMacros](hasmacros) { get; } | Returns **true** if the document has a VBA project (macros). |
| [HasRevisions](hasrevisions) { get; } | Returns **true** if the document has any tracked changes. |
| [HyphenationOptions](hyphenationoptions) { get; } | Provides access to document hyphenation options. |
| [LastSection](lastsection) { get; } | Gets the last section in the document. |
| [LayoutOptions](layoutoptions) { get; } | Gets a **LayoutOptions** object that represents options to control the layout process of this document. |
| [MailMerge](mailmerge) { get; } | Returns a **MailMerge** object that represents the mail merge functionality for the document. |
| [MailMergeSettings](mailmergesettings) { get; set; } | Gets or sets the object that contains all of the mail merge information for a document. |
| override [NodeType](nodetype) { get; } | Returns **NodeType.Document**. |
| [OriginalFileName](originalfilename) { get; } | Gets the original file name of the document. |
| [OriginalLoadFormat](originalloadformat) { get; } | Gets the format of the original document that was loaded into this object. |
| [PackageCustomParts](packagecustomparts) { get; set; } | Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [PageCount](pagecount) { get; } | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [ProtectionType](protectiontype) { get; } | Gets the currently active document protection type. |
| [RemovePersonalInformation](removepersonalinformation) { get; set; } | Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [Revisions](revisions) { get; } | Gets a collection of revisions (tracked changes) that exist in this document. |
| [RevisionsView](revisionsview) { get; set; } | Gets or sets a value indicating whether to work with the original or revised version of a document. |
| [Sections](sections) { get; } | Returns a collection that represents all sections in the document. |
| [ShadeFormData](shadeformdata) { get; set; } | Specifies whether to turn on the gray shading on form fields. |
| [ShowGrammaticalErrors](showgrammaticalerrors) { get; set; } | Specifies whether to display grammar errors in this document. |
| [ShowSpellingErrors](showspellingerrors) { get; set; } | Specifies whether to display spelling errors in this document. |
| [SpellingChecked](spellingchecked) { get; set; } | Returns **true** if the document has been checked for spelling. |
| [Theme](theme) { get; } | Gets the [`Theme`](./theme) object for this document. |
| [TrackRevisions](trackrevisions) { get; set; } | **True** if changes are tracked when this document is edited in Microsoft Word. |
| [Variables](variables) { get; } | Returns the collection of variables added to a document or template. |
| [VbaProject](vbaproject) { get; set; } | Gets or sets a [`VbaProject`](./vbaproject). |
| [VersionsCount](versionscount) { get; } | Gets the number of document versions that was stored in the DOC document. |
| [ViewOptions](viewoptions) { get; } | Provides options to control how the document is displayed in Microsoft Word. |
| [Watermark](watermark) { get; } | Provides access to the document watermark. |
| [WebExtensionTaskPanes](webextensiontaskpanes) { get; } | Returns a collection that represents a list of task pane add-ins. |
| [WriteProtection](writeprotection) { get; } | Provides access to the document write protection options. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](accept)(DocumentVisitor) | Accepts a visitor. |
| [AcceptAllRevisions](acceptallrevisions)() | Accepts all tracked changes in the document. |
| [AppendDocument](appenddocument)(Document, ImportFormatMode) | Appends the specified document to the end of this document. |
| [AppendDocument](appenddocument)(Document, ImportFormatMode, ImportFormatOptions) | Appends the specified document to the end of this document. |
| [Cleanup](cleanup)() | Cleans unused styles and lists from the document. |
| [Cleanup](cleanup)(CleanupOptions) | Cleans unused styles and lists from the document depending on given [`CleanupOptions`](../cleanupoptions). |
| [Clone](clone)() | Performs a deep copy of the [`Document`](../document). |
| [Compare](compare)(Document, string, DateTime) | Compares this document with another document producing changes as number of edit and format revisions [`Revision`](../revision). |
| [Compare](compare)(Document, string, DateTime, CompareOptions) | Compares this document with another document producing changes as a number of edit and format revisions [`Revision`](../revision). Allows to specify comparison options using [`CompareOptions`](../../aspose.words.comparing/compareoptions). |
| [CopyStylesFromTemplate](copystylesfromtemplate)(Document) | Copies styles from the specified template to a document. |
| [CopyStylesFromTemplate](copystylesfromtemplate)(string) | Copies styles from the specified template to a document. |
| [EnsureMinimum](ensureminimum)() | If the document contains no sections, creates one section with one paragraph. |
| [ExpandTableStylesToDirectFormatting](expandtablestylestodirectformatting)() | Converts formatting specified in table styles into direct formatting on tables in the document. |
| [ExtractPages](extractpages)(int, int) | Returns the [`Document`](../document) object representing specified range of pages. |
| [GetPageInfo](getpageinfo)(int) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
| [JoinRunsWithSameFormatting](joinrunswithsameformatting)() | Joins runs with same formatting in all paragraphs of the document. |
| [NormalizeFieldTypes](normalizefieldtypes)() | Changes field type values [`FieldType`](../../aspose.words.fields/fieldchar/fieldtype) of [`FieldStart`](../../aspose.words.fields/fieldstart), [`FieldSeparator`](../../aspose.words.fields/fieldseparator), [`FieldEnd`](../../aspose.words.fields/fieldend) in the whole document so that they correspond to the field types contained in the field codes. |
| [Print](print)() | Prints the whole document to the default printer. |
| [Print](print)(PrinterSettings) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller. |
| [Print](print)(string) | Print the whole document to the specified printer, using the standard (no User Interface) print controller. |
| [Print](print)(PrinterSettings, string) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name. |
| [Protect](protect)(ProtectionType) | Protects the document from changes without changing the existing password or assigns a random password. |
| [Protect](protect)(ProtectionType, string) | Protects the document from changes and optionally sets a protection password. |
| [RemoveExternalSchemaReferences](removeexternalschemareferences)() | Removes external XML schema references from this document. |
| [RemoveMacros](removemacros)() | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
| [RenderToScale](rendertoscale)(int, Graphics, float, float, float) | Renders a document page into a Graphics object to a specified scale. |
| [RenderToSize](rendertosize)(int, Graphics, float, float, float, float) | Renders a document page into a Graphics object to a specified size. |
| [Save](save)(string) | Saves the document to a file. Automatically determines the save format from the extension. |
| [Save](save)(Stream, SaveFormat) | Saves the document to a stream using the specified format. |
| [Save](save)(Stream, SaveOptions) | Saves the document to a stream using the specified save options. |
| [Save](save)(string, SaveFormat) | Saves the document to a file in the specified format. |
| [Save](save)(string, SaveOptions) | Saves the document to a file using the specified save options. |
| [Save](save)(HttpResponse, string, ContentDisposition, SaveOptions) | Sends the document to the client browser. |
| [StartTrackRevisions](starttrackrevisions)(string) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [StartTrackRevisions](starttrackrevisions)(string, DateTime) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [StopTrackRevisions](stoptrackrevisions)() | Stops automatic marking of document changes as revisions. |
| [UnlinkFields](unlinkfields)() | Unlinks fields in the whole document. |
| [Unprotect](unprotect)() | Removes protection from the document regardless of the password. |
| [Unprotect](unprotect)(string) | Removes protection from the document if a correct password is specified. |
| [UpdateFields](updatefields)() | Updates the values of fields in the whole document. |
| [UpdateListLabels](updatelistlabels)() | Updates list labels for all list items in the document. |
| [UpdatePageLayout](updatepagelayout)() | Rebuilds the page layout of the document. |
| [UpdateThumbnail](updatethumbnail)() | Updates [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) of the document using default options. |
| [UpdateThumbnail](updatethumbnail)(ThumbnailGeneratingOptions) | Updates [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail) of the document according to the specified options. |
| [UpdateWordCount](updatewordcount)() | Updates word count properties of the document. |
| [UpdateWordCount](updatewordcount)(bool) | Updates word count properties of the document, optionally updates [`Lines`](../../aspose.words.properties/builtindocumentproperties/lines) property. |

### Remarks

The **Document** is a central object in the Aspose.Words library.

To load an existing document in any of the [`LoadFormat`](../loadformat) formats, pass a file name or a stream into one of the **Document** constructors. To create a blank document, call the constructor without parameters.

Use one of the Save method overloads to save the document in any of the [`SaveFormat`](../saveformat) formats.

To draw document pages directly onto a **Graphics** object use [`RenderToScale`](./rendertoscale) or [`RenderToSize`](./rendertosize) method.

To print the document, use one of the [`Print`](./print) methods.

[`MailMerge`](./mailmerge) is the Aspose.Words's reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a DataSet, DataTable, DataView, IDataReader or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

**Document** stores document-wide information such as [`Styles`](../documentbase/styles), [`BuiltInDocumentProperties`](./builtindocumentproperties), [`CustomDocumentProperties`](./customdocumentproperties), lists and macros. Most of these objects are accessible via the corresponding properties of the **Document**.

The **Document** is a root node of a tree that contains all other nodes of the document. The tree is a Composite design pattern and in many ways similar to XmlDocument. The content of the document can be manipulated freely programmatically:

* The nodes of the document can be accessed via typed collections, for example [`Sections`](./sections), [`ParagraphCollection`](../paragraphcollection) etc.
* The nodes of the document can be selected by their node type using [`GetChildNodes`](../compositenode/getchildnodes) or using an XPath query with [`SelectNodes`](../compositenode/selectnodes) or [`SelectSingleNode`](../compositenode/selectsinglenode).
* Content nodes can be added or removed from anywhere in the document using [`InsertBefore`](../compositenode/insertbefore), [`InsertAfter`](../compositenode/insertafter), [`RemoveChild`](../compositenode/removechild) and other methods provided by the base class [`CompositeNode`](../compositenode).
* The formatting attributes of each node can be changed via the properties of that node.

Consider using [`DocumentBuilder`](../documentbuilder) that simplifies the task of programmatically creating or populating the document tree.

The **Document** can contain only [`Section`](../section) objects.

In Microsoft Word, a valid document needs to have at least one section.

### See Also

* class [DocumentBase](../documentbase)
* namespace [Aspose.Words](../../aspose.words)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
