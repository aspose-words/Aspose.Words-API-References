---
title: Aspose::Words::Saving::HtmlSaveOptions class
linktitle: HtmlSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions class. Can be used to specify additional options when saving a document into the Html, Mhtml, Epub, Azw3 or Mobi format. To learn more, visit the Specify Save Options documentation article in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Can be used to specify additional options when saving a document into the [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/) format. 
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class HtmlSaveOptions : public SaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Initializes a new instance of this class that can be used to save a document in the [Html](../../aspose.words/saveformat/) format. |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Initializes a new instance of this class that can be used to save a document in the [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/) format. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [Inline](../cssstylesheettype/) for HTML/MHTML and [External](../cssstylesheettype/) for EPUB. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Specifies how the document should be split when saving to [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) or [Azw3](../../aspose.words/saveformat/) format. Default is [None](../documentsplitcriteria/) for HTML and [HeadingParagraph](../documentsplitcriteria/) for EPUB and AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Specifies the maximum level of headings at which to split the document. Default value is **2**. |
| [get_Encoding](./get_encoding/)() const | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is **new UTF8Encoding(false)** (UTF-8 without BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Controls how drop-down form fields are saved to HTML or MHTML. Default value is **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is **false**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [PerSection](../exportheadersfootersmode/) for HTML/MHTML and [None](../exportheadersfootersmode/) for EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Controls how list labels are output to HTML, MHTML or EPUB. Default value is [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Specifies whether original URL should be used as the URL of the linked images. Default value is **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is **true** for HTML and **false** for MHTML and EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() | Controls whether [Shape](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Controls how text input form fields are saved to HTML or MHTML. Default value is **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When **true**, writes a DOCTYPE declaration in the document prior to the root element. Default value is **false**. When saving to EPUB or HTML5 ([Html5](../htmlversion/)) the DOCTYPE declaration is always written. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is **0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [get_HtmlVersion](./get_htmlversion/)() const | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is **96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [get_MetafileFormat](./get_metafileformat/)() | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [Png](../htmlmetafileformat/), meaning that metafiles are rendered to raster PNG images. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is **3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [Image](../htmlofficemathoutputmode/). |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Specifies whether JavaScript will be removed from links. Default is **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Specifies whether backslash characters should be replaced with yen signs. Default value is **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Specifies whether font family names used in the document are resolved and substituted according to [FontSettings](../../aspose.words/document/get_fontsettings/) when being written into HTML-based formats. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can be [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [All](../htmlelementsizeoutputmode/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Specifies whether negative left and right indents of paragraphs are normalized when saving to HTML, MHTML or EPUB. Default value is **false**. |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String \&) | Specifies a prefix which is added to all CSS class names. Default value is an empty string and generated CSS class names have no common prefix. |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\> \&) | Allows to control how CSS styles are saved when a document is saved to HTML, MHTML or EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String \&) | Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string. |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Specifies how CSS (Cascading Style Sheet) styles are exported to HTML, MHTML or EPUB. Default value is [Inline](../cssstylesheettype/) for HTML/MHTML and [External](../cssstylesheettype/) for EPUB. |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\> \&) | Allows to control how document parts are saved when a document is saved to HTML or EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Specifies how the document should be split when saving to [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) or [Azw3](../../aspose.words/saveformat/) format. Default is [None](../documentsplitcriteria/) for HTML and [HeadingParagraph](../documentsplitcriteria/) for EPUB and AZW3. |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Specifies the maximum level of headings at which to split the document. Default value is **2**. |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\> \&) | Specifies the encoding to use when exporting to HTML, MHTML or EPUB. Default value is **new UTF8Encoding(false)** (UTF-8 without BOM). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Specifies whether to use CID (Content-ID) URLs to reference resources (images, fonts, CSS) included in MHTML documents. Default value is **false**. |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Specifies whether to export built-in and custom document properties to HTML, MHTML or EPUB. Default value is **false**. |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Controls how drop-down form fields are saved to HTML or MHTML. Default value is **false**. |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is **false**. |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Specifies how headers and footers are output to HTML, MHTML or EPUB. Default value is [PerSection](../exportheadersfootersmode/) for HTML/MHTML and [None](../exportheadersfootersmode/) for EPUB. |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Specifies whether language information is exported to HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Controls how list labels are output to HTML, MHTML or EPUB. Default value is [Auto](../exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Specifies whether original URL should be used as the URL of the linked images. Default value is **false**. |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Specifies whether page margins is exported to HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is **false**. |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is **true** for HTML and **false** for MHTML and EPUB. |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Controls whether [Shape](../../aspose.words.drawing/shape/) nodes are converted to SVG images when saving to HTML, MHTML, EPUB or AZW3. Default value is **false**. |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Controls how text input form fields are saved to HTML or MHTML. Default value is **false**. |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is **false**. |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Specifies whether to write the DOCTYPE declaration when saving to HTML or MHTML. When **true**, writes a DOCTYPE declaration in the document prior to the root element. Default value is **false**. When saving to EPUB or HTML5 ([Html5](../htmlversion/)) the DOCTYPE declaration is always written. |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is **0**. |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\> \&) | Allows to control how fonts are saved when a document is saved to HTML, MHTML or EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String \&) | Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string. |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String \&) | Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string. |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Specifies version of HTML standard that should be used when saving the document to HTML or MHTML. Default value is [Xhtml](../htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Specifies the output resolution for images when exporting to HTML, MHTML or EPUB. Default is **96 dpi**. |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\> \&) | Allows to control how images are saved when a document is saved to HTML, MHTML or EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String \&) | Specifies the physical folder where images are saved when exporting a document to HTML format. Default is an empty string. |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String \&) | Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Specifies in what format metafiles are saved when exporting to HTML, MHTML, or EPUB. Default value is [Png](../htmlmetafileformat/), meaning that metafiles are rendered to raster PNG images. |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats. Default value is **3**. |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Controls how OfficeMath objects are exported to HTML, MHTML or EPUB. Default value is [Image](../htmlofficemathoutputmode/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Specifies whether JavaScript will be removed from links. Default is **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Specifies whether backslash characters should be replaced with yen signs. Default value is **false**. |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Specifies whether font family names used in the document are resolved and substituted according to [FontSettings](../../aspose.words/document/get_fontsettings/) when being written into HTML-based formats. |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String \&) | Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML. Default is an empty string. |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String \&) | Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifies the format in which the document will be saved if this save options object is used. Can be [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) or [Mobi](../../aspose.words/saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Specifies whether images are scaled by Aspose.Words to the bounding shape size when exporting to HTML, MHTML or EPUB. Default value is **true**. |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [All](../htmlelementsizeoutputmode/). |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String \&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
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
## Examples


Shows how to use a specific encoding when saving a document to .epub.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

// Use a SaveOptions object to specify the encoding for a document that we will save.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// By default, an output .epub document will have all its contents in one HTML part.
// A split criterion allows us to segment the document into several HTML parts.
// We will set the criteria to split the document into heading paragraphs.
// This is useful for readers who cannot read HTML files more significant than a specific size.
saveOptions->set_DocumentSplitCriteria(DocumentSplitCriteria::HeadingParagraph);

// Specify that we want to export document properties.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Shows how to specify the folder for storing linked images after saving to .html.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Set an option to export form fields as plain text instead of HTML input elements.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```
## See Also

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
