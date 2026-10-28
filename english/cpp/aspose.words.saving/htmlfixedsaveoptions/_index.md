---
title: Aspose::Words::Saving::HtmlFixedSaveOptions class
linktitle: HtmlFixedSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions class. Can be used to specify additional options when saving a document into the HtmlFixed format. To learn more, visit the Specify Save Options documentation article in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Can be used to specify additional options when saving a document into the [HtmlFixed](../../aspose.words/saveformat/) format. 
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class HtmlFixedSaveOptions : public FixedPageSaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| static [Type](./type/)() |  |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Specifies prefix which is added to all class names in style.css file. Default value is **"aw"**. |
| [get_Encoding](./get_encoding/)() const | Specifies the encoding to use when exporting to HTML. Default value is **new UTF8Encoding(true)** (UTF-8 with BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Specifies whether SVG resources should be embedded into Html document. Default value is **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [get_FontFormat](./get_fontformat/)() const | Gets or sets [ExportFontFormat](../exportfontformat/) used for font exporting. Default value is [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Specifies the horizontal alignment of pages in an HTML document. Default value is [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Specifies whether JavaScript will be removed from links. Default is **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Specifies the name of the folder used to construct image URIs written into an Html document. Default is **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [ExportEmbeddedCss](./get_exportembeddedcss/) is **false**). Default value is **false**, all CSS rules are written into single file "styles.css". |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Specifies whether border around pages should be shown. Default is **true**. |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to **true**, [FontFormat](./get_fontformat/) and [ExportEmbeddedFonts](./get_exportembeddedfonts/) properties do not have effect, also [ResourceSavingCallback](./get_resourcesavingcallback/) is not fired for fonts. Default is **false**. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String \&) | Specifies prefix which is added to all class names in style.css file. Default value is **"aw"**. |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\> \&) | Specifies the encoding to use when exporting to HTML. Default value is **new UTF8Encoding(true)** (UTF-8 with BOM). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Specifies whether SVG resources should be embedded into Html document. Default value is **true**. |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Sets [ExportFontFormat](../exportfontformat/) used for font exporting. Default value is [Woff](../exportfontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String \&) | Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **true**. |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Specifies the horizontal alignment of pages in an HTML document. Default value is [Center](../htmlfixedpagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points. |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Specifies whether JavaScript will be removed from links. Default is **false**. |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\> \&) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String \&) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is **null**. |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String \&) | Specifies the name of the folder used to construct image URIs written into an Html document. Default is **null**. |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [ExportEmbeddedCss](./get_exportembeddedcss/) is **false**). Default value is **false**, all CSS rules are written into single file "styles.css". |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Specifies the format in which the document will be saved if this save options object is used. Can only be [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Specifies whether border around pages should be shown. Default is **true**. |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to **true**, [FontFormat](./get_fontformat/) and [ExportEmbeddedFonts](./get_exportembeddedfonts/) properties do not have effect, also [ResourceSavingCallback](./get_resourcesavingcallback/) is not fired for fonts. Default is **false**. |
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
