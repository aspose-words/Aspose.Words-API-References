---
title: "Aspose::Words::Saving::RtfSaveOptions 类"
linktitle: "RtfSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::RtfSaveOptions 类。可用于在将文档保存为 Rtf 格式时指定其他选项。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words.saving/rtfsaveoptions/
---
## RtfSaveOptions class


可用于在将文档保存为 [Rtf](../../aspose.words/saveformat/) 格式时指定其他选项。欲了解更多，请访问 [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) 文档文章。

```cpp
class RtfSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | 创建一个适用于指定保存格式的保存选项对象。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | 创建一个适用于给定文件名中指定的文件扩展名的保存选项对象。 |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | 获取或设置一个布尔值，指示在文档保存时是否允许在嵌入 TrueType 字体时嵌入带有 PostScript 描边的字体。默认值为 **false**。 |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | 获取或设置默认模板的路径（包括文件名）。此属性的默认值为 **empty string**。 |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 获取决定 3D 效果渲染方式的值。 |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | 获取或设置决定 DrawingML 效果渲染方式的值。 |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | 获取或设置决定 DrawingML 形状渲染方式的值。 |
| [get_ExportCompactSize](./get_exportcompactsize/)() const | 允许使输出的 RTF 文档体积更小，但如果其中包含 RTL（从右到左）文本，则无法正确显示。默认值为 **false**。 |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | 当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。 |
| [get_ExportImagesForOldReaders](./get_exportimagesforoldreaders/)() const | 指定是否将针对 \"old readers\" 的关键字写入 RTF。此设置可能显著影响 RTF 文档的大小。默认值为 **true**。 |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | 获取或设置决定墨水 (InkML) 对象渲染方式的值。 |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | 获取决定在保存文档之前是否执行内存优化的值。此属性的默认值为 **false**。 |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | 当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。 |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | 在保存文档期间调用，并接受有关保存进度的数据。 |
| [get_SaveFormat](./get_saveformat/)() override | 指定在使用此保存选项对象时文档将保存的格式。只能是 [Rtf](../../aspose.words/saveformat/)。 |
| [get_SaveImagesAsWmf](./get_saveimagesaswmf/)() const | 当 **true** 时，所有图像将保存为 WMF。 |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | 指定在保存为 DOC 或 DOCX 文件时使用的临时文件夹。默认情况下，此属性为 **null**，且不使用临时文件。 |
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
| [RtfSaveOptions](./rtfsaveoptions/)() |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) 的 setter。 |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) 的 setter。 |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) 的 setter。 |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 设置一个值，用于确定 3D 效果的渲染方式。 |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/) 的 setter。 |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/) 的 setter。 |
| [set_ExportCompactSize](./set_exportcompactsize/)(bool) | 用于设置 [Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize](./get_exportcompactsize/) 的 setter。 |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/) 的 setter。 |
| [set_ExportImagesForOldReaders](./set_exportimagesforoldreaders/)(bool) | 用于设置 [Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders](./get_exportimagesforoldreaders/) 的 setter。 |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)。 |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | 设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为 **false**。 |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/)。 |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/) 的 setter。 |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | 用于设置 [Aspose::Words::Saving::RtfSaveOptions::get_SaveFormat](./get_saveformat/) 的 setter。 |
| [set_SaveImagesAsWmf](./set_saveimagesaswmf/)(bool) | 用于设置 [Aspose::Words::Saving::RtfSaveOptions::get_SaveImagesAsWmf](./get_saveimagesaswmf/) 的 setter。 |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/) 的 setter。 |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/) 的 setter。 |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/) 的 setter。 |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | 设置一个值，用于确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为 **true**。 |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/) 的 setter。 |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/) 的 setter。 |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | 设置一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/) 的 setter。 |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/) 的 setter。 |
| static [Type](./type/)() |  |

## 示例



展示如何使用自定义选项将文档保存为 .rtf。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 创建一个 \"RtfSaveOptions\" 对象并传递给文档的 \"Save\" 方法，以修改我们将其保存为 RTF 的方式。
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// 将 \"ExportCompactSize\" 属性设置为 \"true\" 以
// 在牺牲从右到左文本兼容性的前提下减小已保存文档的大小。
options->set_ExportCompactSize(true);

// 将 \"ExportImagesFotOldReaders\" 属性设置为 \"true\" 以使用额外的关键字，确保我们的文档是
// 兼容 Microsoft Word 97 之前的阅读器和 WordPad。
// 将 \"ExportImagesFotOldReaders\" 属性设置为 \"false\" 以减小文档的大小，
// 但会阻止旧阅读器读取文档中可能包含的任何非元文件或 BMP 图像。
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## 另见

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
