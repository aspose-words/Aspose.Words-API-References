---
title: "Aspose::Words::Saving::SvgSaveOptions 类"
linktitle: "SvgSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions 类。可用于在将文档保存为 Svg 格式时指定其他选项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class


可用于在将文档保存为 [Svg](../../aspose.words/saveformat/) 格式时指定其他选项。要了解更多信息，请访问 [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) 文档文章。

```cpp
class SvgSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
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
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | 指定是否应将图像以 base64 形式嵌入 SVG 文档。请注意，启用此选项可能会导致输出 SVG 文件的大小显著增加。 |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | 当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。 |
| [get_FitToViewPort](./get_fittoviewport/)() const | 指定输出 SVG 是否应填满可用的视口区域（浏览器窗口或容器）。设置为 **true** 时，输出 SVG 的宽度和高度将设为 100%。默认值为 **false**。 |
| [get_IdPrefix](./get_idprefix/)() const | 指定一个前缀，该前缀会预先添加到输出文档中所有生成的元素 ID 前。默认值为 null，且不添加前缀。 |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | 获取或设置决定墨水 (InkML) 对象渲染方式的值。 |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | 获取或设置决定 Html 文档中 JPEG 图像质量的值。 |
| [get_MaxImageResolution](./get_maximageresolution/)() const | 获取或设置以每英寸像素为单位的值，用于限制导出栅格图像的分辨率。默认值为零。 |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | 获取决定在保存文档之前是否执行内存优化的值。此属性的默认值为 **false**。 |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | 允许指定元文件渲染选项。 |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | 获取用于数字渲染的 [NumeralFormat](../numeralformat/)。默认使用欧洲数字。 |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | 标志指示是否需要优化输出。如果设置此标志，将移除冗余的嵌套画布和空画布，并且相邻具有相同格式的字形会被合并。注意：如果此属性设置为 **true**，内容显示的准确性可能受到影响。默认是 **false**。 |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | 允许控制文档导出为固定页面格式时各个页面的保存方式。 |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | 获取或设置要渲染的页面。默认是文档中的所有页面。 |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | 当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。 |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | 在保存文档期间调用，并接受有关保存进度的数据。 |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | 指定是否从链接中移除 JavaScript。默认值为 **false**。如果启用此选项，所有包含 JavaScript 的链接将被替换为 "javascript:void(0)"。 |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | 允许控制在将文档导出为 SVG 格式时资源（图像）的保存方式。 |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | 指定在将文档导出为 Svg 格式时资源（图像）保存的物理文件夹。默认值为 **null**。 |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | 指定用于构建写入 SVG 文档的图像 URI 的文件夹名称。默认值为 **null**。 |
| [get_SaveFormat](./get_saveformat/)() override | 指定如果使用此保存选项对象，文档将保存的格式。只能是 [Svg](../../aspose.words/saveformat/)。 |
| [get_ShowPageBorder](./get_showpageborder/)() const | 控制是否在页面轮廓添加边框。默认值为 **true**。 |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | 指定在保存为 DOC 或 DOCX 文件时使用的临时文件夹。默认情况下，此属性为 **null**，且不使用临时文件。 |
| [get_TextOutputMode](./get_textoutputmode/)() const | 获取或设置决定文本在 SVG 中如何呈现的值。 |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | 确定字体属性是否会根据所使用的字符代码进行更改。 |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) 属性的值。默认值为 **false**；。 |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | 获取决定在将文档保存为固定页面格式之前是否应更新某些类型字段的值。此属性的默认值为 **true**。 |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | 获取或设置决定在保存前是否更新 [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) 属性的值。 |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) 属性的值。 |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | 获取一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | 获取或设置一个值，用于确定是否在渲染时使用抗锯齿。 |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | 获取或设置一个值，用于确定是否使用高质量（即慢速）的渲染算法。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) 的 setter。 |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | 设置决定颜色呈现方式的值。 |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) 的 setter。 |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) 的 setter。 |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 设置一个值，用于确定 3D 效果的渲染方式。 |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/) 的 setter。 |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/) 的 setter。 |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | 指定是否应将图像以 base64 形式嵌入 SVG 文档。请注意，启用此选项可能会导致输出 SVG 文件的大小显著增加。 |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/) 的 setter。 |
| [set_FitToViewPort](./set_fittoviewport/)(bool) | 用于设置 [Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort](./get_fittoviewport/) 的 setter。 |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SvgSaveOptions::get_IdPrefix](./get_idprefix/) 的 setter。 |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)。 |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | 用于设置 [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/) 的 setter。 |
| [set_MaxImageResolution](./set_maximageresolution/)(int32_t) | 用于设置 [Aspose::Words::Saving::SvgSaveOptions::get_MaxImageResolution](./get_maximageresolution/) 的 setter。 |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | 设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为 **false**。 |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | 允许指定元文件渲染选项。 |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | 设置用于数字渲染的 [NumeralFormat](../numeralformat/)。默认使用欧洲数字。 |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | 用于设置 [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) 的 setter。 |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | 允许控制文档导出为固定页面格式时各个页面的保存方式。 |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | 用于设置 [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/) 的 setter。 |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/)。 |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/) 的 setter。 |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | 设置 [Aspose::Words::Saving::SvgSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)。 |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | 允许控制在将文档导出为 SVG 格式时资源（图像）的保存方式。 |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | 设置 [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder](./get_resourcesfolder/)。 |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | 设置 [Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/)。 |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | 指定如果使用此保存选项对象，文档将保存的格式。只能是 [Svg](../../aspose.words/saveformat/)。 |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | 设置 [Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder](./get_showpageborder/)。 |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/) 的 setter。 |
| [set_TextOutputMode](./set_textoutputmode/)(Aspose::Words::Saving::SvgTextOutputMode) | 设置 [Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode](./get_textoutputmode/)。 |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/) 的 setter。 |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/) 的 setter。 |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | 设置一个值，用于确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为 **true**。 |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/) 的 setter。 |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/) 的 setter。 |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | 设置一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/) 的 setter。 |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/) 的 setter。 |
| [SvgSaveOptions](./svgsaveoptions/)() |  |
| static [Type](./type/)() |  |
## 另见

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
