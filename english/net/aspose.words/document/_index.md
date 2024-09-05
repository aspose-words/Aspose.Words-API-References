---
title: Document Class
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: Aspose.Words.Document class. Represents a Word document in C#.
type: docs
weight: 530
url: /net/aspose.words/document/
---
## Document class

Represents a Word document.

To learn more, visit the [Working with Document](https://docs.aspose.com/words/net/working-with-document/) documentation article.

```csharp
public class Document : DocumentBase
```

## Constructors

| Name | Description |
| --- | --- |
| [Document](document/#constructor)() | Creates a blank Word document. |
| [Document](document/#constructor_1)(*Stream*) | Opens an existing document from a stream. Automatically detects the file format. |
| [Document](document/#constructor_3)(*string*) | Opens an existing document from a file. Automatically detects the file format. |
| [Document](document/#constructor_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Opens an existing document from a stream. Allows to specify additional options such as an encryption password. |
| [Document](document/#constructor_4)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Opens an existing document from a file. Allows to specify additional options such as an encryption password. |

## Properties

| Name | Description |
| --- | --- |
| [AttachedTemplate](../../aspose.words/document/attachedtemplate/) { get; set; } | Gets or sets the full path of the template attached to the document. |
| [AutomaticallyUpdateStyles](../../aspose.words/document/automaticallyupdatestyles/) { get; set; } | Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Gets or sets the background shape of the document. Can be `null`. |
| [Bibliography](../../aspose.words/document/bibliography/) { get; } | Gets the [`Bibliography`](./bibliography/) object that represents the list of sources available in the document. |
| [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/) { get; } | Returns a collection that represents all the built-in document properties of the document. |
| [CompatibilityOptions](../../aspose.words/document/compatibilityoptions/) { get; } | Provides access to document compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Word). |
| [Compliance](../../aspose.words/document/compliance/) { get; } | Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Gets the number of immediate children of this node. |
| [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/) { get; } | Returns a collection that represents all the custom document properties of the document. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifies custom node identifier. |
| [CustomXmlParts](../../aspose.words/document/customxmlparts/) { get; set; } | Gets or sets the collection of Custom XML Data Storage Parts. |
| [DefaultTabStop](../../aspose.words/document/defaulttabstop/) { get; set; } | Gets or sets the interval (in points) between the default tab stops. |
| [DigitalSignatures](../../aspose.words/document/digitalsignatures/) { get; } | Gets the collection of digital signatures for this document and their validation results. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Gets this instance. |
| [EndnoteOptions](../../aspose.words/document/endnoteoptions/) { get; } | Provides options that control numbering and positioning of endnotes in this document. |
| [FieldOptions](../../aspose.words/document/fieldoptions/) { get; } | Gets a [`FieldOptions`](../../aspose.words.fields/fieldoptions/) object that represents options to control field handling in the document. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Gets the first child of the node. |
| [FirstSection](../../aspose.words/document/firstsection/) { get; } | Gets the first section in the document. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Provides access to properties of fonts used in this document. |
| [FontSettings](../../aspose.words/document/fontsettings/) { get; set; } | Gets or sets document font settings. |
| [FootnoteOptions](../../aspose.words/document/footnoteoptions/) { get; } | Provides options that control numbering and positioning of footnotes in this document. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Provides access to the footnote/endnote separators defined in the document. |
| [Frameset](../../aspose.words/document/frameset/) { get; } | Returns a [`Frameset`](./frameset/) instance if this document represents a frames page. |
| [GlossaryDocument](../../aspose.words/document/glossarydocument/) { get; set; } | Gets or sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document. |
| [GrammarChecked](../../aspose.words/document/grammarchecked/) { get; set; } | Returns `true` if the document has been checked for grammar. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Returns `true` if this node has any child nodes. |
| [HasMacros](../../aspose.words/document/hasmacros/) { get; } | Returns `true` if the document has a VBA project (macros). |
| [HasRevisions](../../aspose.words/document/hasrevisions/) { get; } | Returns `true` if the document has any tracked changes. |
| [HyphenationOptions](../../aspose.words/document/hyphenationoptions/) { get; } | Provides access to document hyphenation options. |
| [IncludeTextboxesFootnotesEndnotesInStat](../../aspose.words/document/includetextboxesfootnotesendnotesinstat/) { get; set; } | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Returns `true` as this node can have child nodes. |
| [JustificationMode](../../aspose.words/document/justificationmode/) { get; set; } | Gets or sets the character spacing adjustment of a document. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Gets the last child of the node. |
| [LastSection](../../aspose.words/document/lastsection/) { get; } | Gets the last section in the document. |
| [LayoutOptions](../../aspose.words/document/layoutoptions/) { get; } | Gets a [`LayoutOptions`](../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Provides access to the list formatting used in the document. |
| [MailMerge](../../aspose.words/document/mailmerge/) { get; } | Returns a [`MailMerge`](../../aspose.words.mailmerging/mailmerge/) object that represents the mail merge functionality for the document. |
| [MailMergeSettings](../../aspose.words/document/mailmergesettings/) { get; set; } | Gets or sets the object that contains all of the mail merge information for a document. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Gets the node immediately following this node. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Called when a node is inserted or removed in the document. |
| override [NodeType](../../aspose.words/document/nodetype/) { get; } | Returns Document. |
| [OriginalFileName](../../aspose.words/document/originalfilename/) { get; } | Gets the original file name of the document. |
| [OriginalLoadFormat](../../aspose.words/document/originalloadformat/) { get; } | Gets the format of the original document that was loaded into this object. |
| [PackageCustomParts](../../aspose.words/document/packagecustomparts/) { get; set; } | Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Gets or sets the page color of the document. This property is a simpler version of [`BackgroundShape`](../documentbase/backgroundshape/). |
| [PageCount](../../aspose.words/document/pagecount/) { get; } | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Gets the immediate parent of this node. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Gets the node immediately preceding this node. |
| [ProtectionType](../../aspose.words/document/protectiontype/) { get; } | Gets the currently active document protection type. |
| [PunctuationKerning](../../aspose.words/document/punctuationkerning/) { get; set; } | Specifies whether kerning applies to both Latin text and punctuation. |
| [Range](../../aspose.words/node/range/) { get; } | Returns a [`Range`](../range/) object that represents the portion of a document that is contained in this node. |
| [RemovePersonalInformation](../../aspose.words/document/removepersonalinformation/) { get; set; } | Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Allows to control how external resources are loaded. |
| [Revisions](../../aspose.words/document/revisions/) { get; } | Gets a collection of revisions (tracked changes) that exist in this document. |
| [RevisionsView](../../aspose.words/document/revisionsview/) { get; set; } | Gets or sets a value indicating whether to work with the original or revised version of a document. |
| [Sections](../../aspose.words/document/sections/) { get; } | Returns a collection that represents all sections in the document. |
| [ShadeFormData](../../aspose.words/document/shadeformdata/) { get; set; } | Specifies whether to turn on the gray shading on form fields. |
| [ShowGrammaticalErrors](../../aspose.words/document/showgrammaticalerrors/) { get; set; } | Specifies whether to display grammar errors in this document. |
| [ShowSpellingErrors](../../aspose.words/document/showspellingerrors/) { get; set; } | Specifies whether to display spelling errors in this document. |
| [SpellingChecked](../../aspose.words/document/spellingchecked/) { get; set; } | Returns `true` if the document has been checked for spelling. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Returns a collection of styles defined in the document. |
| [Theme](../../aspose.words/document/theme/) { get; } | Gets the [`Theme`](./theme/) object for this document. |
| [TrackRevisions](../../aspose.words/document/trackrevisions/) { get; set; } | True if changes are tracked when this document is edited in Microsoft Word. |
| [Variables](../../aspose.words/document/variables/) { get; } | Returns the collection of variables added to a document or template. |
| [VbaProject](../../aspose.words/document/vbaproject/) { get; set; } | Gets or sets a [`VbaProject`](./vbaproject/). |
| [VersionsCount](../../aspose.words/document/versionscount/) { get; } | Gets the number of document versions that was stored in the DOC document. |
| [ViewOptions](../../aspose.words/document/viewoptions/) { get; } | Provides options to control how the document is displayed in Microsoft Word. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [Watermark](../../aspose.words/document/watermark/) { get; } | Provides access to the document watermark. |
| [WebExtensionTaskPanes](../../aspose.words/document/webextensiontaskpanes/) { get; } | Returns a collection that represents a list of task pane add-ins. |
| [WriteProtection](../../aspose.words/document/writeprotection/) { get; } | Provides access to the document write protection options. |

## Methods

| Name | Description |
| --- | --- |
| override [Accept](../../aspose.words/document/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor. |
| [AcceptAllRevisions](../../aspose.words/document/acceptallrevisions/)() | Accepts all tracked changes in the document. |
| override [AcceptEnd](../../aspose.words/document/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor for visiting the end of the document. |
| override [AcceptStart](../../aspose.words/document/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Accepts a visitor for visiting the start of the document. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Adds the specified node to the end of the list of child nodes for this node. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument)(*Document, [ImportFormatMode](../importformatmode/)*) | Appends the specified document to the end of this document. |
| [AppendDocument](../../aspose.words/document/appenddocument/#appenddocument_1)(*Document, [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Appends the specified document to the end of this document. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup)() | Cleans unused styles and lists from the document. |
| [Cleanup](../../aspose.words/document/cleanup/#cleanup_1)(*[CleanupOptions](../cleanupoptions/)*) | Cleans unused styles and lists from the document depending on given [`CleanupOptions`](../cleanupoptions/). |
| [Clone](../../aspose.words/document/clone/#clone)() | Performs a deep copy of the `Document`. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Creates a duplicate of the node. |
| [Compare](../../aspose.words/document/compare/#compare)(*Document, string, DateTime*) | Compares this document with another document producing changes as number of edit and format revisions [`Revision`](../revision/). |
| [Compare](../../aspose.words/document/compare/#compare_1)(*Document, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compares this document with another document producing changes as a number of edit and format revisions [`Revision`](../revision/). Allows to specify comparison options using [`CompareOptions`](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate)(*Document*) | Copies styles from the specified template to a document. |
| [CopyStylesFromTemplate](../../aspose.words/document/copystylesfromtemplate/#copystylesfromtemplate_1)(*string*) | Copies styles from the specified template to a document. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Creates navigator which can be used to traverse and read nodes. |
| [EnsureMinimum](../../aspose.words/document/ensureminimum/)() | If the document contains no sections, creates one section with one paragraph. |
| [ExpandTableStylesToDirectFormatting](../../aspose.words/document/expandtablestylestodirectformatting/)() | Converts formatting specified in table styles into direct formatting on tables in the document. |
| [ExtractPages](../../aspose.words/document/extractpages/)(*int, int*) | Returns the `Document` object representing specified range of pages. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Gets the first ancestor of the specified [`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Gets the first ancestor of the specified object type. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Provides support for the for each style iteration over the child nodes of this node. |
| [GetPageInfo](../../aspose.words/document/getpageinfo/)(*int*) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Gets the text of this node and of all its children. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool*) | Imports a node from another document to the current document. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../node/), bool, [ImportFormatMode](../importformatmode/)*) | Imports a node from another document to the current document with an option to control formatting. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Returns the index of the specified child node in the child node array. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Inserts the specified node immediately before the specified reference node. |
| [JoinRunsWithSameFormatting](../../aspose.words/document/joinrunswithsameformatting/)() | Joins runs with same formatting in all paragraphs of the document. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Gets next node according to the pre-order tree traversal algorithm. |
| [NormalizeFieldTypes](../../aspose.words/document/normalizefieldtypes/)() | Changes field type values [`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) of [`FieldStart`](../../aspose.words.fields/fieldstart/), [`FieldSeparator`](../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Print](../../aspose.words/document/print/#print)() | Prints the whole document to the default printer. |
| [Print](../../aspose.words/document/print/#print_1)(*PrinterSettings*) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller. |
| [Print](../../aspose.words/document/print/#print_3)(*string*) | Print the whole document to the specified printer, using the standard (no User Interface) print controller. |
| [Print](../../aspose.words/document/print/#print_2)(*PrinterSettings, string*) | Prints the document according to the specified printer settings, using the standard (no User Interface) print controller and a document name. |
| [Protect](../../aspose.words/document/protect/#protect)(*[ProtectionType](../protectiontype/)*) | Protects the document from changes without changing the existing password or assigns a random password. |
| [Protect](../../aspose.words/document/protect/#protect_1)(*[ProtectionType](../protectiontype/), string*) | Protects the document from changes and optionally sets a protection password. |
| [Remove](../../aspose.words/node/remove/)() | Removes itself from the parent. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveBlankPages](../../aspose.words/document/removeblankpages/)() | Removes blank pages from the document. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Removes the specified child node. |
| [RemoveExternalSchemaReferences](../../aspose.words/document/removeexternalschemareferences/)() | Removes external XML schema references from this document. |
| [RemoveMacros](../../aspose.words/document/removemacros/)() | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Removes all [`SmartTag`](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [RenderToScale](../../aspose.words/document/rendertoscale/)(*int, Graphics, float, float, float*) | Renders a document page into a Graphics object to a specified scale. |
| [RenderToSize](../../aspose.words/document/rendertosize/)(*int, Graphics, float, float, float, float*) | Renders a document page into a Graphics object to a specified size. |
| [Save](../../aspose.words/document/save/#save_2)(*string*) | Saves the document to a file. Automatically determines the save format from the extension. |
| [Save](../../aspose.words/document/save/#save)(*Stream, [SaveFormat](../saveformat/)*) | Saves the document to a stream using the specified format. |
| [Save](../../aspose.words/document/save/#save_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Saves the document to a stream using the specified save options. |
| [Save](../../aspose.words/document/save/#save_3)(*string, [SaveFormat](../saveformat/)*) | Saves the document to a file in the specified format. |
| [Save](../../aspose.words/document/save/#save_4)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Saves the document to a file using the specified save options. |
| [Save](../../aspose.words/document/save/#save_5)(*HttpResponse, string, [ContentDisposition](../contentdisposition/), [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Sends the document to the client browser. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Selects the first [`Node`](../node/) that matches the XPath expression. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions)(*string*) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [StartTrackRevisions](../../aspose.words/document/starttrackrevisions/#starttrackrevisions_1)(*string, DateTime*) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [StopTrackRevisions](../../aspose.words/document/stoptrackrevisions/)() | Stops automatic marking of document changes as revisions. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exports the content of the node into a string in the specified format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exports the content of the node into a string using the specified save options. |
| [UnlinkFields](../../aspose.words/document/unlinkfields/)() | Unlinks fields in the whole document. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect_1)() | Removes protection from the document regardless of the password. |
| [Unprotect](../../aspose.words/document/unprotect/#unprotect)(*string*) | Removes protection from the document if a correct password is specified. |
| [UpdateActualReferenceMarks](../../aspose.words/document/updateactualreferencemarks/)() | Updates the [`ActualReferenceMark`](../../aspose.words.notes/footnote/actualreferencemark/) property of all footnotes and endnotes in the document. |
| [UpdateFields](../../aspose.words/document/updatefields/)() | Updates the values of fields in the whole document. |
| [UpdateListLabels](../../aspose.words/document/updatelistlabels/)() | Updates list labels for all list items in the document. |
| [UpdatePageLayout](../../aspose.words/document/updatepagelayout/)() | Rebuilds the page layout of the document. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail)() | Updates [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document using default options. |
| [UpdateThumbnail](../../aspose.words/document/updatethumbnail/#updatethumbnail_1)(*[ThumbnailGeneratingOptions](../../aspose.words.rendering/thumbnailgeneratingoptions/)*) | Updates [`Thumbnail`](../../aspose.words.properties/builtindocumentproperties/thumbnail/) of the document according to the specified options. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount)() | Updates word count properties of the document. |
| [UpdateWordCount](../../aspose.words/document/updatewordcount/#updatewordcount_1)(*bool*) | Updates word count properties of the document, optionally updates [`Lines`](../../aspose.words.properties/builtindocumentproperties/lines/) property. |

## Remarks

The `Document` is a central object in the Aspose.Words library.

To load an existing document in any of the [`LoadFormat`](../loadformat/) formats, pass a file name or a stream into one of the `Document` constructors. To create a blank document, call the constructor without parameters.

Use one of the Save method overloads to save the document in any of the [`SaveFormat`](../saveformat/) formats.

To draw document pages directly onto a **Graphics** object use [`RenderToScale`](./rendertoscale/) or [`RenderToSize`](./rendertosize/) method.

To print the document, use one of the [`Print`](./print/) methods.

[`MailMerge`](./mailmerge/) is the Aspose.Words's reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a DataSet, DataTable, DataView, IDataReader or an array of values. **MailMerge** will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

`Document` stores document-wide information such as [`Styles`](../documentbase/styles/), [`BuiltInDocumentProperties`](./builtindocumentproperties/), [`CustomDocumentProperties`](./customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the `Document`.

The `Document` is a root node of a tree that contains all other nodes of the document. The tree is a Composite design pattern and in many ways similar to XmlDocument. The content of the document can be manipulated freely programmatically:

* The nodes of the document can be accessed via typed collections, for example [`Sections`](./sections/), [`ParagraphCollection`](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [`GetChildNodes`](../compositenode/getchildnodes/) or using an XPath query with [`SelectNodes`](../compositenode/selectnodes/) or [`SelectSingleNode`](../compositenode/selectsinglenode/).
* Content nodes can be added or removed from anywhere in the document using [`InsertBefore`](../compositenode/insertbefore/), [`InsertAfter`](../compositenode/insertafter/), [`RemoveChild`](../compositenode/removechild/) and other methods provided by the base class [`CompositeNode`](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.

Consider using [`DocumentBuilder`](../documentbuilder/) that simplifies the task of programmatically creating or populating the document tree.

The `Document` can contain only [`Section`](../section/) objects.

In Microsoft Word, a valid document needs to have at least one section.

## Examples

Shows how to execute a mail merge with data from a DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Below are two ways of using a DataTable as the data source for a mail merge.
    // 1 -  Use the entire table for the mail merge to create one output mail merge document for every row in the table:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 -  Use one row of the table to create one output mail merge document:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Creates a mail merge source document.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### See Also

* class [DocumentBase](../documentbase/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
