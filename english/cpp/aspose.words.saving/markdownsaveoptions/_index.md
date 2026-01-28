---
title: Aspose::Words::Saving::MarkdownSaveOptions class
linktitle: MarkdownSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions class. Class to specify additional options when saving a document into the Markdown format. To learn more, visit the  documentation article in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class


Class to specify additional options when saving a document into the [Markdown](../../aspose.words/saveformat/) format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class MarkdownSaveOptions : public Aspose::Words::Saving::TxtSaveOptionsBase
```

## Methods

| Method | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/)() const | Specifies how to export empty paragraphs to Markdown. Default value is [EmptyLine](../markdownemptyparagraphexportmode/). |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | Specifies the encoding to use when exporting in text formats. Default value is **Encoding.UTF8**. |
| [get_ExportAsHtml](./get_exportashtml/)() const | Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [None](../markdownexportashtml/). |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | Specifies the way headers and footers are exported to the text formats. Default value is [PrimaryOnly](../txtexportheadersfootersmode/). |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Specifies whether images are saved in Base64 format to the output file. Default value is **false**. |
| [get_ExportUnderlineFormatting](./get_exportunderlineformatting/)() const | Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is **false**. |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | Allows to specify whether the page breaks should be preserved during export. The default value is **false**. |
| [get_ImageResolution](./get_imageresolution/)() const | Specifies the output resolution for images when exporting to Markdown. Default is **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Allows to control how images are saved when a document is saved to [Markdown](../../aspose.words/saveformat/) format. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Specifies the physical folder where images are saved when exporting a document to the [Markdown](../../aspose.words/saveformat/) format. Default is an empty string. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_LinkExportMode](./get_linkexportmode/)() const | Specifies how links will be written to the output file. Default value is [Auto](../markdownlinkexportmode/). |
| [get_ListExportMode](./get_listexportmode/)() const | Specifies how list items will be written to the output file. Default value is [MarkdownSyntax](../markdownlistexportmode/). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | Specifies how OfficeMath will be written to the output file. Default value is [Text](../markdownofficemathexportmode/). |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | Specifies the string to use as a paragraph break when exporting in text formats. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Allows to control how resources are saved when a document is exported to [Markdown](../../aspose.words/saveformat/) format. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Markdown](../../aspose.words/saveformat/). |
| [get_TableContentAlignment](./get_tablecontentalignment/)() const | Gets or sets a value that specifies how to align contents in tables when exporting into the [Markdown](../../aspose.words/saveformat/) format. The default value is [Auto](../tablecontentalignment/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is **null** and no temporary files are used. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determines whether the font attributes will be changed according to the character code being used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets or sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Gets a value determining whether OLE controls presentation image will be updated. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MarkdownSaveOptions](./markdownsaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the [Markdown](../../aspose.words/saveformat/) format. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_EmptyParagraphExportMode](./set_emptyparagraphexportmode/)(Aspose::Words::Saving::MarkdownEmptyParagraphExportMode) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/). |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter for [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](../txtsaveoptionsbase/get_encoding/). |
| [set_ExportAsHtml](./set_exportashtml/)(Aspose::Words::Saving::MarkdownExportAsHtml) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml](./get_exportashtml/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | Setter for [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportUnderlineFormatting](./set_exportunderlineformatting/)(bool) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting](./get_exportunderlineformatting/). |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | Setter for [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Allows to control how images are saved when a document is saved to [Markdown](../../aspose.words/saveformat/) format. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_LinkExportMode](./set_linkexportmode/)(Aspose::Words::Saving::MarkdownLinkExportMode) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode](./get_linkexportmode/). |
| [set_ListExportMode](./set_listexportmode/)(Aspose::Words::Saving::MarkdownListExportMode) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode](./get_listexportmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::MarkdownOfficeMathExportMode) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode](./get_officemathexportmode/). |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String\&) | Setter for [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Allows to control how resources are saved when a document is exported to [Markdown](../../aspose.words/saveformat/) format. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Markdown](../../aspose.words/saveformat/). |
| [set_TableContentAlignment](./set_tablecontentalignment/)(Aspose::Words::Saving::TableContentAlignment) | Setter for [Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment](./get_tablecontentalignment/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Sets a value determining whether OLE controls presentation image will be updated. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |
## See Also

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
