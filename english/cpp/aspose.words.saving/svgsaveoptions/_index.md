---
title: Aspose::Words::Saving::SvgSaveOptions class
linktitle: SvgSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::SvgSaveOptions class. Can be used to specify additional options when saving a document into the Svg format. To learn more, visit the  documentation article in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class


Can be used to specify additional options when saving a document into the [Svg](../../aspose.words/saveformat/) format. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class SvgSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Gets or sets a value determining how colors are rendered. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const |  |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Specified whether images should be embedded into SVG document as base64. Note setting this flag can significantly increase size of output SVG file. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_FitToViewPort](./get_fittoviewport/)() const | Specifies if the output SVG should fill the available viewport area (browser window or container). When set to **true** width and height of output SVG are set to 100%. The default value is **false**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Gets or sets a value determining the quality of the JPEG images inside Html document. |
| [get_MaxImageResolution](./get_maximageresolution/)() const |  |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Allows to specify metafile rendering options. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **false**. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Gets or sets the pages to render. Default is all the pages in the document. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Allows to control how resources (images) are saved when a document is exported to SVG format. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Specifies the name of the folder used to construct image URIs written into an SVG document. Default is **null**. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the document will be saved if this save options object is used. Can only be [Svg](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Controls whether a border is added to the outline of the page. Default is **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used. |
| [get_TextOutputMode](./get_textoutputmode/)() const | Gets or sets a value determining how text should be rendered in SVG. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_ColorMode](../fixedpagesaveoptions/get_colormode/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) |  |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FitToViewPort](./set_fittoviewport/)(bool) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort](./get_fittoviewport/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MaxImageResolution](./set_maximageresolution/)(int32_t) |  |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_MemoryOptimization](../saveoptions/get_memoryoptimization/). |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/). |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/). |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_ResourceSavingCallback](./get_resourcesavingcallback/). |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder](./get_showpageborder/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextOutputMode](./set_textoutputmode/)(Aspose::Words::Saving::SvgTextOutputMode) | Setter for [Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode](./get_textoutputmode/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateFields](../saveoptions/get_updatefields/). |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [SvgSaveOptions](./svgsaveoptions/)() |  |
| static [Type](./type/)() |  |

## Examples



Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg. 
```cpp
void SvgResourceFolder()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    auto options = MakeObject<SvgSaveOptions>();
    options->set_SaveFormat(SaveFormat::Svg);
    options->set_ExportEmbeddedImages(false);
    options->set_ResourcesFolder(ArtifactsDir + u"SvgResourceFolder");
    options->set_ResourcesFolderAlias(ArtifactsDir + u"SvgResourceFolderAlias");
    options->set_ShowPageBorder(false);
    options->set_ResourceSavingCallback(MakeObject<ExSvgSaveOptions::ResourceUriPrinter>());

    System::IO::Directory::CreateDirectory_(options->get_ResourcesFolderAlias());

    doc->Save(ArtifactsDir + u"SvgSaveOptions.SvgResourceFolder.svg", options);
}

class ResourceUriPrinter : public IResourceSavingCallback
{
public:
    ResourceUriPrinter() : mSavedResourceCount(0)
    {
    }

private:
    int mSavedResourceCount;

    void ResourceSaving(SharedPtr<ResourceSavingArgs> args) override
    {
        std::cout << "Resource #" << ++mSavedResourceCount << " \"" << args->get_ResourceFileName() << "\"" << std::endl;
        std::cout << (String(u"\t") + args->get_ResourceFileUri()) << std::endl;
    }
};
```

## See Also

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
