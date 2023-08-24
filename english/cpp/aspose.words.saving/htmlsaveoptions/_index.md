---
title: Aspose::Words::Saving::HtmlSaveOptions class
linktitle: HtmlSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions class. Can be used to specify additional options when saving a document into the Html, Mhtml, Epub, Azw3 or Mobi format. To learn more, visit the  documentation article in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Can be used to specify additional options when saving a document into the [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/) format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Specifies the path and the name of the Cascading [Style](../../aspose.words/style/) Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Specifies how CSS (Cascading [Style](../../aspose.words/style/) Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [Inline](../cssstylesheettype/) for HTML/MHTML and [External](../cssstylesheettype/) for EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const |  |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Specifies how the document should be split when saving to [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) or [Azw3](../../aspose.words/saveformat/) format. Default is [None](../documentsplitcriteria/) for HTML and [HeadingParagraph](../documentsplitcriteria/) for EPUB and AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Specifies the maximum level of headings at which to split the document. Default value is **%2**. |
| [get_Encoding](./get_encoding/)() const | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is **new UTF8Encoding(false)** (UTF-8 without BOM). |
| [get_EpubNavigationMapLevel](./get_epubnavigationmaplevel/)() | Specifies the maximum level of headings populated to the navigation map when exporting to IDPF EPUB, MOBI, or AZW3 formats. Default value is **%3**. |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Controls how drop-down form fields are saved to HTML or MHTML. Default value is **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [PerSection](../exportheadersfootersmode/) for HTML/MHTML and [None](../exportheadersfootersmode/) for EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Controls how list labels are output to HTML, MHTML or EPUB. Default value is [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Specifies whether original URL should be used as the URL of the linked images. Default value is **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is **true** for HTML and **false** for MHTML and EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Controls whether [Shape](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Controls how text input form fields are saved to HTML or MHTML. Default value is **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When **true**, writes a DOCTYPE declaration in the document prior to the root element. Default value is **false**. When saving to EPUB or HTML5 ([Html5](../htmlversion/)) the DOCTYPE declaration is always written. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [get_HtmlVersion](./get_htmlversion/)() const | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [Png](../htmlmetafileformat/), meaning that metafiles are rendered to raster PNG images. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Specifies whether font family names used in the document are resolved and substituted according to [FontSettings](../../aspose.words/document/get_fontsettings/) when being written into HTML-based formats. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can be [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [All](../htmlelementsizeoutputmode/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [GetType](./gettype/)() const override |  |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the [Html](../../aspose.words/saveformat/) format. |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Initializes a new instance of this class that can be used to save a document in the [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/) format. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_CssSavingCallback](./get_csssavingcallback/). |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) |  |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentPartSavingCallback](./get_documentpartsavingcallback/). |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_EpubNavigationMapLevel](./set_epubnavigationmaplevel/)(int32_t) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_EpubNavigationMapLevel](./get_epubnavigationmaplevel/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is **false**. |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_FontSavingCallback](./get_fontsavingcallback/). |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ImageSavingCallback](./get_imagesavingcallback/). |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_MemoryOptimization](../saveoptions/get_memoryoptimization/). |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Setter for [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateFields](../saveoptions/get_updatefields/). |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Examples



Shows how to use a specific encoding when saving a document to .epub. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Use a SaveOptions object to specify the encoding for a document that we will save.
auto saveOptions = MakeObject<HtmlSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions->set_DocumentSplitCriteria(DocumentSplitCriteria::HeadingParagraph);

// Specify that we want to export document properties.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Shows how to specify the folder for storing linked images after saving to .html. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

String imagesDir = System::IO::Path::Combine(ArtifactsDir, u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```


Shows how to split a document into parts and save them. 
```cpp
void DocumentPartsFileNames()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");
    String outFileName = u"SavingCallback.DocumentPartsFileNames.html";

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    auto options = MakeObject<HtmlSaveOptions>();

    // If we save the document normally, there will be one output HTML
    // document with all the source document's contents.
    // Set the "DocumentSplitCriteria" property to "DocumentSplitCriteria.SectionBreak" to
    // save our document to multiple HTML files: one for each section.
    options->set_DocumentSplitCriteria(DocumentSplitCriteria::SectionBreak);

    // Assign a custom callback to the "DocumentPartSavingCallback" property to alter the document part saving logic.
    options->set_DocumentPartSavingCallback(MakeObject<ExSavingCallback::SavedDocumentPartRename>(outFileName, options->get_DocumentSplitCriteria()));

    // If we convert a document that contains images into html, we will end up with one html file which links to several images.
    // Each image will be in the form of a file in the local file system.
    // There is also a callback that can customize the name and file system location of each image.
    options->set_ImageSavingCallback(MakeObject<ExSavingCallback::SavedImageRename>(outFileName));

    doc->Save(ArtifactsDir + outFileName, options);
}

class SavedDocumentPartRename : public IDocumentPartSavingCallback
{
public:
    SavedDocumentPartRename(String outFileName, DocumentSplitCriteria documentSplitCriteria)
        : mCount(0), mDocumentSplitCriteria(((Aspose::Words::Saving::DocumentSplitCriteria)0))
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

private:
    int mCount;
    String mOutFileName;
    DocumentSplitCriteria mDocumentSplitCriteria;

    void DocumentPartSaving(SharedPtr<DocumentPartSavingArgs> args) override
    {
        // We can access the entire source document via the "Document" property.
        ASSERT_TRUE(args->get_Document()->get_OriginalFileName().EndsWith(u"Rendering.docx"));

        String partType = String::Empty;

        switch (mDocumentSplitCriteria)
        {
        case DocumentSplitCriteria::PageBreak:
            partType = u"Page";
            break;

        case DocumentSplitCriteria::ColumnBreak:
            partType = u"Column";
            break;

        case DocumentSplitCriteria::SectionBreak:
            partType = u"Section";
            break;

        case DocumentSplitCriteria::HeadingParagraph:
            partType = u"Paragraph from heading";
            break;

        default:
            break;
        }

        String partFileName = String::Format(u"{0} part {1}, of type {2}{3}", mOutFileName, ++mCount, partType,
                                             System::IO::Path::GetExtension(args->get_DocumentPartFileName()));

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output part file:
        args->set_DocumentPartFileName(partFileName);

        // 2 -  Create a custom stream for the output part file:
        args->set_DocumentPartStream(MakeObject<System::IO::FileStream>(ArtifactsDir + partFileName, System::IO::FileMode::Create));

        ASSERT_TRUE(args->get_DocumentPartStream()->get_CanWrite());
        ASSERT_FALSE(args->get_KeepDocumentPartStreamOpen());
    }
};

class SavedImageRename : public IImageSavingCallback
{
public:
    SavedImageRename(String outFileName) : mCount(0)
    {
        mOutFileName = outFileName;
    }

private:
    int mCount;
    String mOutFileName;

    void ImageSaving(SharedPtr<ImageSavingArgs> args) override
    {
        String imageFileName = String::Format(u"{0} shape {1}, of type {2}{3}", mOutFileName, ++mCount, args->get_CurrentShape()->get_ShapeType(),
                                              System::IO::Path::GetExtension(args->get_ImageFileName()));

        // Below are two ways of specifying where Aspose.Words will save each part of the document.
        // 1 -  Set a filename for the output image file:
        args->set_ImageFileName(imageFileName);

        // 2 -  Create a custom stream for the output image file:
        args->set_ImageStream(MakeObject<System::IO::FileStream>(ArtifactsDir + imageFileName, System::IO::FileMode::Create));

        ASSERT_TRUE(args->get_ImageStream()->get_CanWrite());
        ASSERT_TRUE(args->get_IsImageAvailable());
        ASSERT_FALSE(args->get_KeepImageStreamOpen());
    }
};
```

## See Also

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
