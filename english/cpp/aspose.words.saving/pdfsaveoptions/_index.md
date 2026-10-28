---
title: Aspose::Words::Saving::PdfSaveOptions class
linktitle: PdfSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfSaveOptions class. Can be used to specify additional options when saving a document into the Pdf format. To learn more, visit the Specify Save Options documentation article in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Can be used to specify additional options when saving a document into the [Pdf](../../aspose.words/saveformat/) format. 
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class PdfSaveOptions : public FixedPageSaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Creates a deep clone of this object. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the [Pdf](../../aspose.words/saveformat/) format. |
| static [Type](./type/)() |  |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | A flag specifying whether to write additional text positioning operators or not. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Gets or sets a value determining how attachments are embedded to the PDF document. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Gets or sets a value determining whether or not to cache graphics placed in document's background. |
| [get_Compliance](./get_compliance/)() const | Specifies the PDF standards compliance level for output documents. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Gets or sets a value determining the way [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) are exported to PDF file. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Gets or sets the details for signing the output PDF document. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Allows to specify downsample options. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Controls how fonts are embedded into the resulting PDF documents. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Gets or sets the details for encrypting the output PDF document. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Gets or sets a value determining whether or not to export document structure. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Gets or sets a value determining whether floating shapes are exported as inline tags in the document structure. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Gets or sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Gets or sets a value determining whether a paragraph graphic should be marked as an artifact. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Specifies the font embedding mode. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF. Default is **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Determines how bookmarks in headers/footers are exported. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Specifies how the color space will be selected for the images in PDF document. |
| [get_ImageCompression](./get_imagecompression/)() const | Specifies compression type to be used for all images in the document. |
| [get_InterpolateImages](./get_interpolateimages/)() const | A flag indicating whether image interpolation shall be performed by a conforming reader. When **false** is specified, the flag is not written to the output document and the default behaviour of reader is used instead. |
| [get_JpegQuality](./get_jpegquality/)() | Gets or sets a value determining the quality of the JPEG images inside PDF document. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Allows to specify outline options. |
| [get_PageLayout](./get_pagelayout/)() const | Specifies the page layout to be used when the document is opened in a PDF reader. |
| [get_PageMode](./get_pagemode/)() const | Specifies how the PDF document should be displayed when opened in a PDF reader. |
| [get_PreblendImages](./get_preblendimages/)() const | Gets or sets a value determining whether or not to preblend transparent images with black background color. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is **false**. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Specifies whether to render PDF choice form field border. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Pdf](../../aspose.words/saveformat/). |
| [get_TextCompression](./get_textcompression/)() const | Specifies compression type to be used for all textual content in the document. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Specifies whether to use SDT control Tag or Id property as a name of form field in PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Gets or sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Gets or sets a value determining zoom factor (in percentages) for a document. |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | A flag specifying whether to write additional text positioning operators or not. |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Sets a value determining how attachments are embedded to the PDF document. |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Sets a value determining whether or not to cache graphics placed in document's background. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Specifies the PDF standards compliance level for output documents. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Specifies whether to convert footnote/endnote references in main text story into active hyperlinks. When clicked the hyperlink will lead to the corresponding footnote/endnote. Default is **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Sets a value determining the way [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) are exported to PDF file. |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\> \&) | Sets the details for signing the output PDF document. |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | A flag specifying whether the window’s title bar should display the document title taken from the Title entry of the document information dictionary. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Sets a value determining how DrawingML effects are rendered. |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\> \&) | Allows to specify downsample options. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Controls how fonts are embedded into the resulting PDF documents. |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\> \&) | Sets the details for encrypting the output PDF document. |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Sets a value determining whether or not to export document structure. |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Sets a value determining whether floating shapes are exported as inline tags in the document structure. |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Sets a value determining whether or not to create a "Span" tag in the document structure to export the text language. |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Sets a value determining whether a paragraph graphic should be marked as an artifact. |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Specifies the font embedding mode. |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF. Default is **false**. |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Determines how bookmarks in headers/footers are exported. |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Specifies how the color space will be selected for the images in PDF document. |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Specifies compression type to be used for all images in the document. |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | A flag indicating whether image interpolation shall be performed by a conforming reader. When **false** is specified, the flag is not written to the output document and the default behaviour of reader is used instead. |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Sets a value determining the quality of the JPEG images inside PDF document. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser. |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Specifies the page layout to be used when the document is opened in a PDF reader. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Specifies how the PDF document should be displayed when opened in a PDF reader. |
| [set_PreblendImages](./set_preblendimages/)(bool) | Sets a value determining whether or not to preblend transparent images with black background color. |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Specifies whether to preserve Microsoft Word form fields as form fields in PDF or convert them to text. Default is **false**. |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Specifies whether to render PDF choice form field border. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Pdf](../../aspose.words/saveformat/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Specifies compression type to be used for all textual content in the document. |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts. |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Specifies whether to use SDT control Tag or Id property as a name of form field in PDF. |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Sets a value determining what type of zoom should be applied when a document is opened with a PDF viewer. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Sets a value determining zoom factor (in percentages) for a document. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [GetType](../fixedpagesaveoptions/gettype/)() const override |  |
| [Is](../fixedpagesaveoptions/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../fixedpagesaveoptions/type/)() |  |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Gets or sets a value determining how colors are rendered. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Gets or sets a value determining the quality of the JPEG images inside Html document. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Allows to specify metafile rendering options. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **false**. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Gets or sets the pages to render. Default is all the pages in the document. |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Sets a value determining how colors are rendered. |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Sets a value determining the quality of the JPEG images inside Html document. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\> \&) | Allows to specify metafile rendering options. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **false**. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\> \&) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\> \&) | Sets the pages to render. Default is all the pages in the document. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String \&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [GetType](../saveoptions/gettype/)() const override |  |
| [Is](../saveoptions/is/)(const System::TypeInfo \&) const override |  |
| static [Type](../saveoptions/type/)() |  |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is empty string. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets or sets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| virtual [get_SaveFormat](../saveoptions/get_saveformat/)() | Specifies the format in which the document will be saved if this save options object is used. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is **null** and no temporary files are used. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determines whether the font attributes will be changed according to the character code being used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets or sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**; |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Gets a value determining whether OLE controls presentation image will be updated. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\> \&) | Sets custom local time zone used for date/time fields. |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String \&) | Sets path to default template (including filename). Default value for this property is empty string. |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Sets a value determining how DrawingML effects are rendered. |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Sets a value determining how DrawingML shapes are rendered. |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Sets a value determining how ink (InkML) objects are rendered. |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | When **true**, pretty formats output where applicable. Default value is **false**. |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\> \&) | Called during saving a document and accepts data about saving progress. |
| virtual [set_SaveFormat](../saveoptions/set_saveformat/)(Aspose::Words::SaveFormat) | Specifies the format in which the document will be saved if this save options object is used. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String \&) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default, this property is **null** and no temporary files are used. |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Determines whether the font attributes will be changed according to the character code being used. |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**; |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Sets a value determining whether OLE controls presentation image will be updated. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Sets a value determining whether or not to use anti-aliasing for rendering. |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
## See Also

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
