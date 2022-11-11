---
title: HtmlSaveOptions
second_title: Aspose.Words for Java API 参考
description:可用于在将文档保存为 or 格式时指定其他选项。
type: docs
weight: 331
url: /zh/java/com.aspose.words/htmlsaveoptions/
---

**遗产:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)

**All Implemented 界面s:**
java.lang.Cloneable
```
public class HtmlSaveOptions extends SaveOptions implements Cloneable
```

可用于在将文档保存到[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式。

要了解更多信息，请访问**Specify Save Options**文档文章。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [HtmlSaveOptions()](#HtmlSaveOptions--) | 初始化此类的新实例，该实例可用于将文档保存在[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML)格式。 |
| [HtmlSaveOptions(int saveFormat)](#HtmlSaveOptions-int-) | 初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | 创建适合给定文件名中指定的文件扩展名的类的保存选项对象。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | 获取一个布尔值，该值指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [getAllowNegativeIndent()](#getAllowNegativeIndent--) | 指定在保存为 HTML、MHTML 或 EPUB 时是否规范段落的负左缩进和右缩进。 |
| [get班级()](#get班级--) |  |
| [getCss班级NamePrefix()](#getCss班级NamePrefix--) | 指定添加到所有 CSS 类名称的前缀。 |
| [getCssSavingCallback()](#getCssSavingCallback--) | 允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存 CSS 样式。 |
| [getCssStyleSheetFileName()](#getCssStyleSheetFileName--) | 指定将文档导出为 HTML 时写入的层叠样式表 (CSS) 文件的路径和名称。 |
| [getCssStyleSheet类型()](#getCssStyleSheet类型--) | 指定如何将 CSS（层叠样式表）样式导出为 HTML、MHTML 或 EPUB。 |
| [getDefaultTemplate()](#getDefaultTemplate--) | 获取默认模板的路径（包括文件名）。 |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | 获取确定如何渲染 3D 效果的值。 |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | 获取一个值，该值确定如何呈现 DrawingML 效果。 |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | 获取一个值，该值确定如何呈现 DrawingML 形状。 |
| [getDocumentPartSavingCallback()](#getDocumentPartSavingCallback--) | 允许控制将文档保存为 HTML 或 EPUB 时如何保存文档部分。 |
| [getDocumentSplitCriteria()](#getDocumentSplitCriteria--) | 指定在保存到时应如何拆分文档[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式。 |
| [getDocumentSplitHeadingLevel()](#getDocumentSplitHeadingLevel--) | 指定拆分文档的最大标题级别。 |
| [getEncoding()](#getEncoding--) |  |
| [getEpubNavigationMapLevel()](#getEpubNavigationMapLevel--) | 指定导出为 IDPF EPUB 格式时填充到导航地图的最大标题级别。 |
| [getExportCidUrlsForMhtmlResources()](#getExportCidUrlsForMhtmlResources--) | 指定是否使用 CID (Content-ID) URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。 |
| [getExportDocumentProperties()](#getExportDocumentProperties--) | 指定是否将内置和自定义文档属性导出为 HTML、MHTML 或 EPUB。 |
| [getExportDropDownForm字段AsText()](#getExportDropDownForm字段AsText--) | 控制如何将下拉表单字段保存为 HTML 或 MHTML。 |
| [getExportFontResources()](#getExportFontResources--) | 指定字体资源是否应导出为 HTML、MHTML 或 EPUB。 |
| [getExportFontsAsBase64()](#getExportFontsAsBase64--) | 指定字体资源是否应以 Base64 编码嵌入到 HTML。 |
| [getExportGeneratorName()](#getExportGeneratorName--) | 如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode--) | 指定页眉和页脚如何输出到 HTML、MHTML 或 EPUB。 |
| [getExportImagesAsBase64()](#getExportImagesAsBase64--) | 指定图像是否以 Base64 格式保存到输出 HTML、MHTML 或 EPUB。 |
| [getExportLanguageInformation()](#getExportLanguageInformation--) | 指定是否将语言信息导出为 HTML、MHTML 或 EPUB。 |
| [getExportListLabels()](#getExportListLabels--) | 控制列表标签如何输出到 HTML、MHTML 或 EPUB。 |
| [getExportOriginalUrlForLinkedImages()](#getExportOriginalUrlForLinkedImages--) | 指定是否应将原始 URL 用作链接图像的 URL。 |
| [getExportPageMargins()](#getExportPageMargins--) | 指定页边距是否导出为 HTML、MHTML 或 EPUB。 |
| [getExportPageSetup()](#getExportPageSetup--) | 指定是否将页面设置导出为 HTML、MHTML 或 EPUB。 |
| [getExportRelativeFontSize()](#getExportRelativeFontSize--) | 指定保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。 |
| [getExportRoundtripInformation()](#getExportRoundtripInformation--) | 指定保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。 |
| [getExportShapesAsSvg()](#getExportShapesAsSvg--) | 控制是否[Shape](../../com.aspose.words/shape)保存为 HTML、MHTML、EPUB 或 AZW3 时，节点将转换为 SVG 图像。 |
| [getExportTextInputForm字段AsText()](#getExportTextInputForm字段AsText--) | 控制文本输入表单字段如何保存为 HTML 或 MHTML。 |
| [getExportTocPageNumbers()](#getExportTocPageNumbers--) | 指定在保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。 |
| [getExportXhtmlTransitional()](#getExportXhtmlTransitional--) | 指定保存为 HTML 或 MHTML 时是否编写 DOCTYPE 声明。 |
| [getFontResourcesSubsettingSizeThreshold()](#getFontResourcesSubsettingSizeThreshold--) | 控制保存为 HTML、MHTML 或 EPUB 时需要子集的字体资源。 |
| [getFontSavingCallback()](#getFontSavingCallback--) | 允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存字体。 |
| [getFontsFolder()](#getFontsFolder--) | 指定将文档导出为 HTML 时保存字体的物理文件夹。 |
| [getFontsFolderAlias()](#getFontsFolderAlias--) | 指定用于构造写入 HTML 文档的字体 URI 的文件夹的名称。 |
| [getHtmlVersion()](#getHtmlVersion--) | 指定将文档保存为 HTML 或 MHTML 时应使用的 HTML 标准版本。 |
| [getImageResolution()](#getImageResolution--) | 指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。 |
| [getImageSavingCallback()](#getImageSavingCallback--) | 允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存图像。 |
| [getImagesFolder()](#getImagesFolder--) | 指定将文档导出为 HTML 格式时保存图像的物理文件夹。 |
| [getImagesFolderAlias()](#getImagesFolderAlias--) | 指定用于构造写入 HTML 文档的图像 URI 的文件夹的名称。 |
| [getImlRenderingMode()](#getImlRenderingMode--) | 获取一个值，该值确定如何呈现墨迹 (InkML) 对象。 |
| [getMemoryOptimization()](#getMemoryOptimization--) | 获取确定是否应在保存文档之前执行内存优化的值。 |
| [getMetafileFormat()](#getMetafileFormat--) | 指定导出为 HTML、MHTML 或 EPUB 时以何种格式保存元文件。 |
| [getOfficeMathOutputMode()](#getOfficeMathOutputMode--) | 控制如何将 OfficeMath 对象导出为 HTML、MHTML 或 EPUB。 |
| [getPrettyFormat()](#getPrettyFormat--) | 如果为 true ，则在适用的情况下输出漂亮的格式。 |
| [getProgressCallback()](#getProgressCallback--) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [getResolveFontNames()](#getResolveFontNames--) | 指定文档中使用的字体系列名称是否根据[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)当被写入基于 HTML 的格式时。 |
| [getResourceFolder()](#getResourceFolder--) | 指定将文档导出为 HTML 时保存所有资源（如图像、字体和外部 CSS）的物理文件夹。 |
| [getResourceFolderAlias()](#getResourceFolderAlias--) | 指定用于构造写入 HTML 文档的所有资源的 URI 的文件夹的名称。 |
| [getSaveFormat()](#getSaveFormat--) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [getScaleImageToShapeSize()](#getScaleImageToShapeSize--) | 指定当导出为 HTML、MHTML 或 EPUB 时，图像是否由 Aspose.Words 缩放到边界形状大小。 |
| [getTableWidthOutputMode()](#getTableWidthOutputMode--) | 控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。 |
| [getTempFolder()](#getTempFolder--) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdate字段()](#getUpdate字段--) | 获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateSdtContent()](#getUpdateSdtContent--) | 获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | 获取一个值，该值确定是否使用抗锯齿进行渲染。 |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | 获取确定是否使用高质量的值（即 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | 设置一个布尔值，指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [setAllowNegativeIndent(boolean value)](#setAllowNegativeIndent-boolean-) | 指定在保存为 HTML、MHTML 或 EPUB 时是否规范段落的负左缩进和右缩进。 |
| [setCss班级NamePrefix(String value)](#setCss班级NamePrefix-java.lang.String-) | 指定添加到所有 CSS 类名称的前缀。 |
| [setCssSavingCallback(ICssSavingCallback value)](#setCssSavingCallback-com.aspose.words.ICssSavingCallback-) | 允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存 CSS 样式。 |
| [setCssStyleSheetFileName(String value)](#setCssStyleSheetFileName-java.lang.String-) | 指定将文档导出为 HTML 时写入的层叠样式表 (CSS) 文件的路径和名称。 |
| [setCssStyleSheet类型(int value)](#setCssStyleSheet类型-int-) | 指定如何将 CSS（层叠样式表）样式导出为 HTML、MHTML 或 EPUB。 |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | 设置默认模板的路径（包括文件名）。 |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | 设置确定如何渲染 3D 效果的值。 |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 效果。 |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 形状。 |
| [setDocumentPartSavingCallback(IDocumentPartSavingCallback value)](#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback-) | 允许控制将文档保存为 HTML 或 EPUB 时如何保存文档部分。 |
| [setDocumentSplitCriteria(int value)](#setDocumentSplitCriteria-int-) | 指定在保存到时应如何拆分文档[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式。 |
| [setDocumentSplitHeadingLevel(int value)](#setDocumentSplitHeadingLevel-int-) | 指定拆分文档的最大标题级别。 |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [setEpubNavigationMapLevel(int value)](#setEpubNavigationMapLevel-int-) | 指定导出为 IDPF EPUB 格式时填充到导航地图的最大标题级别。 |
| [setExportCidUrlsForMhtmlResources(boolean value)](#setExportCidUrlsForMhtmlResources-boolean-) | 指定是否使用 CID (Content-ID) URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。 |
| [setExportDocumentProperties(boolean value)](#setExportDocumentProperties-boolean-) | 指定是否将内置和自定义文档属性导出为 HTML、MHTML 或 EPUB。 |
| [setExportDropDownForm字段AsText(boolean value)](#setExportDropDownForm字段AsText-boolean-) | 控制如何将下拉表单字段保存为 HTML 或 MHTML。 |
| [setExportFontResources(boolean value)](#setExportFontResources-boolean-) | 指定字体资源是否应导出为 HTML、MHTML 或 EPUB。 |
| [setExportFontsAsBase64(boolean value)](#setExportFontsAsBase64-boolean-) | 指定字体资源是否应以 Base64 编码嵌入到 HTML。 |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | 如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int-) | 指定页眉和页脚如何输出到 HTML、MHTML 或 EPUB。 |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean-) | 指定图像是否以 Base64 格式保存到输出 HTML、MHTML 或 EPUB。 |
| [setExportLanguageInformation(boolean value)](#setExportLanguageInformation-boolean-) | 指定是否将语言信息导出为 HTML、MHTML 或 EPUB。 |
| [setExportListLabels(int value)](#setExportListLabels-int-) | 控制列表标签如何输出到 HTML、MHTML 或 EPUB。 |
| [setExportOriginalUrlForLinkedImages(boolean value)](#setExportOriginalUrlForLinkedImages-boolean-) | 指定是否应将原始 URL 用作链接图像的 URL。 |
| [setExportPageMargins(boolean value)](#setExportPageMargins-boolean-) | 指定页边距是否导出为 HTML、MHTML 或 EPUB。 |
| [setExportPageSetup(boolean value)](#setExportPageSetup-boolean-) | 指定是否将页面设置导出为 HTML、MHTML 或 EPUB。 |
| [setExportRelativeFontSize(boolean value)](#setExportRelativeFontSize-boolean-) | 指定保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。 |
| [setExportRoundtripInformation(boolean value)](#setExportRoundtripInformation-boolean-) | 指定保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。 |
| [setExportShapesAsSvg(boolean value)](#setExportShapesAsSvg-boolean-) | 控制是否[Shape](../../com.aspose.words/shape)保存为 HTML、MHTML、EPUB 或 AZW3 时，节点将转换为 SVG 图像。 |
| [setExportTextInputForm字段AsText(boolean value)](#setExportTextInputForm字段AsText-boolean-) | 控制文本输入表单字段如何保存为 HTML 或 MHTML。 |
| [setExportTocPageNumbers(boolean value)](#setExportTocPageNumbers-boolean-) | 指定在保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。 |
| [setExportXhtmlTransitional(boolean value)](#setExportXhtmlTransitional-boolean-) | 指定保存为 HTML 或 MHTML 时是否编写 DOCTYPE 声明。 |
| [setFontResourcesSubsettingSizeThreshold(int value)](#setFontResourcesSubsettingSizeThreshold-int-) | 控制保存为 HTML、MHTML 或 EPUB 时需要子集的字体资源。 |
| [setFontSavingCallback(IFontSavingCallback value)](#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) | 允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存字体。 |
| [setFontsFolder(String value)](#setFontsFolder-java.lang.String-) | 指定将文档导出为 HTML 时保存字体的物理文件夹。 |
| [setFontsFolderAlias(String value)](#setFontsFolderAlias-java.lang.String-) | 指定用于构造写入 HTML 文档的字体 URI 的文件夹的名称。 |
| [setHtmlVersion(int value)](#setHtmlVersion-int-) | 指定将文档保存为 HTML 或 MHTML 时应使用的 HTML 标准版本。 |
| [setImageResolution(int value)](#setImageResolution-int-) | 指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。 |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) | 允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存图像。 |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String-) | 指定将文档导出为 HTML 格式时保存图像的物理文件夹。 |
| [setImagesFolderAlias(String value)](#setImagesFolderAlias-java.lang.String-) | 指定用于构造写入 HTML 文档的图像 URI 的文件夹的名称。 |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | 设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | 设置值确定是否应在保存文档之前执行内存优化。 |
| [setMetafileFormat(int value)](#setMetafileFormat-int-) | 指定导出为 HTML、MHTML 或 EPUB 时以何种格式保存元文件。 |
| [setOfficeMathOutputMode(int value)](#setOfficeMathOutputMode-int-) | 控制如何将 OfficeMath 对象导出为 HTML、MHTML 或 EPUB。 |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | 如果为 true ，则在适用的情况下输出漂亮的格式。 |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [setResolveFontNames(boolean value)](#setResolveFontNames-boolean-) | 指定文档中使用的字体系列名称是否根据[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)当被写入基于 HTML 的格式时。 |
| [setResourceFolder(String value)](#setResourceFolder-java.lang.String-) | 指定将文档导出为 HTML 时保存所有资源（如图像、字体和外部 CSS）的物理文件夹。 |
| [setResourceFolderAlias(String value)](#setResourceFolderAlias-java.lang.String-) | 指定用于构造写入 HTML 文档的所有资源的 URI 的文件夹的名称。 |
| [setSaveFormat(int value)](#setSaveFormat-int-) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [setScaleImageToShapeSize(boolean value)](#setScaleImageToShapeSize-boolean-) | 指定当导出为 HTML、MHTML 或 EPUB 时，图像是否由 Aspose.Words 缩放到边界形状大小。 |
| [setTableWidthOutputMode(int value)](#setTableWidthOutputMode-int-) | 控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdate字段(boolean value)](#setUpdate字段-boolean-) | 设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) | 设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | 设置一个值，确定是否使用抗锯齿进行渲染。 |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | 设置一个值来确定是否使用高质量（即 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### HtmlSaveOptions() {#HtmlSaveOptions--}
```
public HtmlSaveOptions()
```


初始化此类的新实例，该实例可用于将文档保存在[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML)格式。

### HtmlSaveOptions(int saveFormat) {#HtmlSaveOptions-int-}
```
public HtmlSaveOptions(int saveFormat)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

### createSaveOptions(int saveFormat) {#createSaveOptions-int-}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货:**
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String-}
```
public static SaveOptions createSaveOptions(String fileName)
```


创建适合给定文件名中指定的文件扩展名的类的保存选项对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 此文件名的扩展名确定要创建的保存选项对象的类。 |

**退货:**
[SaveOptions](../../com.aspose.words/saveoptions) - 派生自的类的对象[SaveOptions](../../com.aspose.words/saveoptions).
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


获取一个布尔值，该值指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值为**false**.

请注意，Word 不嵌入 PostScript 字体，但可以打开嵌入了这种类型字体的文档。

此选项仅在以下情况下有效[FontInfoCollection.getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [FontInfoCollection.setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)的[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性设置为 true 。

**退货:**
boolean - 一个布尔值，指示在保存文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。
### getAllowNegativeIndent() {#getAllowNegativeIndent--}
```
public boolean getAllowNegativeIndent()
```


指定在保存为 HTML、MHTML 或 EPUB 时是否规范段落的负左缩进和右缩进。默认值为 false 。

当不允许负缩进时，它将作为零边距导出到 HTML。当允许负缩进时，段落可能会部分显示在浏览器窗口之外。

**退货:**
boolean - 对应的布尔值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCss班级NamePrefix() {#getCss班级NamePrefix--}
```
public String getCss班级NamePrefix()
```


指定添加到所有 CSS 类名称的前缀。默认值为空字符串，生成的 CSS 类名没有公共前缀。

如果此值不为空，Aspose.Words 生成的所有 CSS 类都将以指定的前缀开头。这可能很有用，例如，如果您将自定义 CSS 添加到生成的文档并希望防止类名冲突。

如果该值不为 null 或为空，则它必须是有效的 CSS 标识符。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getCssSavingCallback() {#getCssSavingCallback--}
```
public ICssSavingCallback getCssSavingCallback()
```


允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存 CSS 样式。

**退货:**
[ICssSavingCallback](../../com.aspose.words/icsssavingcallback) - 相应的[ICssSavingCallback](../../com.aspose.words/icsssavingcallback)价值。
### getCssStyleSheetFileName() {#getCssStyleSheetFileName--}
```
public String getCssStyleSheetFileName()
```


指定将文档导出为 HTML 时写入的层叠样式表 (CSS) 文件的路径和名称。默认为空字符串。

此属性仅在将文档保存为 HTML 格式并且使用请求外部 CSS 样式表时才有效[getCssStyleSheet类型()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheet类型--) / [setCssStyleSheet类型(int)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheet类型-int-).

如果此属性为空，则 CSS 文件将保存到与 HTML 文档同名但扩展名为“.css”的同一文件夹中。

如果此属性中仅指定路径但未指定文件名，则 CSS 文件将保存到指定文件夹中，并与 HTML 文档同名，但扩展名为“.css”。

如果此属性指定的文件夹不存在，则会在保存 CSS 文件之前自动创建。

指定保存外部 CSS 文件的文件夹的另一种方法是使用[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getCssStyleSheet类型() {#getCssStyleSheet类型--}
```
public int getCssStyleSheet类型()
```


指定如何将 CSS（层叠样式表）样式导出为 HTML、MHTML 或 EPUB。默认值为[CssStyleSheet类型.INLINE](../../com.aspose.words/cssstylesheettype\#INLINE)对于 HTML/MHTML 和[CssStyleSheet类型.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL)对于 EPUB。

仅当保存为 HTML 时才支持将 CSS 样式表保存到外部文件中。当您导出为其中一种容器格式（EPUB 或 MHTML）并指定[CssStyleSheet类型.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL)CSS 文件将被封装到输出包中。

**退货:**
int - 对应的 int 值。返回值是以下之一[CssStyleSheet类型](../../com.aspose.words/cssstylesheettype)常数。
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


获取默认模板的路径（包括文件名）。此属性的默认值为**empty string**.如果指定，此路径用于加载模板时[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-)是真的，但是[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)是空的。

**退货:**
java.lang.String - 默认模板的路径（包括文件名）。
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode--}
```
public int getDml3DEffectsRenderingMode()
```


获取确定如何渲染 3D 效果的值。默认值为[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**退货:**
int - 确定如何渲染 3D 效果的值。返回值是以下之一[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode)常数。
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


获取一个值，该值确定如何呈现 DrawingML 效果。默认值为[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

当文档导出为固定页面格式时使用此属性。

**退货:**
 int - 确定如何呈现 DrawingML 效果的值。返回值是以下之一[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode)常数。
### getDmlRenderingMode() {#getDmlRenderingMode--}
```
public int getDmlRenderingMode()
```


获取一个值，该值确定如何呈现 DrawingML 形状。默认值为[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

当文档导出为固定页面格式时使用此属性。

**退货:**
int - 确定如何呈现 DrawingML 形状的值。返回值是以下之一[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode)常数。
### getDocumentPartSavingCallback() {#getDocumentPartSavingCallback--}
```
public IDocumentPartSavingCallback getDocumentPartSavingCallback()
```


允许控制将文档保存为 HTML 或 EPUB 时如何保存文档部分。

**退货:**
[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) - 相应的[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback)价值。
### getDocumentSplitCriteria() {#getDocumentSplitCriteria--}
```
public int getDocumentSplitCriteria()
```


指定在保存到时应如何拆分文档[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式。默认为[DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria\#NONE)对于 HTML 和[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH)适用于 EPUB 和 AZW3。

通常，您希望将文档作为单个文件保存为 HTML。但在某些情况下，最好将输出拆分为几个较小的 HTML 页面。保存为 HTML 格式时，这些页面将输出到单个文件或流中。当保存为 EPUB 格式时，它们将被合并到相应的包中。

以 MHTML 格式保存时无法拆分文档。

**退货:**
 int - 对应的 int 值。返回值是按位组合[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria)常数。
### getDocumentSplitHeadingLevel() {#getDocumentSplitHeadingLevel--}
```
public int getDocumentSplitHeadingLevel()
```


指定拆分文档的最大标题级别。默认值为 2 。

什么时候[getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-)包括[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH)并且此属性设置为 1 到 9 之间的值，文档将在使用格式化的段落处拆分**Heading 1**, **Heading 2** , **Heading 3**等样式直到指定的标题级别。

默认情况下，仅**Heading 1**和**Heading 2**段落导致文档被拆分。将此属性设置为零将导致文档根本不会在标题段落处拆分。

**退货:**
int - 对应的 int 值。
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**退货:**
java.nio.charset.Charset
### getEpubNavigationMapLevel() {#getEpubNavigationMapLevel--}
```
public int getEpubNavigationMapLevel()
```


指定导出为 IDPF EPUB 格式时填充到导航地图的最大标题级别。默认值为 3 。

IDPF EPUB 格式的导航图允许用户代理通过文档结构提供简单的导航方式。通常导航点对应于文档中的标题。将标题填充到级别**N**将此值分配给[getEpubNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions\#getEpubNavigationMapLevel--) / [setEpubNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions\#setEpubNavigationMapLevel-int-).

默认情况下，会填充三个级别的标题：样式段落**Heading 1**, **Heading 2**和**Heading 3**.您可以将此属性设置为 1 到 9 之间的值，以请求相应的最大级别。将其设置为零会将导航图减少为仅文档根或文档部分的根。

**退货:**
int - 对应的 int 值。
### getExportCidUrlsForMhtmlResources() {#getExportCidUrlsForMhtmlResources--}
```
public boolean getExportCidUrlsForMhtmlResources()
```


指定是否使用 CID (Content-ID) URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。默认值为 false 。

此选项仅影响保存为 MHTML 的文档。

默认情况下，MHTML 文档中的资源由文件名（例如，“image.png”）引用，这些文件名与 MIME 部分的“Content-Location”标题相匹配。

此选项启用另一种方法，其中对资源文件的引用被写入 CID (Content-ID) URL（例如，“cid:image.png”）并与“Content-ID”标头匹配。

理论上，这两种引用方法之间应该没有区别，并且它们中的任何一种都应该在任何浏览器或邮件代理中都可以正常工作。然而，在实践中，一些代理无法通过文件名获取资源。如果您的浏览器或邮件代理拒绝加载 MTHML 文档中包含的资源（不显示图像或不加载 CSS 样式），请尝试使用 CID URL 导出文档。

**退货:**
boolean - 对应的布尔值。
### getExportDocumentProperties() {#getExportDocumentProperties--}
```
public boolean getExportDocumentProperties()
```


指定是否将内置和自定义文档属性导出为 HTML、MHTML 或 EPUB。默认值为 false 。

**退货:**
boolean - 对应的布尔值。
### getExportDropDownForm字段AsText() {#getExportDropDownForm字段AsText--}
```
public boolean getExportDropDownForm字段AsText()
```


控制如何将下拉表单字段保存为 HTML 或 MHTML。默认值为 false 。

当设置为 true 时，将下拉表单字段导出为普通文本。当 false 时，将下拉表单字段导出为 HTML 中的 SELECT 元素。

导出到 EPUB 时，由于此格式的要求，文本下拉表单字段始终保存为文本。

**退货:**
boolean - 对应的布尔值。
### getExportFontResources() {#getExportFontResources--}
```
public boolean getExportFontResources()
```


指定字体资源是否应导出为 HTML、MHTML 或 EPUB。默认为 false 。

导出字体资源允许独立于给定用户环境中可用的字体的一致文档渲染。

如果[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)设置为 true ，主 HTML 文档将通过 CSS 3 引用每种字体**@font-face**at-rule 和 fonts 将作为单独的文件输出。导出为 IDPF EPUB 或 MHTML 格式时，字体将与其他附属文件一起嵌入到相应的包中。

如果[getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions\#getExportFontsAsBase64--) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontsAsBase64-boolean-)设置为 true ，字体将不会保存到单独的文件中。相反，它们将被嵌入**@font-face**Base64 编码中的 at 规则。

**Important!**导出字体资源时，应考虑字体许可问题。希望通过可下载字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可的范围内。许多商业字体目前不允许以任何形式从网络下载其字体。涵盖某些字体的许可协议特别指出，使用**@font-face**CSS 样式表中的规则是不允许的。字体子集也可能违反许可条款。

**退货:**
boolean - 对应的布尔值。
### getExportFontsAsBase64() {#getExportFontsAsBase64--}
```
public boolean getExportFontsAsBase64()
```


指定字体资源是否应以 Base64 编码嵌入到 HTML。默认为 false 。

默认情况下，字体被写入单独的文件。如果此选项设置为 true ，字体将以 Base64 编码嵌入到文档的 CSS 中。

**退货:**
boolean - 对应的布尔值。
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。默认值为**true**.

**退货:**
boolean - 对应的布尔值。
### getExportHeadersFootersMode() {#getExportHeadersFootersMode--}
```
public int getExportHeadersFootersMode()
```


指定页眉和页脚如何输出到 HTML、MHTML 或 EPUB。默认值为[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION)对于 HTML/MHTML 和[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE)对于 EPUB。

很难将页眉和页脚有意义地输出到 HTML，因为 HTML 没有分页。

当这个属性是[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION)Aspose.Words 只导出每个部分开头和结尾的主要页眉和页脚。

几时[ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER)仅导出第一个主页眉和最后一个主页脚（包括链接到上一个页脚）。

您可以通过将此属性设置为来完全禁用页眉和页脚的导出[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE).

**退货:**
int - 对应的 int 值。返回值是以下之一[ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode)常数。
### getExportImagesAsBase64() {#getExportImagesAsBase64--}
```
public boolean getExportImagesAsBase64()
```


指定图像是否以 Base64 格式保存到输出 HTML、MHTML 或 EPUB。默认为 false 。

当此属性设置为 true 时，图像数据将直接导出到**img**不会创建元素和单独的文件。

**退货:**
boolean - 对应的布尔值。
### getExportLanguageInformation() {#getExportLanguageInformation--}
```
public boolean getExportLanguageInformation()
```


指定是否将语言信息导出为 HTML、MHTML 或 EPUB。默认为 false 。

当此属性设置为 true 时，Aspose.Words 输出**lang**指定语言的文档元素上的 HTML 属性。这可能需要保留与语言相关的语义。

**退货:**
boolean - 对应的布尔值。
### getExportListLabels() {#getExportListLabels--}
```
public int getExportListLabels()
```


控制列表标签如何输出到 HTML、MHTML 或 EPUB。默认值为[ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels\#AUTO).

**退货:**
int - 对应的 int 值。返回值是以下之一[ExportListLabels](../../com.aspose.words/exportlistlabels)常数。
### getExportOriginalUrlForLinkedImages() {#getExportOriginalUrlForLinkedImages--}
```
public boolean getExportOriginalUrlForLinkedImages()
```


指定是否应将原始 URL 用作链接图像的 URL。默认值为 false 。

如果值设置为 true[ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)值用作链接图像的 URL，并且链接图像未加载到文档的文件夹中或[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-).

如果值设置为 false 链接图像被加载到文档的文件夹或[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)每个链接图像的 URL 是根据文档的文件夹构建的，[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)特性。

**退货:**
boolean - 对应的布尔值。
### getExportPageMargins() {#getExportPageMargins--}
```
public boolean getExportPageMargins()
```


指定页边距是否导出为 HTML、MHTML 或 EPUB。默认为 false 。 Aspose.Words 默认不显示页边距区域。如果任何元素被文档边缘完全或部分剪裁，则可以使用此选项扩展显示区域。

**退货:**
boolean - 对应的布尔值。
### getExportPageSetup() {#getExportPageSetup--}
```
public boolean getExportPageSetup()
```


指定是否将页面设置导出为 HTML、MHTML 或 EPUB。默认为 false 。

每个[Section](../../com.aspose.words/section)在 Aspose.Words 文档模型中通过以下方式提供页面设置信息[PageSetup](../../com.aspose.words/pagesetup)班级。当您将文档导出为 HTML 格式时，您可能需要保留此信息以供进一步使用。特别是，页面设置对于渲染到分页媒体（打印）或随后转换为本地 Microsoft Word 文件格式（DOCX、DOC、RTF、WML）可能很重要。

在大多数情况下，HTML 旨在用于在不执行分页的浏览器中查看。所以这个功能默认是不活动的。

**退货:**
boolean - 对应的布尔值。
### getExportRelativeFontSize() {#getExportRelativeFontSize--}
```
public boolean getExportRelativeFontSize()
```


指定保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。默认为 false 。

在许多现有文档（HTML、IDPF EPUB）中，字体大小以相对单位指定。这允许应用程序在查看/处理文档时调整文本大小。例如，Microsoft Internet Explorer 有“查看->文本大小”子菜单，Adobe Digital Editions 有两个按钮：增加/减小文本大小。如果您希望此功能正常工作，请设置[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-)属性为 true 。

Aspose Words 文档模型包含并且仅使用绝对字体大小单位进行操作。相对单位需要从一些初始（标准）大小重新计算的额外逻辑。字体大小**Normal**文档样式作为标准。例如，如果**Normal**有 12pt 字体和一些文本是 18pt 那么它将被输出为**1.5em.**到 HTML。

启用此选项后，文本以外的文档元素仍将具有绝对大小。一些与文本相关的属性也可能被绝对表达。特别是，使用“精确”规则指定的行距可能会在缩放文本时产生不需要的结果。因此，在导出时应正确设计和测试源文档[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-)设置为 true 。

**退货:**
boolean - 对应的布尔值。
### getExportRoundtripInformation() {#getExportRoundtripInformation--}
```
public boolean getExportRoundtripInformation()
```


指定保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。对于 HTML，默认值为 true，对于 MHTML 和 EPUB，默认值为 false。

保存往返信息允许在将 HTML 文档加载回[Document](../../com.aspose.words/document)目的。

当 true 时，往返信息导出为 -aw-\* 对应 HTML 元素的 CSS 属性。

如果为 false ，则不会将往返信息输出到生成的文件中。

**退货:**
boolean - 对应的布尔值。
### getExportShapesAsSvg() {#getExportShapesAsSvg--}
```
public boolean getExportShapesAsSvg()
```


控制是否[Shape](../../com.aspose.words/shape)保存为 HTML、MHTML、EPUB 或 AZW3 时，节点将转换为 SVG 图像。默认值为 false 。

如果此选项设置为 true ，[Shape](../../com.aspose.words/shape)节点作为元素导出。否则，它们将呈现为位图并导出为![图1][] 元素。


[图1]： 

**退货:**
boolean - 对应的布尔值。
### getExportTextInputForm字段AsText() {#getExportTextInputForm字段AsText--}
```
public boolean getExportTextInputForm字段AsText()
```


控制文本输入表单字段如何保存为 HTML 或 MHTML。默认值为 false 。

当设置为 true 时，将文本输入表单字段导出为普通文本。当为 false 时，将 Word 文本输入表单字段导出为 HTML 中的 INPUT 元素。

导出到 EPUB 时，由于此格式的要求，文本输入表单字段始终保存为文本。

**退货:**
boolean - 对应的布尔值。
### getExportTocPageNumbers() {#getExportTocPageNumbers--}
```
public boolean getExportTocPageNumbers()
```


指定在保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。默认值为 false 。

**退货:**
boolean - 对应的布尔值。
### getExportXhtmlTransitional() {#getExportXhtmlTransitional--}
```
public boolean getExportXhtmlTransitional()
```


指定保存为 HTML 或 MHTML 时是否编写 DOCTYPE 声明。当为 true 时，在根元素之前的文档中写入 DOCTYPE 声明。默认值为 false 。保存到 EPUB 或 HTML5 时（[HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion\#HTML-5)) DOCTYPE 声明总是被写入。

无论此设置如何，Aspose.Words 始终编写格式良好的 HTML。

当为 true 时，HTML 输出文档的开头将如下所示：

```

 
 
 
 
```

Aspose.Words 旨在根据 XHTML 1.0 过渡规范输出 XHTML，但输出并不总是根据 DTD 进行验证。 Microsoft Word 文档中的某些结构很难或不可能映射到将根据 XHTML 模式进行验证的文档。例如，XHTML 不允许嵌套列表（UL 不能嵌套在另一个 UL 元素中），但在 Microsoft Word 文档中，多级列表经常出现。

**退货:**
boolean - 对应的布尔值。
### getFontResourcesSubsettingSizeThreshold() {#getFontResourcesSubsettingSizeThreshold--}
```
public int getFontResourcesSubsettingSizeThreshold()
```


控制保存为 HTML、MHTML 或 EPUB 时需要子集的字体资源。默认为 0 。

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)允许将字体导出为辅助文件或作为输出包的一部分。如果文档使用多种字体，尤其是使用大量字形，则输出大小会显着增长。字体子集通过过滤掉当前文档未使用的字形来减小导出字体资源的大小。

字体子集的工作方式如下：

 *  默认情况下，所有导出的字体都是子集。
 *  环境[getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-)为正值指示 Aspose.Words 对文件大小大于指定值的字体进行子集化。
 *  将属性设置为抑制字体子集。

**Important!**导出字体资源时，应考虑字体许可问题。希望通过可下载字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可的范围内。许多商业字体目前不允许以任何形式从网络下载其字体。涵盖某些字体的许可协议特别指出，使用**@font-face**CSS 样式表中的规则是不允许的。字体子集也可能违反许可条款。

**退货:**
int - 对应的 int 值。
### getFontSavingCallback() {#getFontSavingCallback--}
```
public IFontSavingCallback getFontSavingCallback()
```


允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存字体。

**退货:**
[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) - 相应的[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback)价值。
### getFontsFolder() {#getFontsFolder--}
```
public String getFontsFolder()
```


指定将文档导出为 HTML 时保存字体的物理文件夹。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)以 HTML 格式和[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)设置为 true ，Aspose.Words 需要将文档中使用的字体保存为独立文件。[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)允许您指定字体的保存位置和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)允许指定如何构造字体 URI。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认将字体保存在保存文档文件的同一文件夹中。利用[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有保存字体的文件夹，但仍需要将字体保存在某处。在这种情况下，您需要在[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)属性或通过[getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getFontSavingCallback--) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setFontSavingCallback-com.aspose.words.IFontSavingCallback-)事件处理程序。

如果指定的文件夹[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)不存在，会自动创建。

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)是另一种指定应保存字体的文件夹的方法。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getFontsFolderAlias() {#getFontsFolderAlias--}
```
public String getFontsFolderAlias()
```


指定用于构造写入 HTML 文档的字体 URI 的文件夹的名称。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)以 HTML 格式和[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)设置为 true ，Aspose.Words 需要将文档中使用的字体保存为独立文件。[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)允许您指定字体的保存位置和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)允许指定如何构造字体 URI。

如果[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)不是空字符串，那么写入 HTML 的字体 URI 将是*FontsFolderAlias +* . 

如果[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)是一个空字符串，那么写入 HTML 的字体 URI 将是*FontsFolder +* . 

如果[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)被设定为 '。' （点），那么无论其他选项如何，字体文件名都将写入没有路径的 HTML。

指定文件夹名称以构造字体 URI 的另一种方法是使用[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getHtmlVersion() {#getHtmlVersion--}
```
public int getHtmlVersion()
```


指定将文档保存为 HTML 或 MHTML 时应使用的 HTML 标准版本。默认值为[HtmlVersion.XHTML](../../com.aspose.words/htmlversion\#XHTML).

**退货:**
int - 对应的 int 值。返回值是以下之一[HtmlVersion](../../com.aspose.words/htmlversion)常数。
### getImageResolution() {#getImageResolution--}
```
public int getImageResolution()
```


指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。默认为 96 dpi。

此属性会在以下情况下影响光栅图像[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)是 true 并且效果图元文件导出为光栅图像。某些图像属性（例如裁剪或旋转）需要保存转换后的图像，在这种情况下，转换后的图像以给定的分辨率创建。

**退货:**
int - 对应的 int 值。
### getImageSavingCallback() {#getImageSavingCallback--}
```
public IImageSavingCallback getImageSavingCallback()
```


允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存图像。

**退货:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) - 相应的[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback)价值。
### getImagesFolder() {#getImagesFolder--}
```
public String getImagesFolder()
```


指定将文档导出为 HTML 格式时保存图像的物理文件夹。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)在 HTML 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)允许您指定图像的保存位置和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)允许指定如何构建图像 URI。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认情况下会将图像保存在保存文档文件的同一文件夹中。利用[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)覆盖此行为。

如果将文档保存到流中，Aspose.Words 没有保存图像的文件夹，但仍需要将图像保存在某个位置。在这种情况下，您需要在[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)属性或通过[getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-)事件处理程序。

如果指定的文件夹[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)不存在，会自动创建。

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)是另一种指定应保存图像的文件夹的方法。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getImagesFolderAlias() {#getImagesFolderAlias--}
```
public String getImagesFolderAlias()
```


指定用于构造写入 HTML 文档的图像 URI 的文件夹的名称。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)在 HTML 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)允许您指定图像的保存位置和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)允许指定如何构建图像 URI。

如果[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)不是空字符串，则写入 HTML 的图像 URI 将是*ImagesFolderAlias + ![Image 1][]*.

如果[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)是一个空字符串，那么写入 HTML 的图像 URI 将是*ImagesFolder + ![Image 1][]*.

如果[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)被设定为 '。' （点），则无论其他选项如何，图像文件名都将写入没有路径的 HTML。

指定文件夹名称以构造图像 URI 的另一种方法是使用[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).


[图1]： 

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


获取一个值，该值确定如何呈现墨迹 (InkML) 对象。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**退货:**
int - 确定如何呈现墨水 (InkML) 对象的值。返回值是以下之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


获取确定是否应在保存文档之前执行内存优化的值。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的节省时间为代价来保存大型文档。

**退货:**
boolean - 确定是否应在保存文档之前执行内存优化的值。
### getMetafileFormat() {#getMetafileFormat--}
```
public int getMetafileFormat()
```


指定导出为 HTML、MHTML 或 EPUB 时以何种格式保存元文件。默认值为[HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat\#PNG)，这意味着元文件被渲染为光栅 PNG 图像。

HTML 浏览器本身不会显示元文件。默认情况下，Aspose.Words 在导出为 HTML 时会将 WMF 和 EMF 图像转换为 PNG 文件。其他选项是将元文件转换为 SVG 图像或按原样导出它们而不进行转换。

如果将元文件图像导出为未经转换的 HTML，则某些图像转换（尤其是图像裁剪）将不会应用于这些图像。

**退货:**
int - 对应的 int 值。返回值是以下之一[HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat)常数。
### getOfficeMathOutputMode() {#getOfficeMathOutputMode--}
```
public int getOfficeMathOutputMode()
```


控制如何将 OfficeMath 对象导出为 HTML、MHTML 或 EPUB。默认值为 HtmlOfficeMathOutputMode.Image 。

**退货:**
int - 对应的 int 值。返回值是以下之一[HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode)常数。
### getPrettyFormat() {#getPrettyFormat--}
```
public boolean getPrettyFormat()
```


如果为 true ，则在适用的情况下输出漂亮的格式。默认值为**false**.

调成**true**使 HTML、MHTML、EPUB、WordML、RTF、DOCX 和 ODT 输出具有人类可读性。用于测试或调试。

**退货:**
boolean - 对应的布尔值。
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentSavingCallback getProgressCallback()
```


在保存文档期间调用并接受有关保存进度的数据。

保存到时报告进度[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW)， 或者[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**退货:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - 相应的[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback)价值。
### getResolveFontNames() {#getResolveFontNames--}
```
public boolean getResolveFontNames()
```


指定文档中使用的字体系列名称是否根据[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)当被写入基于 HTML 的格式时。

默认情况下，此选项设置为 false，并且字体系列名称将写入源文档中指定的 HTML。那是，[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)被忽略并且不执行字体系列名称的解析或替换。

如果此选项设置为 true ，Aspose.Words 使用[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)将源文档中指定的每个字体系列名称解析为可用字体系列的名称，并根据需要执行字体替换。

**退货:**
boolean - 对应的布尔值。
### getResourceFolder() {#getResourceFolder--}
```
public String getResourceFolder()
```


指定将文档导出为 HTML 时保存所有资源（如图像、字体和外部 CSS）的物理文件夹。默认为空字符串。

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)是指定应写入所有资源的文件夹的最简单方法。另一种方法是使用单个属性[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)， 和[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)优先级低于通过指定的文件夹[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)， 和[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).例如，如果两者[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)和[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)指定，字体将被保存到[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) 而图像和 CSS 将被保存到[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

如果指定的文件夹[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)不存在，会自动创建。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getResourceFolderAlias() {#getResourceFolderAlias--}
```
public String getResourceFolderAlias()
```


指定用于构造写入 HTML 文档的所有资源的 URI 的文件夹的名称。默认为空字符串。

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)是指定如何构造所有资源文件的 URI 的最简单方法。可以通过分别为图像和字体指定相同的信息[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)属性，分别。但是，CSS 没有单独的属性。

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)优先级低于[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-).例如，如果两者[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)指定，字体的 URI 将使用[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) 而图像和 CSS 的 URI 将使用[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

如果[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)为空，则[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)属性值将用于构造资源 URI。

如果[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)被设定为 '。' （点），资源 URI 将仅包含文件名，不包含任何路径。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


如果使用此保存选项对象，则指定保存文档的格式。可[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3).

**退货:**
int - 对应的 int 值。返回值是以下之一[SaveFormat](../../com.aspose.words/saveformat)常数。
### getScaleImageToShapeSize() {#getScaleImageToShapeSize--}
```
public boolean getScaleImageToShapeSize()
```


指定当导出为 HTML、MHTML 或 EPUB 时，图像是否由 Aspose.Words 缩放到边界形状大小。默认值为 true 。

Microsoft Word 文档中的图像是一种形状。形状有大小，图像有自己的大小。尺寸没有直接联系。例如，图像可以是 1024x786 像素，但显示该图像的形状可以是 400x300 点。

为了在浏览器中显示图像，必须将其缩放到形状大小。这[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)属性控制图像缩放发生的位置：在 Aspose.Words 中导出到 HTML 时或在浏览器中显示文档时。

什么时候[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)为 true 时，图像由 Aspose.Words 在导出到 HTML 期间使用高质量缩放进行缩放。什么时候[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)为 false ，图像以其原始大小输出，浏览器必须对其进行缩放。

通常，浏览器会进行快速且质量较差的缩放。因此，您通常会在浏览器中获得更好的显示质量和更小的文件大小[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)是的，但更好的打印质量和更快的转换时[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)是假的。

**退货:**
boolean - 对应的布尔值。
### getTableWidthOutputMode() {#getTableWidthOutputMode--}
```
public int getTableWidthOutputMode()
```


控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。默认值为[HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode\#ALL).

在 HTML 格式中，表格、行和单元格元素 ( 

    | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.
 
 当您使用 Aspose.Words 将文档转换为 HTML 时，您可能希望控制表格、行和单元格宽度的导出方式，以影响结果文档在可视代理（例如浏览器或查看器）中的显示方式。
 
 使用此属性作为过滤器来指定将哪些表格宽度值导出到目标文档中。例如，如果您要将文档转换为 EPUB 并打算在移动阅读设备上查看文档，那么您可能希望避免导出绝对宽度值。为此，您需要指定输出模式[HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode\#RELATIVE-ONLY)或者[HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode\#NONE)因此移动设备上的查看器可以尽可能地布置表格以适应屏幕的宽度。|

**退货:**
int - 对应的 int 值。返回值是以下之一[HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode)常数。
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。默认情况下，此属性为 null，并且不使用临时文件。

当 Aspose.Words 保存文档时，它需要创建临时的内部结构。默认情况下，这些内部结构是在内存中创建的，并且在保存文档时内存使用量会在短时间内达到峰值。保存完成后，内存将被垃圾收集器释放和回收。

如果您要保存一个非常大的文档（数千页）和/或同时处理许多文档，那么保存期间的内存峰值可能会非常显着，从而导致系统抛出 java.lang.IndexOutOfBoundsException。使用指定临时文件夹[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)将导致 Aspose.Words 将内部结构保存在临时文件而不是内存中。它会减少保存期间的内存使用量，但会降低保存性能。

文件夹必须存在且可写，否则会抛出异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty--}
```
public boolean getUpdateCreatedTimeProperty()
```


获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。默认值为假；

**退货:**
 boolean - 确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。
### getUpdate字段() {#getUpdate字段--}
```
public boolean getUpdate字段()
```


获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为**true**.允许指定是否模仿 MS Word 行为。

**退货:**
boolean - 确定在将文档保存为固定页面格式之前是否应更新某些类型的字段的值。
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty--}
```
public boolean getUpdateLastPrintedProperty()
```


获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。

**退货:**
 boolean - 确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty--}
```
public boolean getUpdateLastSavedTimeProperty()
```


获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。

**退货:**
 boolean - 确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。
### getUpdateSdtContent() {#getUpdateSdtContent--}
```
public boolean getUpdateSdtContent()
```


获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。默认值为 false 。

**退货:**
 boolean - 确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。
### getUseAntiAliasing() {#getUseAntiAliasing--}
```
public boolean getUseAntiAliasing()
```


获取一个值，该值确定是否使用抗锯齿进行渲染。

默认值为 false 。当此值设置为 true 时，将使用抗锯齿进行渲染。

当文档导出为以下格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) .当文档导出到[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)和[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式 此选项用于光栅图像。

**退货:**
boolean - 确定是否使用抗锯齿进行渲染的值。
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


获取确定是否使用高质量（即慢速）渲染算法的值。默认值为 false 。

当文档导出为图像格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**退货:**
boolean - 确定是否使用高质量的值（即
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean-}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


设置一个布尔值，指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值为**false**.

请注意，Word 不嵌入 PostScript 字体，但可以打开嵌入了这种类型字体的文档。

此选项仅在以下情况下有效[FontInfoCollection.getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [FontInfoCollection.setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)的[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性设置为 true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示当在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |

### setAllowNegativeIndent(boolean value) {#setAllowNegativeIndent-boolean-}
```
public void setAllowNegativeIndent(boolean value)
```


指定在保存为 HTML、MHTML 或 EPUB 时是否规范段落的负左缩进和右缩进。默认值为 false 。

当不允许负缩进时，它将作为零边距导出到 HTML。当允许负缩进时，段落可能会部分显示在浏览器窗口之外。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCss班级NamePrefix(String value) {#setCss班级NamePrefix-java.lang.String-}
```
public void setCss班级NamePrefix(String value)
```


指定添加到所有 CSS 类名称的前缀。默认值为空字符串，生成的 CSS 类名没有公共前缀。

如果此值不为空，Aspose.Words 生成的所有 CSS 类都将以指定的前缀开头。这可能很有用，例如，如果您将自定义 CSS 添加到生成的文档并希望防止类名冲突。

如果该值不为 null 或为空，则它必须是有效的 CSS 标识符。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setCssSavingCallback(ICssSavingCallback value) {#setCssSavingCallback-com.aspose.words.ICssSavingCallback-}
```
public void setCssSavingCallback(ICssSavingCallback value)
```


允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存 CSS 样式。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [ICssSavingCallback](../../com.aspose.words/icsssavingcallback) | 相应的[ICssSavingCallback](../../com.aspose.words/icsssavingcallback)价值。 |

### setCssStyleSheetFileName(String value) {#setCssStyleSheetFileName-java.lang.String-}
```
public void setCssStyleSheetFileName(String value)
```


指定将文档导出为 HTML 时写入的层叠样式表 (CSS) 文件的路径和名称。默认为空字符串。

此属性仅在将文档保存为 HTML 格式并且使用请求外部 CSS 样式表时才有效[getCssStyleSheet类型()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheet类型--) / [setCssStyleSheet类型(int)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheet类型-int-).

如果此属性为空，则 CSS 文件将保存到与 HTML 文档同名但扩展名为“.css”的同一文件夹中。

如果此属性中仅指定路径但未指定文件名，则 CSS 文件将保存到指定文件夹中，并与 HTML 文档同名，但扩展名为“.css”。

如果此属性指定的文件夹不存在，则会在保存 CSS 文件之前自动创建。

指定保存外部 CSS 文件的文件夹的另一种方法是使用[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setCssStyleSheet类型(int value) {#setCssStyleSheet类型-int-}
```
public void setCssStyleSheet类型(int value)
```


指定如何将 CSS（层叠样式表）样式导出为 HTML、MHTML 或 EPUB。默认值为[CssStyleSheet类型.INLINE](../../com.aspose.words/cssstylesheettype\#INLINE)对于 HTML/MHTML 和[CssStyleSheet类型.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL)对于 EPUB。

仅当保存为 HTML 时才支持将 CSS 样式表保存到外部文件中。当您导出为其中一种容器格式（EPUB 或 MHTML）并指定[CssStyleSheet类型.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL)CSS 文件将被封装到输出包中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[CssStyleSheet类型](../../com.aspose.words/cssstylesheettype)常数。 |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


设置默认模板的路径（包括文件名）。此属性的默认值为**empty string**.如果指定，此路径用于加载模板时[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-)是真的，但是[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)是空的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 默认模板的路径（包括文件名）。 |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int-}
```
public void setDml3DEffectsRenderingMode(int value)
```


设置确定如何渲染 3D 效果的值。默认值为[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何渲染 3D 效果的值。该值必须是以下之一[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode)常数。 |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


设置一个值，确定如何呈现 DrawingML 效果。默认值为[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

当文档导出为固定页面格式时使用此属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现 DrawingML 效果的值。该值必须是以下之一[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode)常数。 |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int-}
```
public void setDmlRenderingMode(int value)
```


设置一个值，确定如何呈现 DrawingML 形状。默认值为[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

当文档导出为固定页面格式时使用此属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现 DrawingML 形状的值。该值必须是以下之一[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode)常数。 |

### setDocumentPartSavingCallback(IDocumentPartSavingCallback value) {#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback-}
```
public void setDocumentPartSavingCallback(IDocumentPartSavingCallback value)
```


允许控制将文档保存为 HTML 或 EPUB 时如何保存文档部分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) | 相应的[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback)价值。 |

### setDocumentSplitCriteria(int value) {#setDocumentSplitCriteria-int-}
```
public void setDocumentSplitCriteria(int value)
```


指定在保存到时应如何拆分文档[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式。默认为[DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria\#NONE)对于 HTML 和[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH)适用于 EPUB 和 AZW3。

通常，您希望将文档作为单个文件保存为 HTML。但在某些情况下，最好将输出拆分为几个较小的 HTML 页面。保存为 HTML 格式时，这些页面将输出到单个文件或流中。当保存为 EPUB 格式时，它们将被合并到相应的包中。

以 MHTML 格式保存时无法拆分文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是按位组合[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria)常数。 |

### setDocumentSplitHeadingLevel(int value) {#setDocumentSplitHeadingLevel-int-}
```
public void setDocumentSplitHeadingLevel(int value)
```


指定拆分文档的最大标题级别。默认值为 2 。

什么时候[getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-)包括[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH)并且此属性设置为 1 到 9 之间的值，文档将在使用格式化的段落处拆分**Heading 1**, **Heading 2** , **Heading 3**等样式直到指定的标题级别。

默认情况下，仅**Heading 1**和**Heading 2**段落导致文档被拆分。将此属性设置为零将导致文档根本不会在标题段落处拆分。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setEpubNavigationMapLevel(int value) {#setEpubNavigationMapLevel-int-}
```
public void setEpubNavigationMapLevel(int value)
```


指定导出为 IDPF EPUB 格式时填充到导航地图的最大标题级别。默认值为 3 。

IDPF EPUB 格式的导航图允许用户代理通过文档结构提供简单的导航方式。通常导航点对应于文档中的标题。将标题填充到级别**N**将此值分配给[getEpubNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions\#getEpubNavigationMapLevel--) / [setEpubNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions\#setEpubNavigationMapLevel-int-).

默认情况下，会填充三个级别的标题：样式段落**Heading 1**, **Heading 2**和**Heading 3**.您可以将此属性设置为 1 到 9 之间的值，以请求相应的最大级别。将其设置为零会将导航图减少为仅文档根或文档部分的根。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setExportCidUrlsForMhtmlResources(boolean value) {#setExportCidUrlsForMhtmlResources-boolean-}
```
public void setExportCidUrlsForMhtmlResources(boolean value)
```


指定是否使用 CID (Content-ID) URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。默认值为 false 。

此选项仅影响保存为 MHTML 的文档。

默认情况下，MHTML 文档中的资源由文件名（例如，“image.png”）引用，这些文件名与 MIME 部分的“Content-Location”标题相匹配。

此选项启用另一种方法，其中对资源文件的引用被写入 CID (Content-ID) URL（例如，“cid:image.png”）并与“Content-ID”标头匹配。

理论上，这两种引用方法之间应该没有区别，并且它们中的任何一种都应该在任何浏览器或邮件代理中都可以正常工作。然而，在实践中，一些代理无法通过文件名获取资源。如果您的浏览器或邮件代理拒绝加载 MTHML 文档中包含的资源（不显示图像或不加载 CSS 样式），请尝试使用 CID URL 导出文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportDocumentProperties(boolean value) {#setExportDocumentProperties-boolean-}
```
public void setExportDocumentProperties(boolean value)
```


指定是否将内置和自定义文档属性导出为 HTML、MHTML 或 EPUB。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportDropDownForm字段AsText(boolean value) {#setExportDropDownForm字段AsText-boolean-}
```
public void setExportDropDownForm字段AsText(boolean value)
```


控制如何将下拉表单字段保存为 HTML 或 MHTML。默认值为 false 。

当设置为 true 时，将下拉表单字段导出为普通文本。当 false 时，将下拉表单字段导出为 HTML 中的 SELECT 元素。

导出到 EPUB 时，由于此格式的要求，文本下拉表单字段始终保存为文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportFontResources(boolean value) {#setExportFontResources-boolean-}
```
public void setExportFontResources(boolean value)
```


指定字体资源是否应导出为 HTML、MHTML 或 EPUB。默认为 false 。

导出字体资源允许独立于给定用户环境中可用的字体的一致文档渲染。

如果[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)设置为 true ，主 HTML 文档将通过 CSS 3 引用每种字体**@font-face**at-rule 和 fonts 将作为单独的文件输出。导出为 IDPF EPUB 或 MHTML 格式时，字体将与其他附属文件一起嵌入到相应的包中。

如果[getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions\#getExportFontsAsBase64--) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontsAsBase64-boolean-)设置为 true ，字体将不会保存到单独的文件中。相反，它们将被嵌入**@font-face**Base64 编码中的 at 规则。

**Important!**导出字体资源时，应考虑字体许可问题。希望通过可下载字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可的范围内。许多商业字体目前不允许以任何形式从网络下载其字体。涵盖某些字体的许可协议特别指出，使用**@font-face**CSS 样式表中的规则是不允许的。字体子集也可能违反许可条款。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportFontsAsBase64(boolean value) {#setExportFontsAsBase64-boolean-}
```
public void setExportFontsAsBase64(boolean value)
```


指定字体资源是否应以 Base64 编码嵌入到 HTML。默认为 false 。

默认情况下，字体被写入单独的文件。如果此选项设置为 true ，字体将以 Base64 编码嵌入到文档的 CSS 中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。默认值为**true**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportHeadersFootersMode(int value) {#setExportHeadersFootersMode-int-}
```
public void setExportHeadersFootersMode(int value)
```


指定页眉和页脚如何输出到 HTML、MHTML 或 EPUB。默认值为[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION)对于 HTML/MHTML 和[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE)对于 EPUB。

很难将页眉和页脚有意义地输出到 HTML，因为 HTML 没有分页。

当这个属性是[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION)Aspose.Words 只导出每个部分开头和结尾的主要页眉和页脚。

几时[ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER)仅导出第一个主页眉和最后一个主页脚（包括链接到上一个页脚）。

您可以通过将此属性设置为来完全禁用页眉和页脚的导出[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode)常数。 |

### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean-}
```
public void setExportImagesAsBase64(boolean value)
```


指定图像是否以 Base64 格式保存到输出 HTML、MHTML 或 EPUB。默认为 false 。

当此属性设置为 true 时，图像数据将直接导出到**img**不会创建元素和单独的文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportLanguageInformation(boolean value) {#setExportLanguageInformation-boolean-}
```
public void setExportLanguageInformation(boolean value)
```


指定是否将语言信息导出为 HTML、MHTML 或 EPUB。默认为 false 。

当此属性设置为 true 时，Aspose.Words 输出**lang**指定语言的文档元素上的 HTML 属性。这可能需要保留与语言相关的语义。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportListLabels(int value) {#setExportListLabels-int-}
```
public void setExportListLabels(int value)
```


控制列表标签如何输出到 HTML、MHTML 或 EPUB。默认值为[ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels\#AUTO).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[ExportListLabels](../../com.aspose.words/exportlistlabels)常数。 |

### setExportOriginalUrlForLinkedImages(boolean value) {#setExportOriginalUrlForLinkedImages-boolean-}
```
public void setExportOriginalUrlForLinkedImages(boolean value)
```


指定是否应将原始 URL 用作链接图像的 URL。默认值为 false 。

如果值设置为 true[ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)值用作链接图像的 URL，并且链接图像未加载到文档的文件夹中或[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-).

如果值设置为 false 链接图像被加载到文档的文件夹或[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)每个链接图像的 URL 是根据文档的文件夹构建的，[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)特性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportPageMargins(boolean value) {#setExportPageMargins-boolean-}
```
public void setExportPageMargins(boolean value)
```


指定页边距是否导出为 HTML、MHTML 或 EPUB。默认为 false 。 Aspose.Words 默认不显示页边距区域。如果任何元素被文档边缘完全或部分剪裁，则可以使用此选项扩展显示区域。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportPageSetup(boolean value) {#setExportPageSetup-boolean-}
```
public void setExportPageSetup(boolean value)
```


指定是否将页面设置导出为 HTML、MHTML 或 EPUB。默认为 false 。

每个[Section](../../com.aspose.words/section)在 Aspose.Words 文档模型中通过以下方式提供页面设置信息[PageSetup](../../com.aspose.words/pagesetup)班级。当您将文档导出为 HTML 格式时，您可能需要保留此信息以供进一步使用。特别是，页面设置对于渲染到分页媒体（打印）或随后转换为本地 Microsoft Word 文件格式（DOCX、DOC、RTF、WML）可能很重要。

在大多数情况下，HTML 旨在用于在不执行分页的浏览器中查看。所以这个功能默认是不活动的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportRelativeFontSize(boolean value) {#setExportRelativeFontSize-boolean-}
```
public void setExportRelativeFontSize(boolean value)
```


指定保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。默认为 false 。

在许多现有文档（HTML、IDPF EPUB）中，字体大小以相对单位指定。这允许应用程序在查看/处理文档时调整文本大小。例如，Microsoft Internet Explorer 有“查看->文本大小”子菜单，Adobe Digital Editions 有两个按钮：增加/减小文本大小。如果您希望此功能正常工作，请设置[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-)属性为 true 。

Aspose Words 文档模型包含并且仅使用绝对字体大小单位进行操作。相对单位需要从一些初始（标准）大小重新计算的额外逻辑。字体大小**Normal**文档样式作为标准。例如，如果**Normal**有 12pt 字体和一些文本是 18pt 那么它将被输出为**1.5em.**到 HTML。

启用此选项后，文本以外的文档元素仍将具有绝对大小。一些与文本相关的属性也可能被绝对表达。特别是，使用“精确”规则指定的行距可能会在缩放文本时产生不需要的结果。因此，在导出时应正确设计和测试源文档[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-)设置为 true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportRoundtripInformation(boolean value) {#setExportRoundtripInformation-boolean-}
```
public void setExportRoundtripInformation(boolean value)
```


指定保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。对于 HTML，默认值为 true，对于 MHTML 和 EPUB，默认值为 false。

保存往返信息允许在将 HTML 文档加载回[Document](../../com.aspose.words/document)目的。

当 true 时，往返信息导出为 -aw-\* 对应 HTML 元素的 CSS 属性。

如果为 false ，则不会将往返信息输出到生成的文件中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportShapesAsSvg(boolean value) {#setExportShapesAsSvg-boolean-}
```
public void setExportShapesAsSvg(boolean value)
```


控制是否[Shape](../../com.aspose.words/shape)保存为 HTML、MHTML、EPUB 或 AZW3 时，节点将转换为 SVG 图像。默认值为 false 。

如果此选项设置为 true ，[Shape](../../com.aspose.words/shape)节点作为元素导出。否则，它们将呈现为位图并导出为![图1][] 元素。


[图1]： 

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportTextInputForm字段AsText(boolean value) {#setExportTextInputForm字段AsText-boolean-}
```
public void setExportTextInputForm字段AsText(boolean value)
```


控制文本输入表单字段如何保存为 HTML 或 MHTML。默认值为 false 。

当设置为 true 时，将文本输入表单字段导出为普通文本。当为 false 时，将 Word 文本输入表单字段导出为 HTML 中的 INPUT 元素。

导出到 EPUB 时，由于此格式的要求，文本输入表单字段始终保存为文本。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportTocPageNumbers(boolean value) {#setExportTocPageNumbers-boolean-}
```
public void setExportTocPageNumbers(boolean value)
```


指定在保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportXhtmlTransitional(boolean value) {#setExportXhtmlTransitional-boolean-}
```
public void setExportXhtmlTransitional(boolean value)
```


指定保存为 HTML 或 MHTML 时是否编写 DOCTYPE 声明。当为 true 时，在根元素之前的文档中写入 DOCTYPE 声明。默认值为 false 。保存到 EPUB 或 HTML5 时（[HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion\#HTML-5)) DOCTYPE 声明总是被写入。

无论此设置如何，Aspose.Words 始终编写格式良好的 HTML。

当为 true 时，HTML 输出文档的开头将如下所示：

```

 
 
 
 
```

Aspose.Words 旨在根据 XHTML 1.0 过渡规范输出 XHTML，但输出并不总是根据 DTD 进行验证。 Microsoft Word 文档中的某些结构很难或不可能映射到将根据 XHTML 模式进行验证的文档。例如，XHTML 不允许嵌套列表（UL 不能嵌套在另一个 UL 元素中），但在 Microsoft Word 文档中，多级列表经常出现。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFontResourcesSubsettingSizeThreshold(int value) {#setFontResourcesSubsettingSizeThreshold-int-}
```
public void setFontResourcesSubsettingSizeThreshold(int value)
```


控制保存为 HTML、MHTML 或 EPUB 时需要子集的字体资源。默认为 0 。

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)允许将字体导出为辅助文件或作为输出包的一部分。如果文档使用多种字体，尤其是使用大量字形，则输出大小会显着增长。字体子集通过过滤掉当前文档未使用的字形来减小导出字体资源的大小。

字体子集的工作方式如下：

 *  默认情况下，所有导出的字体都是子集。
 *  环境[getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-)为正值指示 Aspose.Words 对文件大小大于指定值的字体进行子集化。
 *  将属性设置为抑制字体子集。

**Important!**导出字体资源时，应考虑字体许可问题。希望通过可下载字体机制使用特定字体的作者必须始终仔细验证其预期用途是否在字体许可的范围内。许多商业字体目前不允许以任何形式从网络下载其字体。涵盖某些字体的许可协议特别指出，使用**@font-face**CSS 样式表中的规则是不允许的。字体子集也可能违反许可条款。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setFontSavingCallback(IFontSavingCallback value) {#setFontSavingCallback-com.aspose.words.IFontSavingCallback-}
```
public void setFontSavingCallback(IFontSavingCallback value)
```


允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存字体。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) | 相应的[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback)价值。 |

### setFontsFolder(String value) {#setFontsFolder-java.lang.String-}
```
public void setFontsFolder(String value)
```


指定将文档导出为 HTML 时保存字体的物理文件夹。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)以 HTML 格式和[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)设置为 true ，Aspose.Words 需要将文档中使用的字体保存为独立文件。[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)允许您指定字体的保存位置和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)允许指定如何构造字体 URI。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认将字体保存在保存文档文件的同一文件夹中。利用[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有保存字体的文件夹，但仍需要将字体保存在某处。在这种情况下，您需要在[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)属性或通过[getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getFontSavingCallback--) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setFontSavingCallback-com.aspose.words.IFontSavingCallback-)事件处理程序。

如果指定的文件夹[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)不存在，会自动创建。

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)是另一种指定应保存字体的文件夹的方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setFontsFolderAlias(String value) {#setFontsFolderAlias-java.lang.String-}
```
public void setFontsFolderAlias(String value)
```


指定用于构造写入 HTML 文档的字体 URI 的文件夹的名称。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)以 HTML 格式和[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-)设置为 true ，Aspose.Words 需要将文档中使用的字体保存为独立文件。[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)允许您指定字体的保存位置和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)允许指定如何构造字体 URI。

如果[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)不是空字符串，那么写入 HTML 的字体 URI 将是*FontsFolderAlias +* . 

如果[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)是一个空字符串，那么写入 HTML 的字体 URI 将是*FontsFolder +* . 

如果[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)被设定为 '。' （点），那么无论其他选项如何，字体文件名都将写入没有路径的 HTML。

指定文件夹名称以构造字体 URI 的另一种方法是使用[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setHtmlVersion(int value) {#setHtmlVersion-int-}
```
public void setHtmlVersion(int value)
```


指定将文档保存为 HTML 或 MHTML 时应使用的 HTML 标准版本。默认值为[HtmlVersion.XHTML](../../com.aspose.words/htmlversion\#XHTML).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[HtmlVersion](../../com.aspose.words/htmlversion)常数。 |

### setImageResolution(int value) {#setImageResolution-int-}
```
public void setImageResolution(int value)
```


指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。默认为 96 dpi。

此属性会在以下情况下影响光栅图像[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)是 true 并且效果图元文件导出为光栅图像。某些图像属性（例如裁剪或旋转）需要保存转换后的图像，在这种情况下，转换后的图像以给定的分辨率创建。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback-}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


允许控制在将文档保存为 HTML、MHTML 或 EPUB 时如何保存图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) | 相应的[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback)价值。 |

### setImagesFolder(String value) {#setImagesFolder-java.lang.String-}
```
public void setImagesFolder(String value)
```


指定将文档导出为 HTML 格式时保存图像的物理文件夹。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)在 HTML 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)允许您指定图像的保存位置和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)允许指定如何构建图像 URI。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认情况下会将图像保存在保存文档文件的同一文件夹中。利用[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)覆盖此行为。

如果将文档保存到流中，Aspose.Words 没有保存图像的文件夹，但仍需要将图像保存在某个位置。在这种情况下，您需要在[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)属性或通过[getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-)事件处理程序。

如果指定的文件夹[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)不存在，会自动创建。

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)是另一种指定应保存图像的文件夹的方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setImagesFolderAlias(String value) {#setImagesFolderAlias-java.lang.String-}
```
public void setImagesFolderAlias(String value)
```


指定用于构造写入 HTML 文档的图像 URI 的文件夹的名称。默认为空字符串。

当你保存一个[Document](../../com.aspose.words/document)在 HTML 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)允许您指定图像的保存位置和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)允许指定如何构建图像 URI。

如果[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)不是空字符串，则写入 HTML 的图像 URI 将是*ImagesFolderAlias + ![Image 1][]*.

如果[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)是一个空字符串，那么写入 HTML 的图像 URI 将是*ImagesFolder + ![Image 1][]*.

如果[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)被设定为 '。' （点），则无论其他选项如何，图像文件名都将写入没有路径的 HTML。

指定文件夹名称以构造图像 URI 的另一种方法是使用[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).


[图1]： 

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setImlRenderingMode(int value) {#setImlRenderingMode-int-}
```
public void setImlRenderingMode(int value)
```


设置一个值，确定如何呈现墨水 (InkML) 对象。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现墨水 (InkML) 对象的值。该值必须是以下之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。 |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


设置值确定是否应在保存文档之前执行内存优化。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的节省时间为代价来保存大型文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否应在保存文档之前执行内存优化的值。 |

### setMetafileFormat(int value) {#setMetafileFormat-int-}
```
public void setMetafileFormat(int value)
```


指定导出为 HTML、MHTML 或 EPUB 时以何种格式保存元文件。默认值为[HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat\#PNG)，这意味着元文件被渲染为光栅 PNG 图像。

HTML 浏览器本身不会显示元文件。默认情况下，Aspose.Words 在导出为 HTML 时会将 WMF 和 EMF 图像转换为 PNG 文件。其他选项是将元文件转换为 SVG 图像或按原样导出它们而不进行转换。

如果将元文件图像导出为未经转换的 HTML，则某些图像转换（尤其是图像裁剪）将不会应用于这些图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat)常数。 |

### setOfficeMathOutputMode(int value) {#setOfficeMathOutputMode-int-}
```
public void setOfficeMathOutputMode(int value)
```


控制如何将 OfficeMath 对象导出为 HTML、MHTML 或 EPUB。默认值为 HtmlOfficeMathOutputMode.Image 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode)常数。 |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean-}
```
public void setPrettyFormat(boolean value)
```


如果为 true ，则在适用的情况下输出漂亮的格式。默认值为**false**.

调成**true**使 HTML、MHTML、EPUB、WordML、RTF、DOCX 和 ODT 输出具有人类可读性。用于测试或调试。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback-}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


在保存文档期间调用并接受有关保存进度的数据。

保存到时报告进度[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW)， 或者[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) | 相应的[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback)价值。 |

### setResolveFontNames(boolean value) {#setResolveFontNames-boolean-}
```
public void setResolveFontNames(boolean value)
```


指定文档中使用的字体系列名称是否根据[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)当被写入基于 HTML 的格式时。

默认情况下，此选项设置为 false，并且字体系列名称将写入源文档中指定的 HTML。那是，[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)被忽略并且不执行字体系列名称的解析或替换。

如果此选项设置为 true ，Aspose.Words 使用[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-)将源文档中指定的每个字体系列名称解析为可用字体系列的名称，并根据需要执行字体替换。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setResourceFolder(String value) {#setResourceFolder-java.lang.String-}
```
public void setResourceFolder(String value)
```


指定将文档导出为 HTML 时保存所有资源（如图像、字体和外部 CSS）的物理文件夹。默认为空字符串。

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)是指定应写入所有资源的文件夹的最简单方法。另一种方法是使用单个属性[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)， 和[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)优先级低于通过指定的文件夹[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-)， 和[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).例如，如果两者[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)和[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-)指定，字体将被保存到[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) 而图像和 CSS 将被保存到[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

如果指定的文件夹[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)不存在，会自动创建。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setResourceFolderAlias(String value) {#setResourceFolderAlias-java.lang.String-}
```
public void setResourceFolderAlias(String value)
```


指定用于构造写入 HTML 文档的所有资源的 URI 的文件夹的名称。默认为空字符串。

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)是指定如何构造所有资源文件的 URI 的最简单方法。可以通过分别为图像和字体指定相同的信息[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)属性，分别。但是，CSS 没有单独的属性。

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)优先级低于[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)和[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-).例如，如果两者[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)和[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-)指定，字体的 URI 将使用[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) 而图像和 CSS 的 URI 将使用[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

如果[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)为空，则[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-)属性值将用于构造资源 URI。

如果[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-)被设定为 '。' （点），资源 URI 将仅包含文件名，不包含任何路径。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


如果使用此保存选项对象，则指定保存文档的格式。可[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)或者[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[SaveFormat](../../com.aspose.words/saveformat)常数。 |

### setScaleImageToShapeSize(boolean value) {#setScaleImageToShapeSize-boolean-}
```
public void setScaleImageToShapeSize(boolean value)
```


指定当导出为 HTML、MHTML 或 EPUB 时，图像是否由 Aspose.Words 缩放到边界形状大小。默认值为 true 。

Microsoft Word 文档中的图像是一种形状。形状有大小，图像有自己的大小。尺寸没有直接联系。例如，图像可以是 1024x786 像素，但显示该图像的形状可以是 400x300 点。

为了在浏览器中显示图像，必须将其缩放到形状大小。这[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)属性控制图像缩放发生的位置：在 Aspose.Words 中导出到 HTML 时或在浏览器中显示文档时。

什么时候[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)为 true 时，图像由 Aspose.Words 在导出到 HTML 期间使用高质量缩放进行缩放。什么时候[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)为 false ，图像以其原始大小输出，浏览器必须对其进行缩放。

通常，浏览器会进行快速且质量较差的缩放。因此，您通常会在浏览器中获得更好的显示质量和更小的文件大小[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)是的，但更好的打印质量和更快的转换时[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)是假的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTableWidthOutputMode(int value) {#setTableWidthOutputMode-int-}
```
public void setTableWidthOutputMode(int value)
```


控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。默认值为[HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode\#ALL).

在 HTML 格式中，表格、行和单元格元素 ( 

    | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.
 
 当您使用 Aspose.Words 将文档转换为 HTML 时，您可能希望控制表格、行和单元格宽度的导出方式，以影响结果文档在可视代理（例如浏览器或查看器）中的显示方式。
 
 使用此属性作为过滤器来指定将哪些表格宽度值导出到目标文档中。例如，如果您要将文档转换为 EPUB 并打算在移动阅读设备上查看文档，那么您可能希望避免导出绝对宽度值。为此，您需要指定输出模式[HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode\#RELATIVE-ONLY)或者[HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode\#NONE)因此移动设备上的查看器可以尽可能地布置表格以适应屏幕的宽度。|

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode)常数。 |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。默认情况下，此属性为 null，并且不使用临时文件。

当 Aspose.Words 保存文档时，它需要创建临时的内部结构。默认情况下，这些内部结构是在内存中创建的，并且在保存文档时内存使用量会在短时间内达到峰值。保存完成后，内存将被垃圾收集器释放和回收。

如果您要保存一个非常大的文档（数千页）和/或同时处理许多文档，那么保存期间的内存峰值可能会非常显着，从而导致系统抛出 java.lang.IndexOutOfBoundsException。使用指定临时文件夹[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)将导致 Aspose.Words 将内部结构保存在临时文件而不是内存中。它会减少保存期间的内存使用量，但会降低保存性能。

文件夹必须存在且可写，否则会抛出异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean-}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。默认值为假；

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |

### setUpdate字段(boolean value) {#setUpdate字段-boolean-}
```
public void setUpdate字段(boolean value)
```


设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为**true**.允许指定是否模仿 MS Word 行为。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定在将文档保存为固定页面格式之前是否应更新某些类型的字段的值。 |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean-}
```
public void setUpdateLastPrintedProperty(boolean value)
```


设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean-}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean-}
```
public void setUpdateSdtContent(boolean value)
```


设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 价值决定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean-}
```
public void setUseAntiAliasing(boolean value)
```


设置一个值，确定是否使用抗锯齿进行渲染。

默认值为 false 。当此值设置为 true 时，将使用抗锯齿进行渲染。

当文档导出为以下格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) .当文档导出到[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)和[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式 此选项用于光栅图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否使用抗锯齿进行渲染的值。 |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean-}
```
public void setUseHighQualityRendering(boolean value)
```


设置一个值来确定是否使用高质量（即慢速）渲染算法。默认值为 false 。

当文档导出为图像格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 决定是否使用高质量的值（即 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
