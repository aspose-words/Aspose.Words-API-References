---
title: Aspose::Words::Document class
linktitle: Document
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document class. Represents a Word document. To learn more, visit the Working with Document documentation article in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/document/
---
## Document class


Represents a Word document. 
To learn more, visit the [Working with Document](https://docs.aspose.com/words/cpp/working-with-document/) documentation article.

```cpp
class Document : public DocumentBase,
                 public ISectionAttrSource,
                 public IWatermarkProvider
```

## Methods

| Method | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor. |
| [AcceptAllRevisions](./acceptallrevisions/)() | Accepts all tracked changes in the document. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the end of the document. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepts a visitor for visiting the start of the document. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\> \&, Aspose::Words::ImportFormatMode) | Appends the specified document to the end of this document. |
| [AppendDocument](./appenddocument/)(const System::SharedPtr\<Aspose::Words::Document\> \&, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\> \&) | Appends the specified document to the end of this document. |
| [Cleanup](./cleanup/)() | Cleans unused styles and lists from the document. |
| [Cleanup](./cleanup/)(const System::SharedPtr\<Aspose::Words::CleanupOptions\> \&) | Cleans unused styles and lists from the document depending on given [CleanupOptions](../cleanupoptions/). |
| [Clone](./clone/)() | Performs a deep copy of the [Document](./). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\> \&, const System::String \&, System::DateTime) | Compares this document with another document producing changes as number of edit and format revisions [Revision](../revision/). |
| [Compare](./compare/)(const System::SharedPtr\<Aspose::Words::Document\> \&, const System::String \&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\> \&) | Compares this document with another document producing changes as a number of edit and format revisions [Revision](../revision/). Allows to specify comparison options using [CompareOptions](../../aspose.words.comparing/compareoptions/). |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::SharedPtr\<Aspose::Words::Document\> \&) | Copies styles from the specified template to a document. |
| [CopyStylesFromTemplate](./copystylesfromtemplate/)(const System::String \&) | Copies styles from the specified template to a document. |
| [Document](./document/)() | Creates a blank Word document. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\> \&) | Opens an existing document from a stream. Automatically detects the file format. |
| [Document](./document/)(const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) | Opens an existing document from a stream. Allows to specify additional options such as an encryption password. |
| [Document](./document/)(const System::String \&) | Opens an existing document from a file. Automatically detects the file format. |
| [Document](./document/)(const System::String \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) | Opens an existing document from a file. Allows to specify additional options such as an encryption password. |
| [Document](./document/)(std::istream \&) |  |
| [Document](./document/)(std::istream \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) |  |
| [EnsureMinimum](./ensureminimum/)() | If the document contains no sections, creates one section with one paragraph. |
| [ExpandTableStylesToDirectFormatting](./expandtablestylestodirectformatting/)() | Converts formatting specified in table styles into direct formatting on tables in the document. |
| [ExtractPages](./extractpages/)(int32_t, int32_t) | Returns the [Document](./) object representing specified range of pages. |
| [ExtractPages](./extractpages/)(int32_t, int32_t, const System::SharedPtr\<Aspose::Words::PageExtractOptions\> \&) | Returns the [Document](./) object representing the specified range of pages and the given page extract options. |
| [GetPageInfo](./getpageinfo/)(int32_t) | Gets the page size, orientation and other information about a page that might be useful for printing or rendering. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Joins runs with same formatting in all paragraphs of the document. |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Changes field type values [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) of [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes. |
| [Protect](./protect/)(Aspose::Words::ProtectionType) | Protects the document from changes without changing the existing password or assigns a random password. |
| [Protect](./protect/)(Aspose::Words::ProtectionType, const System::String \&) | Protects the document from changes and optionally sets a protection password. |
| [RemoveBlankPages](./removeblankpages/)() | Removes blank pages from the document. |
| [RemoveCustomizations](./removecustomizations/)() | Removes toolbar and keyboard command customizations from the document. |
| [RemoveExternalSchemaReferences](./removeexternalschemareferences/)() | Removes external XML schema references from this document. |
| [RemoveMacros](./removemacros/)() | Removes all macros (the VBA project) as well as toolbars and command customizations from the document. |
| [RenderToScale](./rendertoscale/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\> \&, float, float, float) | Renders a document page into a **Graphics** object to a specified scale. |
| [RenderToSize](./rendertosize/)(int32_t, const System::SharedPtr\<System::Drawing::Graphics\> \&, float, float, float, float) | Renders a document page into a **Graphics** object to a specified size. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\> \&, Aspose::Words::SaveFormat) | Saves the document to a stream using the specified format. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Saves the document to a stream using the specified save options. |
| [Save](./save/)(const System::String \&) | Saves the document to a file. Automatically determines the save format from the extension. |
| [Save](./save/)(const System::String \&, Aspose::Words::SaveFormat) | Saves the document to a file in the specified format. |
| [Save](./save/)(const System::String \&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Saves the document to a file using the specified save options. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\> \&, Aspose::Words::SaveFormat) |  |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\> \&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) |  |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String \&) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [StartTrackRevisions](./starttrackrevisions/)(const System::String \&, System::DateTime) | Starts automatically marking all further changes you make to the document programmatically as revision changes. |
| [StopTrackRevisions](./stoptrackrevisions/)() | Stops automatic marking of document changes as revisions. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Unlinks fields in the whole document. |
| [Unprotect](./unprotect/)() | Removes protection from the document regardless of the password. |
| [Unprotect](./unprotect/)(const System::String \&) | Removes protection from the document if a correct password is specified. |
| [UpdateActualReferenceMarks](./updateactualreferencemarks/)() | Updates the [ActualReferenceMark](../../aspose.words.notes/footnote/get_actualreferencemark/) property of all footnotes and endnotes in the document. |
| [UpdateFields](./updatefields/)() | Updates the values of fields in the whole document. |
| [UpdateListLabels](./updatelistlabels/)() | Updates list labels for all list items in the document. |
| [UpdatePageLayout](./updatepagelayout/)() | Rebuilds the page layout of the document. |
| [UpdateTableLayout](./updatetablelayout/)() | Implements an earlier approach to table column widths re-calculation that has known issues. |
| [UpdateThumbnail](./updatethumbnail/)() | Updates [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) of the document using default options. |
| [UpdateThumbnail](./updatethumbnail/)(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\> \&) | Updates [Thumbnail](../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) of the document according to the specified options. |
| [UpdateWordCount](./updatewordcount/)() | Updates word count properties of the document. |
| [UpdateWordCount](./updatewordcount/)(bool) | Updates word count properties of the document, optionally updates [Lines](../../aspose.words.properties/builtindocumentproperties/get_lines/) property. |
| [get_AttachedTemplate](./get_attachedtemplate/)() | Gets or sets the full path of the template attached to the document. |
| [get_AutomaticallyUpdateStyles](./get_automaticallyupdatestyles/)() | Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [get_Bibliography](./get_bibliography/)() | Gets the [Bibliography](./get_bibliography/) object that represents the list of sources available in the document. |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Returns a collection that represents all the built-in document properties of the document. |
| [get_CompatibilityOptions](./get_compatibilityoptions/)() | Provides access to document compatibility options (that is, the user preferences entered on the Compatibility tab of the Options dialog in Word). |
| [get_Compliance](./get_compliance/)() | Gets the OOXML compliance version determined from the loaded document content. Makes sense only for OOXML documents. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() | Returns a collection that represents all the custom document properties of the document. |
| [get_CustomXmlParts](./get_customxmlparts/)() const | Gets or sets the collection of Custom XML Data Storage Parts. |
| [get_DefaultTabStop](./get_defaulttabstop/)() | Gets or sets the interval (in points) between the default tab stops. |
| [get_DigitalSignatures](./get_digitalsignatures/)() const | Gets the collection of digital signatures for this document and their validation results. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Provides options that control numbering and positioning of endnotes in this document. |
| [get_FieldOptions](./get_fieldoptions/)() | Gets a [FieldOptions](../../aspose.words.fields/fieldoptions/) object that represents options to control field handling in the document. |
| [get_FirstSection](./get_firstsection/)() | Gets the first section in the document. |
| [get_FontSettings](./get_fontsettings/)() const | Gets or sets document font settings. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Provides options that control numbering and positioning of footnotes in this document. |
| [get_Frameset](./get_frameset/)() const | Returns a [Frameset](./get_frameset/) instance if this document represents a frames page. |
| [get_GlossaryDocument](./get_glossarydocument/)() const | Gets or sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document. |
| [get_GrammarChecked](./get_grammarchecked/)() | Returns **true** if the document has been checked for grammar. |
| [get_HasMacros](./get_hasmacros/)() | Returns **true** if the document has a VBA project (macros). |
| [get_HasRevisions](./get_hasrevisions/)() | Returns **true** if the document has any tracked changes. |
| [get_HyphenationOptions](./get_hyphenationoptions/)() | Provides access to document hyphenation options. |
| [get_IncludeTextboxesFootnotesEndnotesInStat](./get_includetextboxesfootnotesendnotesinstat/)() | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| [get_JustificationMode](./get_justificationmode/)() | Gets or sets the character spacing adjustment of a document. |
| [get_LastSection](./get_lastsection/)() | Gets the last section in the document. |
| [get_LayoutOptions](./get_layoutoptions/)() const | Gets a [LayoutOptions](../../aspose.words.layout/layoutoptions/) object that represents options to control the layout process of this document. |
| [get_MailMerge](./get_mailmerge/)() | Returns a [MailMerge](../../aspose.words.mailmerging/mailmerge/) object that represents the mail merge functionality for the document. |
| [get_MailMergeSettings](./get_mailmergesettings/)() | Gets or sets the object that contains all of the mail merge information for a document. |
| [get_NodeType](./get_nodetype/)() const override | Returns [Document](../nodetype/). |
| [get_OriginalFileName](./get_originalfilename/)() const | Gets the original file name of the document. |
| [get_OriginalLoadFormat](./get_originalloadformat/)() const | Gets the format of the original document that was loaded into this object. |
| [get_PackageCustomParts](./get_packagecustomparts/)() const | Gets or sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [get_PageCount](./get_pagecount/)() | Gets the number of pages in the document as calculated by the most recent page layout operation. |
| [get_ProtectionType](./get_protectiontype/)() | Gets the currently active document protection type. |
| [get_PunctuationKerning](./get_punctuationkerning/)() | Specifies whether kerning applies to both Latin text and punctuation. |
| [get_ReadabilityStatistics](./get_readabilitystatistics/)() | Provides readability score information for the document. |
| [get_RemovePersonalInformation](./get_removepersonalinformation/)() | Gets or sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [get_Revisions](./get_revisions/)() | Gets a collection of revisions (tracked changes) that exist in this document. |
| [get_RevisionsView](./get_revisionsview/)() const | Gets or sets a value indicating whether to work with the original or revised version of a document. |
| [get_Sections](./get_sections/)() | Returns a collection that represents all sections in the document. |
| [get_ShadeFormData](./get_shadeformdata/)() | Specifies whether to turn on the gray shading on form fields. |
| [get_ShowGrammaticalErrors](./get_showgrammaticalerrors/)() | Specifies whether to display grammar errors in this document. |
| [get_ShowSpellingErrors](./get_showspellingerrors/)() | Specifies whether to display spelling errors in this document. |
| [get_SpellingChecked](./get_spellingchecked/)() | Returns **true** if the document has been checked for spelling. |
| [get_Theme](./get_theme/)() | Gets the [Theme](./get_theme/) object for this document. |
| [get_TrackRevisions](./get_trackrevisions/)() | True if changes are tracked when this document is edited in Microsoft Word. |
| [get_Variables](./get_variables/)() | Returns the collection of variables added to a document or template. |
| [get_VbaProject](./get_vbaproject/)() const | Gets or sets a [VbaProject](./get_vbaproject/). |
| [get_VersionsCount](./get_versionscount/)() | Gets the number of document versions that was stored in the DOC document. |
| [get_ViewOptions](./get_viewoptions/)() | Provides options to control how the document is displayed in Microsoft Word. |
| [get_Watermark](./get_watermark/)() | Provides access to the document watermark. |
| [get_WebExtensionTaskPanes](./get_webextensiontaskpanes/)() const | Returns a collection that represents a list of task pane add-ins. |
| [get_WriteProtection](./get_writeprotection/)() | Provides access to the document write protection options. |
| [set_AttachedTemplate](./set_attachedtemplate/)(const System::String \&) | Sets the full path of the template attached to the document. |
| [set_AutomaticallyUpdateStyles](./set_automaticallyupdatestyles/)(bool) | Sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word. |
| [set_CustomXmlParts](./set_customxmlparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPartCollection\> \&) | Sets the collection of Custom XML Data Storage Parts. |
| [set_DefaultTabStop](./set_defaulttabstop/)(double) | Sets the interval (in points) between the default tab stops. |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\> \&) | Sets document font settings. |
| [set_GlossaryDocument](./set_glossarydocument/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\> \&) | Sets the glossary document within this document or template. A glossary document is a storage for AutoText, AutoCorrect and Building Block entries defined in a document. |
| [set_GrammarChecked](./set_grammarchecked/)(bool) | Returns **true** if the document has been checked for grammar. |
| [set_IncludeTextboxesFootnotesEndnotesInStat](./set_includetextboxesfootnotesendnotesinstat/)(bool) | Specifies whether to include textboxes, footnotes and endnotes in word count statistics. |
| [set_JustificationMode](./set_justificationmode/)(Aspose::Words::Settings::JustificationMode) | Sets the character spacing adjustment of a document. |
| [set_MailMergeSettings](./set_mailmergesettings/)(const System::SharedPtr\<Aspose::Words::Settings::MailMergeSettings\> \&) | Sets the object that contains all of the mail merge information for a document. |
| [set_PackageCustomParts](./set_packagecustomparts/)(const System::SharedPtr\<Aspose::Words::Markup::CustomPartCollection\> \&) | Sets the collection of custom parts (arbitrary content) that are linked to the OOXML package using "unknown relationships". |
| [set_PunctuationKerning](./set_punctuationkerning/)(bool) | Specifies whether kerning applies to both Latin text and punctuation. |
| [set_RemovePersonalInformation](./set_removepersonalinformation/)(bool) | Sets a flag indicating that Microsoft Word will remove all user information from comments, revisions and document properties upon saving the document. |
| [set_RevisionsView](./set_revisionsview/)(Aspose::Words::RevisionsView) | Sets a value indicating whether to work with the original or revised version of a document. |
| [set_ShadeFormData](./set_shadeformdata/)(bool) | Specifies whether to turn on the gray shading on form fields. |
| [set_ShowGrammaticalErrors](./set_showgrammaticalerrors/)(bool) | Specifies whether to display grammar errors in this document. |
| [set_ShowSpellingErrors](./set_showspellingerrors/)(bool) | Specifies whether to display spelling errors in this document. |
| [set_SpellingChecked](./set_spellingchecked/)(bool) | Returns **true** if the document has been checked for spelling. |
| [set_TrackRevisions](./set_trackrevisions/)(bool) | True if changes are tracked when this document is edited in Microsoft Word. |
| [set_VbaProject](./set_vbaproject/)(const System::SharedPtr\<Aspose::Words::Vba::VbaProject\> \&) | Sets a [VbaProject](./get_vbaproject/). |
| [GetType](../documentbase/gettype/)() const override |  |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&, bool) | Imports a node from another document to the current document. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&, bool, Aspose::Words::ImportFormatMode) | Imports a node from another document to the current document with an option to control formatting. |
| [ImportNode](../documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\> \&) | Imports a node from another document to the current document with an option to control formatting. |
| [Is](../documentbase/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../documentbase/type/)() |  |
| [get_BackgroundShape](../documentbase/get_backgroundshape/)() const | Gets or sets the background shape of the document. Can be **null**. |
| [get_Document](../documentbase/get_document/)() const override | Gets this instance. |
| [get_FontInfos](../documentbase/get_fontinfos/)() const | Provides access to properties of fonts used in this document. |
| [get_FootnoteSeparators](../documentbase/get_footnoteseparators/)() const | Provides access to the footnote/endnote separators defined in the document. |
| [get_Lists](../documentbase/get_lists/)() const | Provides access to the list formatting used in the document. |
| [get_NodeChangingCallback](../documentbase/get_nodechangingcallback/)() | Called when a node is inserted or removed in the document. |
| [get_PageColor](../documentbase/get_pagecolor/)() | Gets or sets the page color of the document. This property is a simpler version of [BackgroundShape](../documentbase/get_backgroundshape/). |
| [get_ResourceLoadingCallback](../documentbase/get_resourceloadingcallback/)() const | Allows to control how external resources are loaded. |
| [get_Styles](../documentbase/get_styles/)() const | Returns a collection of styles defined in the document. |
| [get_WarningCallback](../documentbase/get_warningcallback/)() const | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| [set_BackgroundShape](../documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\> \&) | Sets the background shape of the document. Can be **null**. |
| [set_NodeChangingCallback](../documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\> \&) | Called when a node is inserted or removed in the document. |
| [set_PageColor](../documentbase/set_pagecolor/)(System::Drawing::Color) | Sets the page color of the document. This property is a simpler version of [BackgroundShape](../documentbase/get_backgroundshape/). |
| [set_ResourceLoadingCallback](../documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\> \&) | Allows to control how external resources are loaded. |
| [set_WarningCallback](../documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Called during various document processing procedures when an issue is detected that might result in data or formatting fidelity loss. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXEnd method of the specified document visitor. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | When implemented in a derived class, calls the VisitXXXStart method of the specified document visitor. |
| [AppendChild](../compositenode/appendchild/)(T) | Adds the specified node to the end of the list of child nodes for this node. |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Returns an Nth child node that matches the specified type. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Returns a live collection of child nodes that match the specified type. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Provides support for the for each style iteration over the child nodes of this node. |
| [GetText](../compositenode/gettext/)() override | Gets the text of this node and of all its children. |
| [GetType](../compositenode/gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Returns the index of the specified child node in the child node array. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately after the specified reference node. |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\> \&) | Inserts the specified node immediately before the specified reference node. |
| [Is](../compositenode/is/)(const System::TypeInfo \&) const override |  |
| [PrependChild](../compositenode/prependchild/)(T) | Adds the specified node to the beginning of the list of child nodes for this node. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Removes all the child nodes of the current node. |
| [RemoveChild](../compositenode/removechild/)(T) | Removes the specified child node. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Removes all [SmartTag](../../aspose.words.markup/smarttag/) descendant nodes of the current node. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String \&) | Selects a list of nodes matching the XPath expression. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String \&) | Selects the first [Node](../node/) that matches the XPath expression. |
| static [Type](../compositenode/type/)() |  |
| [get_Count](../compositenode/get_count/)() | Gets the number of immediate children of this node. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Gets the first child of the node. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Returns **true** if this node has any child nodes. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Returns **true** as this node can have child nodes. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Gets the last child of the node. |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accepts a visitor. |
| [Clone](../node/clone/)(bool) | Creates a duplicate of the node. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Gets the first ancestor of the specified [NodeType](../nodetype/). |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Gets the text of this node and of all its children. |
| [GetType](../node/gettype/)() const override |  |
| [Is](../node/is/)(const System::TypeInfo \&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets next node according to the pre-order tree traversal algorithm. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | A utility method that converts a node type enum value into a user friendly string. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\> \&) | Gets the previous node according to the pre-order tree traversal algorithm. |
| [Remove](../node/remove/)() | Removes itself from the parent. |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Exports the content of the node into a string in the specified format. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> \&) | Exports the content of the node into a string using the specified save options. |
| static [Type](../node/type/)() |  |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifies custom node identifier. |
| virtual [get_Document](../node/get_document/)() const | Gets the document to which this node belongs. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Returns **true** if this node can contain other nodes. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Gets the node immediately following this node. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Gets the type of this node. |
| [get_ParentNode](../node/get_parentnode/)() | Gets the immediate parent of this node. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_PreviousSibling](../node/get_previoussibling/)() | Gets the node immediately preceding this node. |
| [get_Range](../node/get_range/)() | Returns a [Range](../range/) object that represents the portion of a document that is contained in this node. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Specifies custom node identifier. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\> \&) |  |
## Remarks


The [Document](./) is a central object in the Aspose.Words library.

To load an existing document in any of the [LoadFormat](../loadformat/) formats, pass a file name or a stream into one of the [Document](./) constructors. To create a blank document, call the constructor without parameters.

Use one of the Save method overloads to save the document in any of the [SaveFormat](../saveformat/) formats.

To draw document pages directly onto a Graphics object use [RenderToScale()](./rendertoscale/) or [RenderToSize()](./rendertosize/) method.

To print the document, use one of the **Print()** methods.

[MailMerge](./get_mailmerge/) is the Aspose.Words's reporting engine that allows to populate reports designed in Microsoft Word with data from various data sources quickly and easily. The data can be from a or an array of values. MailMerge will go through the records found in the data source and insert them into mail merge fields in the document growing it as necessary.

[Document](./) stores document-wide information such as [Styles](../documentbase/get_styles/), [BuiltInDocumentProperties](./get_builtindocumentproperties/), [CustomDocumentProperties](./get_customdocumentproperties/), lists and macros. Most of these objects are accessible via the corresponding properties of the [Document](./).

The [Document](./) is a root node of a tree that contains all other nodes of the document. The tree is a Composite design pattern and in many ways similar to XmlDocument. The content of the document can be manipulated freely programmatically:
* The nodes of the document can be accessed via typed collections, for example [Sections](./get_sections/), [ParagraphCollection](../paragraphcollection/) etc.
* The nodes of the document can be selected by their node type using [GetChildNodes()](../compositenode/getchildnodes/) or using an XPath query with [SelectNodes()](../compositenode/selectnodes/) or [SelectSingleNode()](../compositenode/selectsinglenode/).
* Content nodes can be added or removed from anywhere in the document using [InsertBefore()](../compositenode/insertbefore/), [InsertAfter()](../compositenode/insertafter/), [RemoveChild()](../compositenode/removechild/) and other methods provided by the base class [CompositeNode](../compositenode/).
* The formatting attributes of each node can be changed via the properties of that node.


Consider using [DocumentBuilder](../documentbuilder/) that simplifies the task of programmatically creating or populating the document tree.

The [Document](./) can contain only [Section](../section/) objects.

In Microsoft Word, a valid document needs to have at least one section.
## See Also

* Class [DocumentBase](../documentbase/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
