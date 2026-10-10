---
title: "Aspose::Words::Saving::HtmlSaveOptions 类"
linktitle: "HtmlSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions 类。可用于在将文档保存为 Html、Mhtml、Epub、Azw3 或 Mobi 格式时指定其他选项。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


可用于在将文档保存为 [Html](../../aspose.words/saveformat/)、[Mhtml](../../aspose.words/saveformat/)、[Epub](../../aspose.words/saveformat/)、[Azw3](../../aspose.words/saveformat/) 或 [Mobi](../../aspose.words/saveformat/) 格式时指定其他选项。欲了解更多信息，请访问 [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/) 文档文章。

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | 创建一个适用于指定保存格式的保存选项对象。 |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | 创建一个适用于给定文件名中指定的文件扩展名的保存选项对象。 |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | 获取或设置一个布尔值，指示在文档保存时是否允许在嵌入 TrueType 字体时嵌入带有 PostScript 描边的字体。默认值为 **false**。 |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | 指定在保存为 HTML、MHTML 或 EPUB 时是否对段落的负左、右缩进进行标准化。默认值为 **false**。 |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | 指定添加到所有 CSS 类名的前缀。默认值为空字符串，生成的 CSS 类名没有公共前缀。 |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | 允许控制文档保存为 HTML、MHTML 或 EPUB 时 CSS 样式的保存方式。 |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | 指定文档导出为 HTML 时写入的层叠 [Style](../../aspose.words/style/) 表（CSS）文件的路径和名称。默认为空字符串。 |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | 指定 CSS（层叠 [Style](../../aspose.words/style/) 表）样式导出到 HTML、MHTML 或 EPUB 的方式。默认值为 HTML/MHTML 的 [Inline](../cssstylesheettype/) 和 EPUB 的 [External](../cssstylesheettype/)。 |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | 获取或设置默认模板的路径（包括文件名）。此属性的默认值为 **empty string**。 |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | 获取决定 3D 效果渲染方式的值。 |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | 获取或设置决定 DrawingML 效果渲染方式的值。 |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | 获取或设置决定 DrawingML 形状渲染方式的值。 |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | 允许控制文档保存为 HTML 或 EPUB 时文档部件的保存方式。 |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | 指定文档在保存为 [Html](../../aspose.words/saveformat/)、[Epub](../../aspose.words/saveformat/) 或 [Azw3](../../aspose.words/saveformat/) 格式时的拆分方式。默认情况下，HTML 为 [None](../documentsplitcriteria/)，EPUB 和 AZW3 为 [HeadingParagraph](../documentsplitcriteria/)。 |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | 指定拆分文档时的最大标题级别。默认值为 **%2**。 |
| [get_Encoding](./get_encoding/)() const | 指定导出为 HTML、MHTML 或 EPUB 时使用的编码。默认值为 **new UTF8Encoding(false)**（UTF-8 无 BOM）。 |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | 指定是否使用 CID（Content-ID）URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。默认值为 **false**。 |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | 指定是否将内置和自定义文档属性导出到 HTML、MHTML 或 EPUB。默认值为 **false**。 |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | 控制下拉表单字段保存到 HTML 或 MHTML 的方式。默认值为 **false**。 |
| [get_ExportFontResources](./get_exportfontresources/)() const | 指定是否应将字体资源导出到 HTML、MHTML 或 EPUB。默认值为 **false**。 |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | 指定是否应以 Base64 编码将字体资源嵌入到 HTML 中。默认值为 **false**。 |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | 当 **true** 时，会将 Aspose.Words 的名称和版本嵌入生成的文件中。默认值为 **true**。 |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | 指定页眉和页脚输出到 HTML、MHTML 或 EPUB 的方式。默认值为 HTML/MHTML 的 [PerSection](../exportheadersfootersmode/) 和 EPUB 的 [None](../exportheadersfootersmode/)。 |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | 指定是否以 Base64 格式将图像保存到输出的 HTML、MHTML 或 EPUB 中。默认值为 **false**。 |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | 指定是否将语言信息导出到 HTML、MHTML 或 EPUB。默认值为 **false**。 |
| [get_ExportListLabels](./get_exportlistlabels/)() const | 控制列表标签输出到 HTML、MHTML 或 EPUB 的方式。默认值为 [Auto](../exportlistlabels/)。 |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | 指定是否应使用原始 URL 作为链接图像的 URL。默认值为 **false**。 |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | 指定是否将页面边距导出到 HTML、MHTML 或 EPUB。默认值为 **false**。 |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | 指定是否将页面设置导出到 HTML、MHTML 或 EPUB。默认值为 **false**。 |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | 指定在保存为 HTML、MHTML 或 EPUB 时是否以相对单位输出字体大小。默认值为 **false**。 |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | 指定在保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。HTML 的默认值为 **true**，而 MHTML 和 EPUB 为 **false**。 |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | 控制在保存为 HTML、MHTML、EPUB 或 AZW3 时是否将 [Shape](../../aspose.words.drawing/shape/) 节点转换为 SVG 图像。默认值为 **false**。 |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | 控制文本输入表单字段保存到 HTML 或 MHTML 的方式。默认值为 **false**。 |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | 指定在保存 HTML、MHTML 和 EPUB 时是否在目录中写入页码。默认值为 **false**。 |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | 指定在保存为 HTML 或 MHTML 时是否写入 DOCTYPE 声明。当 **true** 时，会在根元素之前写入 DOCTYPE 声明。默认值为 **false**。保存为 EPUB 或 HTML5（[Html5](../htmlversion/)）时始终写入 DOCTYPE 声明。 |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | 控制在保存为 HTML、MHTML 或 EPUB 时哪些字体资源需要子集化。默认值为 **%0**。 |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | 允许控制文档保存为 HTML、MHTML 或 EPUB 时字体的保存方式。 |
| [get_FontsFolder](./get_fontsfolder/)() const | 指定将文档导出为 HTML 时保存字体的物理文件夹。默认值为空字符串。 |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | 指定用于构建写入 HTML 文档的字体 URI 的文件夹名称。默认值为空字符串。 |
| [get_HtmlVersion](./get_htmlversion/)() const | 指定保存文档为 HTML 或 MHTML 时应使用的 HTML 标准版本。默认值为 [Xhtml](../htmlversion/)。 |
| [get_ImageResolution](./get_imageresolution/)() const | 指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。默认值为 **%96 dpi**。 |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | 允许控制文档保存为 HTML、MHTML 或 EPUB 时图像的保存方式。 |
| [get_ImagesFolder](./get_imagesfolder/)() const | 指定将文档导出为 HTML 格式时图像保存的物理文件夹。默认是空字符串。 |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | 指定用于构建写入 HTML 文档的图像 URI 的文件夹名称。默认是空字符串。 |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | 获取或设置决定墨水 (InkML) 对象渲染方式的值。 |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | 获取决定在保存文档之前是否执行内存优化的值。此属性的默认值为 **false**。 |
| [get_MetafileFormat](./get_metafileformat/)() const | 指定将元文件导出为 HTML、MHTML 或 EPUB 时的保存格式。默认值是 [Png](../htmlmetafileformat/)，这意味着元文件将渲染为栅格 PNG 图像。 |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | 指定在导出为 EPUB、MOBI 或 AZW3 格式时填充到导航地图的标题最大层级。默认值为 **%3**。 |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | 控制 OfficeMath 对象导出为 HTML、MHTML 或 EPUB 的方式。默认值是 [Image](../htmlofficemathoutputmode/)。 |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | 当 **true** 时，在适用的情况下对输出进行美化格式化。默认值为 **false**。 |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | 在保存文档期间调用，并接受有关保存进度的数据。 |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | 指定是否从链接中移除 JavaScript。默认值为 **false**。 |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | 指定是否应将反斜杠字符替换为日元符号。默认值为 **false**。 |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | 指定在写入基于 HTML 的格式时，文档中使用的字体族名称是否根据 [FontSettings](../../aspose.words/document/get_fontsettings/) 进行解析和替换。 |
| [get_ResourceFolder](./get_resourcefolder/)() const | 指定将文档导出为 HTML 时，所有资源（如图像、字体和外部 CSS）保存的物理文件夹。默认是空字符串。 |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | 指定用于构建写入 HTML 文档的所有资源 URI 的文件夹名称。默认是空字符串。 |
| [get_SaveFormat](./get_saveformat/)() override | 指定如果使用此保存选项对象，文档将保存的格式。可以是 [Html](../../aspose.words/saveformat/)、[Mhtml](../../aspose.words/saveformat/)、[Epub](../../aspose.words/saveformat/)、[Azw3](../../aspose.words/saveformat/) 或 [Mobi](../../aspose.words/saveformat/)。 |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | 指定在导出为 HTML、MHTML 或 EPUB 时，图像是否由 Aspose.Words 按边界形状大小进行缩放。默认值为 **true**。 |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | 控制表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB 的方式。默认值是 [All](../htmlelementsizeoutputmode/)。 |
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
| [HtmlSaveOptions](./htmlsaveoptions/)() | 初始化此类的新实例，可用于将文档保存为 [Html](../../aspose.words/saveformat/) 格式。 |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | 初始化此类的新实例，可用于将文档保存为 [Html](../../aspose.words/saveformat/)、[Mhtml](../../aspose.words/saveformat/)、[Epub](../../aspose.words/saveformat/)、[Azw3](../../aspose.words/saveformat/) 或 [Mobi](../../aspose.words/saveformat/) 格式。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/) 的 setter。 |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/) 的 setter。 |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/) 的 setter。 |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | 允许控制文档保存为 HTML、MHTML 或 EPUB 时 CSS 样式的保存方式。 |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/) 的 setter。 |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/) 的 setter。 |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/) 的 setter。 |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/) 的 setter。 |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | 设置一个值，用于确定 3D 效果的渲染方式。 |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/) 的 setter。 |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/) 的 setter。 |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | 允许控制文档保存为 HTML 或 EPUB 时文档部件的保存方式。 |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/) 的 setter。 |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/) 的 setter。 |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/) 的 setter。 |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/) 的 setter。 |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/) 的 setter。 |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/) 的 setter。 |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/) 的 setter。 |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/) 的 setter。 |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/) 的 setter。 |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/) 的 setter。 |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/)。 |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/)。 |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/)。 |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)。 |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/)。 |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/)。 |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/)。 |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/)。 |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/)。 |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)。 |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/)。 |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)。 |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)。 |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | 允许控制文档保存为 HTML、MHTML 或 EPUB 时字体的保存方式。 |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/)。 |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/)。 |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/)。 |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/)。 |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | 允许控制文档保存为 HTML、MHTML 或 EPUB 时图像的保存方式。 |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/)。 |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/)。 |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)。 |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | 设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为 **false**。 |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/)。 |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/)。 |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/)。 |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/)。 |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | 用于设置 [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/) 的 setter。 |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | 指定是否从链接中移除 JavaScript。默认值为 **false**。 |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/) 的 setter。 |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/) 的 setter。 |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/) 的 setter。 |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/) 的 setter。 |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/) 的 setter。 |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/) 的 setter。 |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | 用于设置 [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/) 的 setter。 |
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



展示如何在将文档保存为 .epub 时使用特定的编码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 使用 SaveOptions 对象来指定我们将要保存的文档的编码。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// 默认情况下，输出的 .epub 文档的所有内容都位于一个 HTML 部分中。
// 拆分条件允许我们将文档划分为多个 HTML 部分。
// 我们将设置条件，以将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的阅读器很有用。
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// 指定我们要导出文档属性。
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


展示如何在保存为 .html 后指定用于存储链接图像的文件夹。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// 设置一个选项，将表单字段导出为纯文本而不是 HTML 输入元素。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## 另见

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
