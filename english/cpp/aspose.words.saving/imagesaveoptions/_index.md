---
title: Aspose::Words::Saving::ImageSaveOptions class
linktitle: ImageSaveOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions class. Allows to specify additional options when rendering document pages or shapes to images. To learn more, visit the  documentation article in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class


Allows to specify additional options when rendering document pages or shapes to images. To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) documentation article.

```cpp
class ImageSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Creates a deep clone of this object. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Creates a save options object of a class suitable for the specified save format. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Creates a save options object of a class suitable for the file extension specified in the given file name. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Determines whether the specified object is equal in value to the current object. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Gets a value determining how colors are rendered. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Gets or sets custom local time zone used for date/time fields. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Gets or sets path to default template (including filename). Default value for this property is **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Gets a value determining how 3D effects are rendered. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Gets or sets a value determining how DrawingML effects are rendered. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Gets or sets a value determining how DrawingML shapes are rendered. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | When **true**, causes the name and version of Aspose.Words to be embedded into produced files. Default value is **true**. |
| [get_GraphicsQualityOptions](./get_graphicsqualityoptions/)() const | Allows to specify rendering mode and quality for the **Graphics** object. |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | Gets or sets the horizontal resolution for the generated images, in dots per inch. |
| [get_ImageBrightness](./get_imagebrightness/)() const | Gets or sets the brightness for the generated images. |
| [get_ImageColorMode](./get_imagecolormode/)() const | Gets or sets the color mode for the generated images. |
| [get_ImageContrast](./get_imagecontrast/)() const | Gets or sets the contrast for the generated images. |
| [get_ImageSize](./get_imagesize/)() const | Gets or sets the size of a generated image in pixels. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Gets or sets a value determining how ink (InkML) objects are rendered. |
| [get_JpegQuality](./get_jpegquality/)() | Gets or sets a value determining the quality of the generated JPEG images. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Gets or sets a value determining the quality of the JPEG images inside Html document. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Gets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [get_MetafileRenderingOptions](./get_metafilerenderingoptions/)() | Allows to specify how metafiles are treated in the rendered output. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Allows to specify metafile rendering options. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Gets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to **true**. Default is **false**. |
| [get_PageLayout](./get_pagelayout/)() const | Gets or sets the layout used when rendering multiple pages into a single output. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [get_PageSet](./get_pageset/)() | Gets or sets the pages to render. Default is all the pages in the document. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Gets or sets the pages to render. Default is all the pages in the document. |
| [get_PaperColor](./get_papercolor/)() | Gets or sets the background (paper) color for the generated images. The default value is **White**. |
| [get_PixelFormat](./get_pixelformat/)() const | Gets or sets the pixel format for the generated images. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | When **true**, pretty formats output where applicable. Default value is **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Called during saving a document and accepts data about saving progress. |
| [get_SaveFormat](./get_saveformat/)() override | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/) or vector [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../), [Svg](../../aspose.words/saveformat/). |
| [get_Scale](./get_scale/)() const | Gets or sets the zoom factor for the generated images. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is **null** and no temporary files are used. |
| [get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/)() const | Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../imagebinarizationmethod/) is [FloydSteinbergDithering](../imagebinarizationmethod/). |
| [get_TiffBinarizationMethod](./get_tiffbinarizationmethod/)() const | Gets or sets method used while converting images to 1 bpp format when [SaveFormat](./get_saveformat/) is [Tiff](../../aspose.words/saveformat/) and [TiffCompression](./get_tiffcompression/) is equal to [Ccitt3](../tiffcompression/) or [Ccitt4](../tiffcompression/). |
| [get_TiffCompression](./get_tiffcompression/)() const | Gets or sets the type of compression to apply when saving generated images to the TIFF format. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Determines whether the font attributes will be changed according to the character code being used. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Gets or sets a value determining whether the [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) property is updated before saving. Default value is **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Gets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Gets or sets a value determining whether the [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) property is updated before saving. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Gets or sets a value determining whether the [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) property is updated before saving. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Gets or sets a value determining whether or not to use anti-aliasing for rendering. |
| [get_UseGdiEmfRenderer](./get_usegdiemfrenderer/)() const | Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms. |
| [get_VerticalResolution](./get_verticalresolution/)() const | Gets or sets the vertical resolution for the generated images, in dots per inch. |
| [GetType](./gettype/)() const override |  |
| [ImageSaveOptions](./imagesaveoptions/)(Aspose::Words::SaveFormat) | Initializes a new instance of this class that can be used to save rendered images in the [Tiff](../../aspose.words/saveformat/), [Png](../../aspose.words/saveformat/), [Bmp](../../aspose.words/saveformat/), [Jpeg](../../aspose.words/saveformat/), [Emf](../../aspose.words/saveformat/), [Eps](../../aspose.words/saveformat/), [WebP](../) or [Svg](../../aspose.words/saveformat/) format. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Sets a value determining how colors are rendered. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Sets a value determining how 3D effects are rendered. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_GraphicsQualityOptions](./set_graphicsqualityoptions/)(const System::SharedPtr\<Aspose::Words::Saving::GraphicsQualityOptions\>\&) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_GraphicsQualityOptions](./get_graphicsqualityoptions/). |
| [set_HorizontalResolution](./set_horizontalresolution/)(float) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution](./get_horizontalresolution/). |
| [set_ImageBrightness](./set_imagebrightness/)(float) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness](./get_imagebrightness/). |
| [set_ImageColorMode](./set_imagecolormode/)(Aspose::Words::Saving::ImageColorMode) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode](./get_imagecolormode/). |
| [set_ImageContrast](./set_imagecontrast/)(float) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast](./get_imagecontrast/). |
| [set_ImageSize](./set_imagesize/)(System::Drawing::Size) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_ImageSize](./get_imagesize/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Setter for [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Sets value determining if memory optimization should be performed before saving the document. Default value for this property is **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Allows to specify metafile rendering options. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default. |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Setter for [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(const System::SharedPtr\<Aspose::Words::Saving::MultiPageLayout\>\&) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_PageLayout](./get_pagelayout/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Allows to control how separate pages are saved when a document is exported to fixed page format. |
| [set_PageSet](./set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_PageSet](./get_pageset/). |
| [set_PaperColor](./set_papercolor/)(System::Drawing::Color) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_PaperColor](./get_papercolor/). |
| [set_PixelFormat](./set_pixelformat/)(Aspose::Words::Saving::ImagePixelFormat) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat](./get_pixelformat/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_Resolution](./set_resolution/)(float) | Sets both horizontal and vertical resolution for the generated images, in dots per inch. |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_Scale](./set_scale/)(float) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_Scale](./get_scale/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Setter for [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_ThresholdForFloydSteinbergDithering](./set_thresholdforfloydsteinbergdithering/)(uint8_t) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/). |
| [set_TiffBinarizationMethod](./set_tiffbinarizationmethod/)(Aspose::Words::Saving::ImageBinarizationMethod) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod](./get_tiffbinarizationmethod/). |
| [set_TiffCompression](./set_tiffcompression/)(Aspose::Words::Saving::TiffCompression) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression](./get_tiffcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseGdiEmfRenderer](./set_usegdiemfrenderer/)(bool) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer](./get_usegdiemfrenderer/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Setter for [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_VerticalResolution](./set_verticalresolution/)(float) | Setter for [Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution](./get_verticalresolution/). |
| static [Type](./type/)() |  |

## Examples



Renders a page of a Word document into an image with transparent or colored background. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Set the "PaperColor" property to a transparent color to apply a transparent
// background to the document while rendering it to an image.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Set the "PaperColor" property to an opaque color to apply that color
// as the background of the document as we render it to an image.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```


Shows how to configure compression while saving a document as a JPEG. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Set the "JpegQuality" property to "10" to use stronger compression when rendering the document.
// This will reduce the file size of the document, but the image will display more prominent compression artifacts.
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// Set the "JpegQuality" property to "100" to use weaker compression when rending the document.
// This will improve the quality of the image at the cost of an increased file size.
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```


Shows how to specify a resolution while rendering a document to PNG. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Set the "Resolution" property to "72" to render the document in 72dpi.
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// Set the "Resolution" property to "300" to render the document in 300dpi.
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## See Also

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
