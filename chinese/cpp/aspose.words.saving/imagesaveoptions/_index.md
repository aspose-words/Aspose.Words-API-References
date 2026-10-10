---
title: "Aspose::Words::Saving::ImageSaveOptions 类"
linktitle: "ImageSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions 类。允许在将文档页面或形状渲染为图像时指定其他选项。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class


允许在将文档页面或形状渲染为图像时指定额外选项。欲了解更多，请访问 [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) 文档文章。

```cpp
class ImageSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 创建此对象的深度克隆。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | 创建一个适用于指定保存格式的保存选项对象。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | 创建一个适用于给定文件名中指定的文件扩展名的保存选项对象。 |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | 获取或设置一个布尔值，指示在文档保存时是否允许在嵌入 TrueType 字体时嵌入带有 PostScript 描边的字体。默认值为 **false**。 |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | 获取决定颜色呈现方式的值。 |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | 获取或设置默认模板的路径（包括文件名）。此属性的默认值为 **empty string**。 |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 获取决定 3D 效果渲染方式的值。 |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | 获取或设置决定 DrawingML 效果渲染方式的值。 |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | 获取或设置决定 DrawingML 形状渲染方式的值。 |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | 当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。 |
| [get_GraphicsQualityOptions](./get_graphicsqualityoptions/)() const | 允许为 **Graphics** 对象指定渲染模式和质量。 |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | 获取或设置生成图像的水平分辨率（单位为每英寸点数）。 |
| [get_ImageBrightness](./get_imagebrightness/)() const | 获取或设置生成图像的亮度。 |
| [get_ImageColorMode](./get_imagecolormode/)() const | 获取或设置生成图像的颜色模式。 |
| [get_ImageContrast](./get_imagecontrast/)() const | 获取或设置生成图像的对比度。 |
| [get_ImageSize](./get_imagesize/)() const | 获取或设置生成图像的大小（像素）。 |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | 获取或设置决定墨水 (InkML) 对象渲染方式的值。 |
| [get_JpegQuality](./get_jpegquality/)() | 获取或设置决定生成 JPEG 图像质量的值。 |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | 获取或设置决定 Html 文档中 JPEG 图像质量的值。 |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | 获取决定在保存文档之前是否执行内存优化的值。此属性的默认值为 **false**。 |
| [get_MetafileRenderingOptions](./get_metafilerenderingoptions/)() | 允许指定在渲染输出中如何处理元文件。 |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | 允许指定元文件渲染选项。 |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | 获取用于数字渲染的 [NumeralFormat](../numeralformat/)。默认使用欧洲数字。 |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | 标志指示是否需要优化输出。如果设置此标志，将移除冗余的嵌套画布和空画布，并且相邻具有相同格式的字形会被合并。注意：如果此属性设置为 **true**，内容显示的准确性可能受到影响。默认是 **false**。 |
| [get_PageLayout](./get_pagelayout/)() const | 获取或设置在将多个页面渲染为单个输出时使用的布局。 |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | 允许控制文档导出为固定页面格式时各个页面的保存方式。 |
| [get_PageSet](./get_pageset/)() | 获取或设置要渲染的页面。默认是文档中的所有页面。 |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | 获取或设置要渲染的页面。默认是文档中的所有页面。 |
| [get_PaperColor](./get_papercolor/)() | 获取或设置生成图像的背景（纸张）颜色。默认值为 **White**。 |
| [get_PixelFormat](./get_pixelformat/)() const | 获取或设置生成图像的像素格式。 |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | 当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。 |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | 在保存文档期间调用，并接受有关保存进度的数据。 |
| [get_SaveFormat](./get_saveformat/)() override | 指定如果使用此保存选项对象，渲染的文档页面或形状将以何种格式保存。可以是栅格 [Tiff](../../aspose.words/saveformat/)、[Png](../../aspose.words/saveformat/)、[Bmp](../../aspose.words/saveformat/)、[Jpeg](../../aspose.words/saveformat/) 或矢量 [Emf](../../aspose.words/saveformat/)、[Eps](../../aspose.words/saveformat/)、[WebP](../)、[Svg](../../aspose.words/saveformat/)。 |
| [get_Scale](./get_scale/)() const | 获取或设置 Floyd‑Steinberg 方法中二值化误差阈值。当 [ImageBinarizationMethod](../imagebinarizationmethod/) 为 [FloydSteinbergDithering](../imagebinarizationmethod/) 时。 |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | 指定在保存为 DOC 或 DOCX 文件时使用的临时文件夹。默认情况下，此属性为 **null**，且不使用临时文件。 |
| [get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/)() const | 获取或设置在将图像转换为 1 bpp 格式时使用的方法，当 [SaveFormat](./get_saveformat/) 为 [Tiff](../../aspose.words/saveformat/) 且 [TiffCompression](./get_tiffcompression/) 等于 [Ccitt3](../tiffcompression/) 或 [Ccitt4](../tiffcompression/) 时。 |
| [get_TiffBinarizationMethod](./get_tiffbinarizationmethod/)() const | 获取或设置保存生成图像为 TIFF 格式时要应用的压缩类型。 |
| [get_TiffCompression](./get_tiffcompression/)() const | 获取或设置决定在保存为 EMF 时使用 GDI+ 还是 Aspose.Words 元文件渲染器的值。 |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | 确定字体属性是否会根据所使用的字符代码进行更改。 |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) 属性的值。默认值为 **false**；。 |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | 获取决定在将文档保存为固定页面格式之前是否应更新某些类型字段的值。此属性的默认值为 **true**。 |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | 获取或设置决定在保存前是否更新 [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) 属性的值。 |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) 属性的值。 |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | 获取一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | 获取或设置一个值，用于确定是否在渲染时使用抗锯齿。 |
| [get_UseGdiEmfRenderer](./get_usegdiemfrenderer/)() const | 获取或设置生成图像的垂直分辨率（单位为每英寸点数）。 |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | 获取或设置一个值，用于确定是否使用高质量（即慢速）的渲染算法。 |
| [get_VerticalResolution](./get_verticalresolution/)() const | 初始化此类的新实例，可用于将渲染的图像保存为 [Tiff](../../aspose.words/saveformat/)、[Png](../../aspose.words/saveformat/)、[Bmp](../../aspose.words/saveformat/)、[Jpeg](../../aspose.words/saveformat/)、[Emf](../../aspose.words/saveformat/)、[Eps](../../aspose.words/saveformat/)、[WebP](../) 或 [Svg](../../aspose.words/saveformat/) 格式。 |
| [GetType](./gettype/)() const override |  |
| [ImageSaveOptions](./imagesaveoptions/)(Aspose::Words::SaveFormat) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_GraphicsQualityOptions](./get_graphicsqualityoptions/) 的 Setter。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) 的 setter。 |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | 设置决定颜色呈现方式的值。 |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) 的 setter。 |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) 的 setter。 |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 设置一个值，用于确定 3D 效果的渲染方式。 |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/) 的 setter。 |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/) 的 setter。 |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/) 的 setter。 |
| [set_GraphicsQualityOptions](./set_graphicsqualityoptions/)(const System::SharedPtr\<Aspose::Words::Saving::GraphicsQualityOptions\>\&) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_HorizontalResolution](./get_horizontalresolution/) 的 Setter。 |
| [set_HorizontalResolution](./set_horizontalresolution/)(float) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_ImageBrightness](./get_imagebrightness/) 的 Setter。 |
| [set_ImageBrightness](./set_imagebrightness/)(float) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode](./get_imagecolormode/) 的 Setter。 |
| [set_ImageColorMode](./set_imagecolormode/)(Aspose::Words::Saving::ImageColorMode) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_ImageContrast](./get_imagecontrast/) 的 Setter。 |
| [set_ImageContrast](./set_imagecontrast/)(float) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_ImageSize](./get_imagesize/) 的 Setter。 |
| [set_ImageSize](./set_imagesize/)(System::Drawing::Size) | 用于 [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/) 的 Setter。 |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)。 |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality](./get_jpegquality/)。 |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | 设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为 **false**。 |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | 允许指定元文件渲染选项。 |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | 设置用于数字渲染的 [NumeralFormat](../numeralformat/)。默认使用欧洲数字。 |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | 用于设置 [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) 的 setter。 |
| [set_PageLayout](./set_pagelayout/)(const System::SharedPtr\<Aspose::Words::Saving::MultiPageLayout\>\&) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_PageLayout](./get_pagelayout/) 的 setter。 |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | 允许控制文档导出为固定页面格式时各个页面的保存方式。 |
| [set_PageSet](./set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_PageSet](./get_pageset/) 的 setter。 |
| [set_PaperColor](./set_papercolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_PaperColor](./get_papercolor/) 的 setter。 |
| [set_PixelFormat](./set_pixelformat/)(Aspose::Words::Saving::ImagePixelFormat) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_PixelFormat](./get_pixelformat/) 的 setter。 |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/)。 |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/) 的 setter。 |
| [set_Resolution](./set_resolution/)(float) | 设置生成图像的水平和垂直分辨率，单位为每英寸点数（dpi）。 |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat](./get_saveformat/) 的 setter。 |
| [set_Scale](./set_scale/)(float) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_Scale](./get_scale/) 的 setter。 |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/) 的 setter。 |
| [set_ThresholdForFloydSteinbergDithering](./set_thresholdforfloydsteinbergdithering/)(uint8_t) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering](./get_thresholdforfloydsteinbergdithering/) 的 setter。 |
| [set_TiffBinarizationMethod](./set_tiffbinarizationmethod/)(Aspose::Words::Saving::ImageBinarizationMethod) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_TiffBinarizationMethod](./get_tiffbinarizationmethod/) 的 setter。 |
| [set_TiffCompression](./set_tiffcompression/)(Aspose::Words::Saving::TiffCompression) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_TiffCompression](./get_tiffcompression/) 的 setter。 |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/) 的 setter。 |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/) 的 setter。 |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | 设置一个值，用于确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为 **true**。 |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/) 的 setter。 |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/) 的 setter。 |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | 设置一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/) 的 setter。 |
| [set_UseGdiEmfRenderer](./set_usegdiemfrenderer/)(bool) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer](./get_usegdiemfrenderer/) 的 setter。 |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/) 的 setter。 |
| [set_VerticalResolution](./set_verticalresolution/)(float) | 用于设置 [Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution](./get_verticalresolution/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



将 Word 文档的页面渲染为具有透明或彩色背景的图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// 将 "PaperColor" 属性设置为透明颜色，以应用透明
// 背景到文档，在将其渲染为图像时。
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// 将 "PaperColor" 属性设置为不透明颜色，以应用该颜色
// 作为文档的背景，在我们将其渲染为图像时。
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```


展示如何在将文档保存为 JPEG 时配置压缩。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// 将 "JpegQuality" 属性设置为 "10"，以在渲染文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像会出现更明显的压缩伪影。
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// 将 "JpegQuality" 属性设置为 "100"，以在渲染文档时使用较弱的压缩。
// 这将提升图像质量，但会导致文件大小增加。
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```


展示如何在将文档渲染为 PNG 时指定分辨率。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// 将 "Resolution" 属性设置为 "72"，以 72dpi 渲染文档。
options->set_Resolution(72.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.72dpi.png", options);

// 将 "Resolution" 属性设置为 "300"，以 300dpi 渲染文档。
options->set_Resolution(300.0f);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Resolution.300dpi.png", options);
```

## 另见

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
