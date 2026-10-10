---
title: "Aspose::Words::Saving::PdfSaveOptions 类"
linktitle: "PdfSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::PdfSaveOptions 类。可用于在将文档保存为 Pdf 格式时指定其他选项。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


可用于在将文档保存为 [Pdf](../../aspose.words/saveformat/) 格式时指定其他选项。要了解更多信息，请访问 [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) 文档文章。

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Clone](./clone/)() | 创建此对象的深度克隆。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | 创建一个适用于指定保存格式的保存选项对象。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | 创建一个适用于给定文件名中指定的文件扩展名的保存选项对象。 |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | 确定指定的对象在值上是否等于当前对象。 |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | 一个标志，指定是否写入额外的文本定位操作符。 |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | 获取或设置一个布尔值，指示在文档保存时是否允许在嵌入 TrueType 字体时嵌入带有 PostScript 描边的字体。默认值为 **false**。 |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | 获取或设置决定附件如何嵌入到 PDF 文档的值。 |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | 获取或设置决定是否缓存放置在文档背景中的图形的值。 |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | 获取决定颜色呈现方式的值。 |
| [get_Compliance](./get_compliance/)() const | 指定输出文档的 PDF 标准合规级别。 |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | 指定是否将正文故事中的脚注/尾注引用转换为活动超链接。单击时，超链接将指向相应的脚注/尾注。默认值为 **false**。 |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | 获取或设置决定 [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) 导出到 PDF 文件方式的值。 |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | 获取或设置默认模板的路径（包括文件名）。此属性的默认值为 **empty string**。 |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | 获取或设置对输出 PDF 文档签名的详细信息。 |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | 一个标志，指定窗口标题栏是否应显示从文档信息字典的 Title 条目获取的文档标题。 |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 获取决定 3D 效果渲染方式的值。 |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | 获取或设置决定 DrawingML 效果渲染方式的值。 |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | 获取或设置决定 DrawingML 形状渲染方式的值。 |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | 允许指定降采样选项。 |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | 控制字体如何嵌入到生成的 PDF 文档中。 |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | 获取或设置用于加密输出 PDF 文档的详细信息。 |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | 获取或设置一个值，以确定是否导出文档结构。 |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | 获取或设置一个值，以确定浮动形状是否以内联标签的形式导出到文档结构中。 |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | 当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。 |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | 获取或设置一个值，以确定是否在文档结构中创建 "Span" 标签来导出文本语言。 |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | 获取或设置一个值，以确定段落图形是否应标记为工件。 |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | 指定字体嵌入模式。 |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | 指定是否在 PDF 中生成模拟特定 Microsoft Word 表单字段行为的脚本。默认值为 **false**。 |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | 确定页眉/页脚中的书签如何导出。 |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | 指定 PDF 文档中图像的颜色空间选择方式。 |
| [get_ImageCompression](./get_imagecompression/)() const | 指定用于文档中所有图像的压缩类型。 |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | 获取或设置决定墨水 (InkML) 对象渲染方式的值。 |
| [get_InterpolateImages](./get_interpolateimages/)() const | 指示符合规范的阅读器是否应执行图像插值的标志。当指定 **false** 时，标志不会写入输出文档，而是使用阅读器的默认行为。 |
| [get_JpegQuality](./get_jpegquality/)() | 获取或设置一个值，以确定 PDF 文档中 JPEG 图像的质量。 |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | 获取或设置决定 Html 文档中 JPEG 图像质量的值。 |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | 获取决定在保存文档之前是否执行内存优化的值。此属性的默认值为 **false**。 |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | 允许指定元文件渲染选项。 |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | 获取用于数字渲染的 [NumeralFormat](../numeralformat/)。默认使用欧洲数字。 |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | 获取或设置一个值，以确定输出 Pdf 文档中的超链接是否强制在浏览器的新窗口（或标签页）中打开。 |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | 标志指示是否需要优化输出。如果设置此标志，将移除冗余的嵌套画布和空画布，并且相邻具有相同格式的字形会被合并。注意：如果此属性设置为 **true**，内容显示的准确性可能受到影响。默认是 **false**。 |
| [get_OutlineOptions](./get_outlineoptions/)() const | 允许指定大纲选项。 |
| [get_PageLayout](./get_pagelayout/)() const | 指定文档在 PDF 阅读器中打开时使用的页面布局。 |
| [get_PageMode](./get_pagemode/)() const | 指定在 PDF 阅读器中打开时 PDF 文档的显示方式。 |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | 允许控制文档导出为固定页面格式时各个页面的保存方式。 |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | 获取或设置要渲染的页面。默认是文档中的所有页面。 |
| [get_PreblendImages](./get_preblendimages/)() const | 获取或设置一个值，以确定是否将透明图像与黑色背景颜色预先混合。 |
| [get_PreserveFormFields](./get_preserveformfields/)() const | 指定是将 Microsoft Word 表单字段保留为 PDF 中的表单字段还是将其转换为文本。默认值为 **false**。 |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | 当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。 |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | 在保存文档期间调用，并接受有关保存进度的数据。 |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | 指定是否渲染 PDF 选择表单字段的边框。 |
| [get_SaveFormat](./get_saveformat/)() override | 指定如果使用此保存选项对象，文档将以何种格式保存。只能是 [Pdf](../../aspose.words/saveformat/)。 |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | 指定在保存为 DOC 或 DOCX 文件时使用的临时文件夹。默认情况下，此属性为 **null**，且不使用临时文件。 |
| [get_TextCompression](./get_textcompression/)() const | 指定用于文档中所有文本内容的压缩类型。 |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | 确定字体属性是否会根据所使用的字符代码进行更改。 |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) 属性的值。默认值为 **false**；。 |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | 获取决定在将文档保存为固定页面格式之前是否应更新某些类型字段的值。此属性的默认值为 **true**。 |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | 获取或设置决定在保存前是否更新 [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) 属性的值。 |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | 获取或设置决定在保存前是否更新 [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) 属性的值。 |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | 获取一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | 获取或设置一个值，用于确定是否在渲染时使用抗锯齿。 |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | 获取或设置一个布尔值，指示文档是否应使用小册子打印布局进行保存（如果通过 [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/) 指定）。 |
| [get_UseCoreFonts](./get_usecorefonts/)() const | 获取或设置一个值，以确定是否用核心 PDF Type 1 字体替换 TrueType 字体 Arial、Times New Roman、Courier New 和 Symbol。 |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | 获取或设置一个值，用于确定是否使用高质量（即慢速）的渲染算法。 |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | 指定是否在 PDF 中使用 SDT 控件的 Tag 或 Id 属性作为表单字段的名称。 |
| [get_ZoomBehavior](./get_zoombehavior/)() const | 获取一个值，以确定在使用 PDF 查看器打开文档时应应用何种缩放类型。 |
| [get_ZoomFactor](./get_zoomfactor/)() const | 获取一个值，以确定文档的缩放因子（百分比）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | 初始化此类的新实例，可用于将文档保存为 [Pdf](../../aspose.words/saveformat/) 格式。 |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/) 的 setter。 |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) 的 setter。 |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/) 的 setter。 |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)。 |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | 设置决定颜色呈现方式的值。 |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | 指定输出文档的 PDF 标准合规级别。 |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | 指定是否将正文故事中的脚注/尾注引用转换为活动超链接。单击时，超链接将指向相应的脚注/尾注。默认值为 **false**。 |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/)。 |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) 的 setter。 |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) 的 setter。 |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/)。 |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/)。 |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 设置一个值，用于确定 3D 效果的渲染方式。 |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)。 |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/) 的 setter。 |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | 允许指定降采样选项。 |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/)。 |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/)。 |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/)。 |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)。 |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/) 的 setter。 |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)。 |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)。 |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/)。 |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/)。 |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)。 |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)。 |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/)。 |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)。 |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/)。 |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/)。 |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | 设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为 **false**。 |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | 允许指定元文件渲染选项。 |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | 设置用于数字渲染的 [NumeralFormat](../numeralformat/)。默认使用欧洲数字。 |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)。 |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | 用于设置 [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/) 的 setter。 |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | 指定文档在 PDF 阅读器中打开时使用的页面布局。 |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | 指定在 PDF 阅读器中打开时 PDF 文档的显示方式。 |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | 允许控制文档导出为固定页面格式时各个页面的保存方式。 |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | 用于设置 [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/) 的 setter。 |
| [set_PreblendImages](./set_preblendimages/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/)。 |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/)。 |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/)。 |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/) 的 setter。 |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)。 |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | 指定如果使用此保存选项对象，文档将以何种格式保存。只能是 [Pdf](../../aspose.words/saveformat/)。 |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/) 的 setter。 |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/)。 |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/) 的 setter。 |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/) 的 setter。 |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | 设置一个值，用于确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为 **true**。 |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/) 的 setter。 |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/) 的 setter。 |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | 设置一个值，用于确定是否会更新 OLE 控件的呈现图像。 |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/) 的 setter。 |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)。 |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | 用于设置 [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/)。 |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/) 的 setter。 |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | 用于 [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)。 |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | 设置一个值，以确定在使用 PDF 查看器打开文档时应应用的缩放类型。 |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | 设置一个值，以确定文档的缩放因子（以百分比表示）。 |
| static [Type](./type/)() |  |
## 另见

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
