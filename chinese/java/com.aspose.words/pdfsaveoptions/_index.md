---
title: PdfSaveOptions
second_title: Aspose.Words for Java API Reference
description: 可用于在将文档保存为格式时指定其他选项。
type: docs
weight: 461
url: /zh/java/com.aspose.words/pdfsaveoptions/
---

**遗产:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)

**所有实现的接口:**
java.lang.Cloneable
```
public class PdfSaveOptions extends FixedPageSaveOptions implements Cloneable
```

可用于在将文档保存到[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF)格式。

要了解更多信息，请访问**Specify Save Options**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [PdfSaveOptions()](#PdfSaveOptions--) | 初始化此类的新实例，该实例可用于将文档保存在[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF)格式。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | 创建适合给定文件名中指定的文件扩展名的类的保存选项对象。 |
| [deepClone()](#deepClone--) | 创建此对象的深层克隆。 |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [getAdditionalTextPositioning()](#getAdditionalTextPositioning--) | 一个标志，指定是否编写额外的文本定位运算符。 |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | 获取一个布尔值，该值指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [getCacheHeaderFooterShapes()](#getCacheHeaderFooterShapes--) | 获取一个值，该值确定是否缓存放置在文档页眉和页脚中的形状。 |
| [get班级()](#get班级--) |  |
| [getColorMode()](#getColorMode--) | 获取一个值，该值确定如何呈现颜色。 |
| [getCompliance()](#getCompliance--) | 指定输出文档的 PDF 标准合规级别。 |
| [getCreateNoteHyperlinks()](#getCreateNoteHyperlinks--) | 指定是否将正文故事中的脚注/尾注引用转换为活动超链接。 |
| [getCustomPropertiesExport()](#getCustomPropertiesExport--) | 获取确定方式的值[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。 |
| [getDefaultTemplate()](#getDefaultTemplate--) | 获取默认模板的路径（包括文件名）。 |
| [getDigitalSignatureDetails()](#getDigitalSignatureDetails--) | 获取用于签署输出 PDF 文档的详细信息。 |
| [getDisplayDocTitle()](#getDisplayDocTitle--) | 一个标志，指定窗口是否\\u2019s 标题栏应显示从文档信息字典的 Title 条目中获取的文档标题。 |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | 获取确定如何渲染 3D 效果的值。 |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | 获取一个值，该值确定如何呈现 DrawingML 效果。 |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | 获取一个值，该值确定如何呈现 DrawingML 形状。 |
| [getDownsampleOptions()](#getDownsampleOptions--) | 允许指定下采样选项。 |
| [getEmbedFullFonts()](#getEmbedFullFonts--) | 控制字体如何嵌入到生成的 PDF 文档中。 |
| [getEncryptionDetails()](#getEncryptionDetails--) | 获取加密输出 PDF 文档的详细信息。 |
| [getExportDocumentStructure()](#getExportDocumentStructure--) | 获取确定是否导出文档结构的值。 |
| [getExportGeneratorName()](#getExportGeneratorName--) | 如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 |
| [getExportLanguageToSpanTag()](#getExportLanguageToSpanTag--) | 获取一个值，该值确定是否在文档结构中创建“Span”标签以导出文本语言。 |
| [getFontEmbeddingMode()](#getFontEmbeddingMode--) | 指定字体嵌入模式。 |
| [getHeaderFooterBookmarksExportMode()](#getHeaderFooterBookmarksExportMode--) | 确定如何导出页眉/页脚中的书签。 |
| [getImageColorSpaceExportMode()](#getImageColorSpaceExportMode--) | 指定如何为 PDF 文档中的图像选择色彩空间。 |
| [getImageCompression()](#getImageCompression--) | 指定要用于文档中所有图像的压缩类型。 |
| [getImlRenderingMode()](#getImlRenderingMode--) | 获取一个值，该值确定如何呈现墨迹 (InkML) 对象。 |
| [getInterpolateImages()](#getInterpolateImages--) | 指示图像插值是否应由合格阅读器执行的标志。 |
| [getJpegQuality()](#getJpegQuality--) | 获取确定 PDF 文档中 JPEG 图像质量的值。 |
| [getMemoryOptimization()](#getMemoryOptimization--) | 获取确定是否应在保存文档之前执行内存优化的值。 |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | 允许指定元文件渲染选项。 |
| [getNumeralFormat()](#getNumeralFormat--) | 获取[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。 |
| [getOpenHyperlinksInNewWindow()](#getOpenHyperlinksInNewWindow--) | 获取一个值，该值确定是否强制在浏览器的新窗口（或选项卡）中打开输出 Pdf 文档中的超链接。 |
| [getOptimizeOutput()](#getOptimizeOutput--) | Flag 表示是否需要优化输出。 |
| [getOutlineOptions()](#getOutlineOptions--) | 允许指定大纲选项。 |
| [getPageMode()](#getPageMode--) | 指定 PDF 文档在 PDF 阅读器中打开时的显示方式。 |
| [getPageSavingCallback()](#getPageSavingCallback--) | 允许控制将文档导出为固定页面格式时如何保存单独的页面。 |
| [getPageSet()](#getPageSet--) | 获取要呈现的页面。 |
| [getPreblendImages()](#getPreblendImages--) | 获取一个值，该值确定是否将透明图像与黑色背景颜色预混合。 |
| [getPreserveForm字段()](#getPreserveForm字段--) | 指定是将 Microsoft Word 表单域保留为 PDF 中的表单域还是将它们转换为文本。 |
| [getPrettyFormat()](#getPrettyFormat--) | 如果为 true ，则在适用的情况下输出漂亮的格式。 |
| [getProgressCallback()](#getProgressCallback--) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [getSaveFormat()](#getSaveFormat--) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [getTempFolder()](#getTempFolder--) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [getTextCompression()](#getTextCompression--) | 指定要用于文档中所有文本内容的压缩类型。 |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdate字段()](#getUpdate字段--) | 获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateSdtContent()](#getUpdateSdtContent--) | 获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | 获取一个值，该值确定是否使用抗锯齿进行渲染。 |
| [getUseBookFoldPrintingSettings()](#getUseBookFoldPrintingSettings--) | 获取一个布尔值，指示是否应使用小册子打印布局保存文档（如果通过以下方式指定）[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [getUseCoreFonts()](#getUseCoreFonts--) | 获取一个值，该值确定是否将 True类型 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF 类型 1 字体。 |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | 获取确定是否使用高质量的值（即 |
| [getZoomBehavior()](#getZoomBehavior--) | 获取一个值，该值确定使用 PDF 查看器打开文档时应应用哪种类型的缩放。 |
| [getZoomFactor()](#getZoomFactor--) | 获取确定文档缩放系数（以百分比为单位）的值。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAdditionalTextPositioning(boolean value)](#setAdditionalTextPositioning-boolean-) | 一个标志，指定是否编写额外的文本定位运算符。 |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | 设置一个布尔值，指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [setCacheHeaderFooterShapes(boolean value)](#setCacheHeaderFooterShapes-boolean-) | 设置一个值，确定是否缓存放置在文档页眉和页脚中的形状。 |
| [setColorMode(int value)](#setColorMode-int-) | 设置一个值来确定如何呈现颜色。 |
| [setCompliance(int value)](#setCompliance-int-) | 指定输出文档的 PDF 标准合规级别。 |
| [setCreateNoteHyperlinks(boolean value)](#setCreateNoteHyperlinks-boolean-) | 指定是否将正文故事中的脚注/尾注引用转换为活动超链接。 |
| [setCustomPropertiesExport(int value)](#setCustomPropertiesExport-int-) | 设置确定方式的值[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。 |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | 设置默认模板的路径（包括文件名）。 |
| [setDigitalSignatureDetails(PdfDigitalSignatureDetails value)](#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-) | 设置用于签署输出 PDF 文档的详细信息。 |
| [setDisplayDocTitle(boolean value)](#setDisplayDocTitle-boolean-) | 一个标志，指定窗口是否\\u2019s 标题栏应显示从文档信息字典的 Title 条目中获取的文档标题。 |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | 设置确定如何渲染 3D 效果的值。 |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 效果。 |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 形状。 |
| [setDownsampleOptions(DownsampleOptions value)](#setDownsampleOptions-com.aspose.words.DownsampleOptions-) | 允许指定下采样选项。 |
| [setEmbedFullFonts(boolean value)](#setEmbedFullFonts-boolean-) | 控制字体如何嵌入到生成的 PDF 文档中。 |
| [setEncryptionDetails(PdfEncryptionDetails value)](#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails-) | 设置加密输出 PDF 文档的详细信息。 |
| [setExportDocumentStructure(boolean value)](#setExportDocumentStructure-boolean-) | 设置确定是否导出文档结构的值。 |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | 如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 |
| [setExportLanguageToSpanTag(boolean value)](#setExportLanguageToSpanTag-boolean-) | 设置一个值，确定是否在文档结构中创建“Span”标签以导出文本语言。 |
| [setFontEmbeddingMode(int value)](#setFontEmbeddingMode-int-) | 指定字体嵌入模式。 |
| [setHeaderFooterBookmarksExportMode(int value)](#setHeaderFooterBookmarksExportMode-int-) | 确定如何导出页眉/页脚中的书签。 |
| [setImageColorSpaceExportMode(int value)](#setImageColorSpaceExportMode-int-) | 指定如何为 PDF 文档中的图像选择色彩空间。 |
| [setImageCompression(int value)](#setImageCompression-int-) | 指定要用于文档中所有图像的压缩类型。 |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | 设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [setInterpolateImages(boolean value)](#setInterpolateImages-boolean-) | 指示图像插值是否应由合格阅读器执行的标志。 |
| [setJpegQuality(int value)](#setJpegQuality-int-) | 设置确定 PDF 文档中 JPEG 图像质量的值。 |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | 设置值确定是否应在保存文档之前执行内存优化。 |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | 允许指定元文件渲染选项。 |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) | 套[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。 |
| [setOpenHyperlinksInNewWindow(boolean value)](#setOpenHyperlinksInNewWindow-boolean-) | 设置一个值，确定是否强制在浏览器的新窗口（或选项卡）中打开输出 Pdf 文档中的超链接。 |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Flag 表示是否需要优化输出。 |
| [setPageMode(int value)](#setPageMode-int-) | 指定 PDF 文档在 PDF 阅读器中打开时的显示方式。 |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | 允许控制将文档导出为固定页面格式时如何保存单独的页面。 |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | 设置要呈现的页面。 |
| [setPreblendImages(boolean value)](#setPreblendImages-boolean-) | 设置一个值，确定是否将透明图像与黑色背景颜色预混合。 |
| [setPreserveForm字段(boolean value)](#setPreserveForm字段-boolean-) | 指定是将 Microsoft Word 表单域保留为 PDF 中的表单域还是将它们转换为文本。 |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | 如果为 true ，则在适用的情况下输出漂亮的格式。 |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [setSaveFormat(int value)](#setSaveFormat-int-) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [setTextCompression(int value)](#setTextCompression-int-) | 指定要用于文档中所有文本内容的压缩类型。 |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdate字段(boolean value)](#setUpdate字段-boolean-) | 设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) | 设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | 设置一个值，确定是否使用抗锯齿进行渲染。 |
| [setUseBookFoldPrintingSettings(boolean value)](#setUseBookFoldPrintingSettings-boolean-) | 设置一个布尔值，指示是否应使用小册子打印布局保存文档，如果它是通过指定的[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [setUseCoreFonts(boolean value)](#setUseCoreFonts-boolean-) | 设置一个值，确定是否将 True类型 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF 类型 1 字体。 |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | 设置一个值来确定是否使用高质量（即 |
| [setZoomBehavior(int value)](#setZoomBehavior-int-) | 设置一个值，用于确定使用 PDF 查看器打开文档时应应用的缩放类型。 |
| [setZoomFactor(int value)](#setZoomFactor-int-) | 设置确定文档缩放系数（以百分比为单位）的值。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfSaveOptions() {#PdfSaveOptions--}
```
public PdfSaveOptions()
```


初始化此类的新实例，该实例可用于将文档保存在[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF)格式。

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
### deepClone() {#deepClone--}
```
public PdfSaveOptions deepClone()
```


创建此对象的深层克隆。

**退货:**
[PdfSaveOptions](../../com.aspose.words/pdfsaveoptions)
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


确定指定对象的值是否与当前对象相等。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货:**
布尔值
### getAdditionalTextPositioning() {#getAdditionalTextPositioning--}
```
public boolean getAdditionalTextPositioning()
```


一个标志，指定是否编写额外的文本定位运算符。

如果为 true ，则会将其他文本定位运算符写入输出 PDF。这可能有助于克服某些打印机的文本定位不准确的问题。缺点是增加了 PDF 文档的大小。

默认值为 false 。

**退货:**
boolean - 对应的布尔值。
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


获取一个布尔值，该值指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值为**false**.

请注意，Word 不嵌入 PostScript 字体，但可以打开嵌入了这种类型字体的文档。

此选项仅在以下情况下有效[FontInfoCollection.getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [FontInfoCollection.setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)的[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性设置为 true 。

**退货:**
boolean - 一个布尔值，指示在保存文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。
### getCacheHeaderFooterShapes() {#getCacheHeaderFooterShapes--}
```
public boolean getCacheHeaderFooterShapes()
```


获取一个值，该值确定是否缓存放置在文档页眉和页脚中的形状。

默认值为 false 并且不缓存形状。

当值为 true 时，图形将作为 xObject 写入 PDF 文档。

某些形状不支持缓存（带有字段、书签、HRef 的形状）。

**退货:**
boolean - 确定是否缓存放置在文档页眉和页脚中的形状的值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColorMode() {#getColorMode--}
```
public int getColorMode()
```


获取一个值，该值确定如何呈现颜色。默认值为[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**退货:**
int - 确定颜色如何呈现的值。返回值是以下之一[ColorMode](../../com.aspose.words/colormode)常数。
### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


指定输出文档的 PDF 标准合规级别。

默认为[PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance\#PDF-17).

**退货:**
int - 对应的 int 值。返回值是以下之一[PdfCompliance](../../com.aspose.words/pdfcompliance)常数。
### getCreateNoteHyperlinks() {#getCreateNoteHyperlinks--}
```
public boolean getCreateNoteHyperlinks()
```


指定是否将正文故事中的脚注/尾注引用转换为活动超链接。点击后，超链接将指向相应的脚注/尾注。默认为 false 。

**退货:**
boolean - 对应的布尔值。
### getCustomPropertiesExport() {#getCustomPropertiesExport--}
```
public int getCustomPropertiesExport()
```


获取确定方式的值[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。

默认值为[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA)保存为 PDF/A 时不支持 value。[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD)将用于 PDF/A-1 和 PDF/A-2 和[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE)对于 PDF/A-4。

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD)保存为 PDF 2.0 时不支持 value。[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA)将被使用。

**退货:**
int - 确定方式的值[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。返回值是以下之一[PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport)常数。
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


获取默认模板的路径（包括文件名）。此属性的默认值为**empty string**.如果指定，此路径用于加载模板时[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-)是真的，但是[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)是空的。

**退货:**
java.lang.String - 默认模板的路径（包括文件名）。
### getDigitalSignatureDetails() {#getDigitalSignatureDetails--}
```
public PdfDigitalSignatureDetails getDigitalSignatureDetails()
```


获取用于签署输出 PDF 文档的详细信息。

默认值为空，输出文档不会被签名。当此属性设置为有效时[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails)对象，则输出的 PDF 文档将被数字签名。

**退货:**
[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) - 签署输出 PDF 文档的详细信息。
### getDisplayDocTitle() {#getDisplayDocTitle--}
```
public boolean getDisplayDocTitle()
```


一个标志，指定窗口是否\\u2019s 标题栏应显示从文档信息字典的 Title 条目中获取的文档标题。

如果为 false ，则标题栏应改为显示包含该文档的 PDF 文件的名称。

PDF/UA 合规性需要此标志。保存到 PDF/UA 时将自动使用 true 值。

默认值为 false 。

**退货:**
boolean - 对应的布尔值。
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

如果[getCompliance()](../../com.aspose.words/pdfsaveoptions\#getCompliance--) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions\#setCompliance-int-)被设定为[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A)或者[PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B) , 属性总是返回[DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode\#NONE).

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
### getDownsampleOptions() {#getDownsampleOptions--}
```
public DownsampleOptions getDownsampleOptions()
```


允许指定下采样选项。

**退货:**
[DownsampleOptions](../../com.aspose.words/downsampleoptions) - 相应的[DownsampleOptions](../../com.aspose.words/downsampleoptions)价值。
### getEmbedFullFonts() {#getEmbedFullFonts--}
```
public boolean getEmbedFullFonts()
```


控制字体如何嵌入到生成的 PDF 文档中。

默认值为 false ，这意味着字体在嵌入之前被子集化。如果您想保持输出文件的大小更小，子集化很有用。子集从字体中删除所有未使用的字形。

当此值设置为 true 时，将完整的字体文件嵌入到 PDF 中而不设置子集。这将导致更大的输出文件，但当您想稍后编辑生成的 PDF（例如添加更多文本）时，它可能是一个有用的选项。

某些字体很大（几兆字节）并且在没有子集的情况下嵌入它们会导致输出文档很大。

**退货:**
boolean - 对应的布尔值。
### getEncryptionDetails() {#getEncryptionDetails--}
```
public PdfEncryptionDetails getEncryptionDetails()
```


获取加密输出 PDF 文档的详细信息。

默认值为空，输出文档不会被加密。当此属性设置为有效时[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails)对象，则输出的 PDF 文档将被加密。

保存到基于 PDF 1.7 的合规性（包括 PDF/UA-1）时使用 AES-128 加密算法。保存到基于 PDF 2.0 的合规性时使用 AES-256 加密算法。

PDF/A 合规性禁止加密。保存为 PDF/A 时将忽略此选项。

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY)如果输出文档是加密的，则 PDF/UA 合规性需要许可。保存到 PDF/UA 时将自动使用此权限。

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY)PDF 2.0 格式不推荐使用权限。保存到 PDF 2.0 时将忽略此权限。

**退货:**
[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) - 加密输出 PDF 文档的详细信息。
### getExportDocumentStructure() {#getExportDocumentStructure--}
```
public boolean getExportDocumentStructure()
```


获取确定是否导出文档结构的值。

保存到 PDF/A-1a、PDF/A-2a 和 PDF/UA-1 时忽略此值，因为此合规性需要文档结构。

请注意，导出文档结构会显着增加内存消耗，尤其是对于大型文档。

**退货:**
boolean - 确定是否导出文档结构的值。
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。默认值为**true**.

**退货:**
boolean - 对应的布尔值。
### getExportLanguageToSpanTag() {#getExportLanguageToSpanTag--}
```
public boolean getExportLanguageToSpanTag()
```


获取一个值，该值确定是否在文档结构中创建“Span”标签以导出文本语言。

默认值为 false，并且“Lang”属性附加到页面内容流中的标记内容序列。

当值为 true 时，将为具有非默认语言的文本创建“Span”标签，并将“Lang”属性附加到此标签。

该值被忽略时[getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions\#getExportDocumentStructure--) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions\#setExportDocumentStructure-boolean-)是假的。

**退货:**
boolean - 确定是否在文档结构中创建“Span”标签以导出文本语言的值。
### getFontEmbeddingMode() {#getFontEmbeddingMode--}
```
public int getFontEmbeddingMode()
```


指定字体嵌入模式。

默认值为[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL).

此设置仅适用于 ANSI (Windows-1252) 编码的文本。如果文档包含非 ANSI 文本，则无论此设置如何，都将嵌入相应的字体。

 PDF/A 和 PDF/UA 合规性要求嵌入所有字体。[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL)保存为 PDF/A 和 PDF/UA 时将自动使用该值。

**退货:**
int - 对应的 int 值。返回值是以下之一[PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode)常数。
### getHeaderFooterBookmarksExportMode() {#getHeaderFooterBookmarksExportMode--}
```
public int getHeaderFooterBookmarksExportMode()
```


确定如何导出页眉/页脚中的书签。

默认值为[HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode\#ALL).

此属性与[getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--)选项。

**退货:**
int - 对应的 int 值。返回值是以下之一[HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode)常数。
### getImageColorSpaceExportMode() {#getImageColorSpaceExportMode--}
```
public int getImageColorSpaceExportMode()
```


指定如何为 PDF 文档中的图像选择色彩空间。

默认值为[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO).

如果[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK)指定值，[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-)选项被忽略，Flate 压缩用于文档中的所有图像。

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK)保存为 PDF/A 时不支持 value。[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO) value 将被使用。

**退货:**
int - 对应的 int 值。返回值是以下之一[PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode)常数。
### getImageCompression() {#getImageCompression--}
```
public int getImageCompression()
```


指定要用于文档中所有图像的压缩类型。

默认为[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO).

使用[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG)让您可以通过[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-)财产。

使用[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG)与其他压缩类型的性能相比，它提供了最快的转换速度，但在这种情况下，存在有损 JPEG 压缩。

使用[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO)让我们通过控制输出文档中 Jpeg 的质量[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-)属性，但对于其他格式，使用 Flate 压缩提取和保存原始像素数据。这种情况比 Jpeg 转换慢但无损。

**退货:**
int - 对应的 int 值。返回值是以下之一[PdfImageCompression](../../com.aspose.words/pdfimagecompression)常数。
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


获取一个值，该值确定如何呈现墨迹 (InkML) 对象。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**退货:**
int - 确定如何呈现墨水 (InkML) 对象的值。返回值是以下之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。
### getInterpolateImages() {#getInterpolateImages--}
```
public boolean getInterpolateImages()
```


指示图像插值是否应由合格阅读器执行的标志。指定 false 时，该标志不会写入输出文档，而是使用 reader 的默认行为。

当源图像的分辨率明显低于输出设备的分辨率时，每个源样本会覆盖许多设备像素。因此，图像可能会出现锯齿状或块状。这些视觉伪影可以通过在渲染过程中应用图像插值算法来减少。图像插值不是用相同的颜色绘制源样本覆盖的所有像素，而是尝试在相邻样本值之间产生平滑过渡。

符合要求的阅读器可以选择不实现 PDF 的此功能，或者可以使用它希望的任何特定的插值实现。

默认值为 false 。

PDF/A 合规性禁止插值标志。保存为 PDF/A 时将自动使用 false 值。

**退货:**
boolean - 对应的布尔值。
### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


获取确定 PDF 文档中 JPEG 图像质量的值。

默认值为 100。

此属性与[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-)选项。

仅当文档包含 JPEG 图像时才有效。

以 PDF 格式保存时，使用此属性可获取或设置文档中图像的质量。该值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。如果质量为 100 且源图像为 JPEG，则表示不压缩 - 将保存原始字节。

**退货:**
int - 确定 PDF 文档中 JPEG 图像质量的值。
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


获取确定是否应在保存文档之前执行内存优化的值。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的节省时间为代价来保存大型文档。

**退货:**
boolean - 确定是否应在保存文档之前执行内存优化的值。
### getMetafileRenderingOptions() {#getMetafileRenderingOptions--}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


允许指定元文件渲染选项。

**退货:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - 相应的[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions)价值。
### getNumeralFormat() {#getNumeralFormat--}
```
public int getNumeralFormat()
```


获取[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。默认使用欧洲数字。如果此属性的值已更改且页面布局已构建，则[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)自动调用以更新任何更改。

**退货:**
诠释 -\{[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。返回值是以下之一[NumeralFormat](../../com.aspose.words/numeralformat)常数。
### getOpenHyperlinksInNewWindow() {#getOpenHyperlinksInNewWindow--}
```
public boolean getOpenHyperlinksInNewWindow()
```


获取一个值，该值确定是否强制在浏览器的新窗口（或选项卡）中打开输出 Pdf 文档中的超链接。

默认值为 false 。当此值设置为 true 时，超链接将使用 JavaScript 代码保存。 JavaScript 代码是 app.launchURL("URL", true); ，其中 URL 是一个超链接。

请注意，如果此选项设置为 true，则超链接在某些 PDF 阅读器（例如 Chrome、Firefox）中无法使用。

PDF/A-1 和 PDF/A-2 合规性禁止 JavaScript 操作。保存到 PDF/A-1 和 PDF/A-2 时将自动使用 false。

**退货:**
boolean - 确定输出 Pdf 文档中的超链接是否强制在浏览器的新窗口（或选项卡）中打开的值。
### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Flag 表示是否需要优化输出。如果设置了此标志，则多余的嵌套画布和空画布被删除，具有相同格式的相邻字形也会被连接。注意：如果此属性设置为 true，可能会影响内容显示的准确性。默认为假。

**退货:**
boolean - 对应的布尔值。
### getOutlineOptions() {#getOutlineOptions--}
```
public OutlineOptions getOutlineOptions()
```


允许指定大纲选项。

可以从标题和书签创建大纲。

对于标题大纲级别由标题级别决定。

可以将最大标题级别设置为包含在大纲中或完全禁用标题大纲。

对于书签，大纲级别可以在选项中设置为所有书签的默认值或特定书签的单独值。

此外，可以使用相同的方法将轮廓导出为 XPS 格式[getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--)班级。

**退货:**
[OutlineOptions](../../com.aspose.words/outlineoptions) - 相应的[OutlineOptions](../../com.aspose.words/outlineoptions)价值。
### getPageMode() {#getPageMode--}
```
public int getPageMode()
```


指定 PDF 文档在 PDF 阅读器中打开时的显示方式。默认值为[PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode\#USE-OUTLINES).

**退货:**
int - 对应的 int 值。返回值是以下之一[PdfPageMode](../../com.aspose.words/pdfpagemode)常数。
### getPageSavingCallback() {#getPageSavingCallback--}
```
public IPageSavingCallback getPageSavingCallback()
```


允许控制将文档导出为固定页面格式时如何保存单独的页面。

**退货:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) - 相应的[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback)价值。
### getPageSet() {#getPageSet--}
```
public PageSet getPageSet()
```


获取要呈现的页面。默认为文档中的所有页面。

**退货:**
[PageSet](../../com.aspose.words/pageset) - 要呈现的页面。
### getPreblendImages() {#getPreblendImages--}
```
public boolean getPreblendImages()
```


获取一个值，该值确定是否将透明图像与黑色背景颜色预混合。

预混合图像可以改善 PDF 文档在 Adobe Reader 中的视觉外观并消除抗锯齿伪影。

为了正确显示预混合图像，PDF 查看器应用程序必须支持软掩模图像字典中的 /Matte 条目。此外，预混合图像可能会降低 PDF 渲染性能。

默认值为 false 。

**退货:**
boolean - 确定是否将透明图像与黑色背景颜色预混合的值。
### getPreserveForm字段() {#getPreserveForm字段--}
```
public boolean getPreserveForm字段()
```


指定是将 Microsoft Word 表单域保留为 PDF 中的表单域还是将它们转换为文本。默认为 false 。

Microsoft Word 表单域包括文本输入、下拉和复选框控件。

当设置为 false 时，这些字段将作为文本导出为 PDF。设置为 true 时，这些字段将导出为 PDF 表单字段。

将表单域作为表单域导出为 PDF 时，可能会出现一些格式丢失，因为 PDF 表单域不支持 Microsoft Word 表单域的所有功能。

此外，输出大小取决于内容大小，因为 Microsoft Word 中的可编辑表单是内联对象。

PDF/A 合规性禁止可编辑表单。保存为 PDF/A 时将自动使用 false 值。

保存为 PDF/UA 时不支持表单域。 false 值将被自动使用。

**退货:**
boolean - 对应的布尔值。
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
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


如果使用此保存选项对象，则指定保存文档的格式。只能是[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF).

**退货:**
int - 对应的 int 值。返回值是以下之一[SaveFormat](../../com.aspose.words/saveformat)常数。
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
### getTextCompression() {#getTextCompression--}
```
public int getTextCompression()
```


指定要用于文档中所有文本内容的压缩类型。

默认为[PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression\#FLATE).

保存未压缩的文档时显着增加输出大小。

**退货:**
int - 对应的 int 值。返回值是以下之一[PdfTextCompression](../../com.aspose.words/pdftextcompression)常数。
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
### getUseBookFoldPrintingSettings() {#getUseBookFoldPrintingSettings--}
```
public boolean getUseBookFoldPrintingSettings()
```


获取一个布尔值，指示是否应使用小册子打印布局保存文档（如果通过以下方式指定）[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).

如果指定了此选项，[FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions\#getPageSet--) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions\#setPageSet-com.aspose.words.PageSet-)保存时被忽略。此行为与 MS Word 匹配。如果页面设置中没有指定折页打印设置，此选项将无效。

**退货:**
 boolean - 一个布尔值，指示是否应使用小册子打印布局保存文档，如果它是通过指定的[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).
### getUseCoreFonts() {#getUseCoreFonts--}
```
public boolean getUseCoreFonts()
```


获取一个值，该值确定是否将 True类型 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF 类型 1 字体。

默认值为 false 。当此值设置为真 Arial 时，Times New Roman、Courier New 和 Symbol 字体在 PDF 文档中被替换为对应的核心 类型 1 字体。

任何 PDF 查看器应用程序都需要核心 PDF 字体或其字体规格和合适的替代字体。

此设置仅适用于 ANSI (Windows-1252) 编码的文本。无论此设置如何，非 ANSI 文本都将使用嵌入的 True类型 字体写入。

PDF/A 和 PDF/UA 合规性要求嵌入所有字体。保存到 PDF/A 和 PDF/UA 时将自动使用 false 值。

保存为 PDF 2.0 格式时不支持核心字体。保存到 PDF 2.0 时将自动使用 false 值。

此选项具有更高的优先级[getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions\#getFontEmbeddingMode--) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions\#setFontEmbeddingMode-int-)选项。

**退货:**
boolean - 确定是否将 True类型 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF 类型 1 字体的值。
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


获取确定是否使用高质量（即慢速）渲染算法的值。默认值为 false 。

当文档导出为图像格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**退货:**
boolean - 确定是否使用高质量的值（即
### getZoomBehavior() {#getZoomBehavior--}
```
public int getZoomBehavior()
```


获取一个值，该值确定使用 PDF 查看器打开文档时应应用哪种类型的缩放。默认值为[PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior\#NONE)，即不应用拟合。

**退货:**
 int - 确定使用 PDF 查看器打开文档时应应用哪种缩放类型的值。返回值是以下之一[PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior)常数。
### getZoomFactor() {#getZoomFactor--}
```
public int getZoomFactor()
```


获取确定文档缩放系数（以百分比为单位）的值。此值仅在以下情况下使用[getZoomBehavior()](../../com.aspose.words/pdfsaveoptions\#getZoomBehavior--) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions\#setZoomBehavior-int-)被设定为[PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior\#ZOOM-FACTOR).

**退货:**
int - 确定文档缩放系数（百分比）的值。
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




### setAdditionalTextPositioning(boolean value) {#setAdditionalTextPositioning-boolean-}
```
public void setAdditionalTextPositioning(boolean value)
```


一个标志，指定是否编写额外的文本定位运算符。

如果为 true ，则会将其他文本定位运算符写入输出 PDF。这可能有助于克服某些打印机的文本定位不准确的问题。缺点是增加了 PDF 文档的大小。

默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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

### setCacheHeaderFooterShapes(boolean value) {#setCacheHeaderFooterShapes-boolean-}
```
public void setCacheHeaderFooterShapes(boolean value)
```


设置一个值，确定是否缓存放置在文档页眉和页脚中的形状。

默认值为 false 并且不缓存形状。

当值为 true 时，图形将作为 xObject 写入 PDF 文档。

某些形状不支持缓存（带有字段、书签、HRef 的形状）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否缓存放置在文档页眉和页脚中的形状的值。 |

### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


设置一个值来确定如何呈现颜色。默认值为[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现颜色的值。该值必须是以下之一[ColorMode](../../com.aspose.words/colormode)常数。 |

### setCompliance(int value) {#setCompliance-int-}
```
public void setCompliance(int value)
```


指定输出文档的 PDF 标准合规级别。

默认为[PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance\#PDF-17).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PdfCompliance](../../com.aspose.words/pdfcompliance)常数。 |

### setCreateNoteHyperlinks(boolean value) {#setCreateNoteHyperlinks-boolean-}
```
public void setCreateNoteHyperlinks(boolean value)
```


指定是否将正文故事中的脚注/尾注引用转换为活动超链接。点击后，超链接将指向相应的脚注/尾注。默认为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setCustomPropertiesExport(int value) {#setCustomPropertiesExport-int-}
```
public void setCustomPropertiesExport(int value)
```


设置确定方式的值[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。

默认值为[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA)保存为 PDF/A 时不支持 value。[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD)将用于 PDF/A-1 和 PDF/A-2 和[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE)对于 PDF/A-4。

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD)保存为 PDF 2.0 时不支持 value。[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA)将被使用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 价值决定方式[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--)导出为 PDF 文件。该值必须是以下之一[PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport)常数。 |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


设置默认模板的路径（包括文件名）。此属性的默认值为**empty string**.如果指定，此路径用于加载模板时[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-)是真的，但是[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)是空的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 默认模板的路径（包括文件名）。 |

### setDigitalSignatureDetails(PdfDigitalSignatureDetails value) {#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-}
```
public void setDigitalSignatureDetails(PdfDigitalSignatureDetails value)
```


设置用于签署输出 PDF 文档的详细信息。

默认值为空，输出文档不会被签名。当此属性设置为有效时[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails)对象，则输出的 PDF 文档将被数字签名。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) | 签署输出 PDF 文档的详细信息。 |

### setDisplayDocTitle(boolean value) {#setDisplayDocTitle-boolean-}
```
public void setDisplayDocTitle(boolean value)
```


一个标志，指定窗口是否\\u2019s 标题栏应显示从文档信息字典的 Title 条目中获取的文档标题。

如果为 false ，则标题栏应改为显示包含该文档的 PDF 文件的名称。

PDF/UA 合规性需要此标志。保存到 PDF/UA 时将自动使用 true 值。

默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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

如果[getCompliance()](../../com.aspose.words/pdfsaveoptions\#getCompliance--) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions\#setCompliance-int-)被设定为[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A)或者[PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B) , 属性总是返回[DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode\#NONE).

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

### setDownsampleOptions(DownsampleOptions value) {#setDownsampleOptions-com.aspose.words.DownsampleOptions-}
```
public void setDownsampleOptions(DownsampleOptions value)
```


允许指定下采样选项。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [DownsampleOptions](../../com.aspose.words/downsampleoptions) | 相应的[DownsampleOptions](../../com.aspose.words/downsampleoptions)价值。 |

### setEmbedFullFonts(boolean value) {#setEmbedFullFonts-boolean-}
```
public void setEmbedFullFonts(boolean value)
```


控制字体如何嵌入到生成的 PDF 文档中。

默认值为 false ，这意味着字体在嵌入之前被子集化。如果您想保持输出文件的大小更小，子集化很有用。子集从字体中删除所有未使用的字形。

当此值设置为 true 时，将完整的字体文件嵌入到 PDF 中而不设置子集。这将导致更大的输出文件，但当您想稍后编辑生成的 PDF（例如添加更多文本）时，它可能是一个有用的选项。

某些字体很大（几兆字节）并且在没有子集的情况下嵌入它们会导致输出文档很大。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setEncryptionDetails(PdfEncryptionDetails value) {#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails-}
```
public void setEncryptionDetails(PdfEncryptionDetails value)
```


设置加密输出 PDF 文档的详细信息。

默认值为空，输出文档不会被加密。当此属性设置为有效时[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails)对象，则输出的 PDF 文档将被加密。

保存到基于 PDF 1.7 的合规性（包括 PDF/UA-1）时使用 AES-128 加密算法。保存到基于 PDF 2.0 的合规性时使用 AES-256 加密算法。

PDF/A 合规性禁止加密。保存为 PDF/A 时将忽略此选项。

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY)如果输出文档是加密的，则 PDF/UA 合规性需要许可。保存到 PDF/UA 时将自动使用此权限。

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY)PDF 2.0 格式不推荐使用权限。保存到 PDF 2.0 时将忽略此权限。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) | 加密输出 PDF 文档的详细信息。 |

### setExportDocumentStructure(boolean value) {#setExportDocumentStructure-boolean-}
```
public void setExportDocumentStructure(boolean value)
```


设置确定是否导出文档结构的值。

保存到 PDF/A-1a、PDF/A-2a 和 PDF/UA-1 时忽略此值，因为此合规性需要文档结构。

请注意，导出文档结构会显着增加内存消耗，尤其是对于大型文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否导出文档结构的值。 |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。默认值为**true**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportLanguageToSpanTag(boolean value) {#setExportLanguageToSpanTag-boolean-}
```
public void setExportLanguageToSpanTag(boolean value)
```


设置一个值，确定是否在文档结构中创建“Span”标签以导出文本语言。

默认值为 false，并且“Lang”属性附加到页面内容流中的标记内容序列。

当值为 true 时，将为具有非默认语言的文本创建“Span”标签，并将“Lang”属性附加到此标签。

该值被忽略时[getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions\#getExportDocumentStructure--) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions\#setExportDocumentStructure-boolean-)是假的。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否在文档结构中创建“Span”标签以导出文本语言的值。 |

### setFontEmbeddingMode(int value) {#setFontEmbeddingMode-int-}
```
public void setFontEmbeddingMode(int value)
```


指定字体嵌入模式。

默认值为[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL).

此设置仅适用于 ANSI (Windows-1252) 编码的文本。如果文档包含非 ANSI 文本，则无论此设置如何，都将嵌入相应的字体。

 PDF/A 和 PDF/UA 合规性要求嵌入所有字体。[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL)保存为 PDF/A 和 PDF/UA 时将自动使用该值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode)常数。 |

### setHeaderFooterBookmarksExportMode(int value) {#setHeaderFooterBookmarksExportMode-int-}
```
public void setHeaderFooterBookmarksExportMode(int value)
```


确定如何导出页眉/页脚中的书签。

默认值为[HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode\#ALL).

此属性与[getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--)选项。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode)常数。 |

### setImageColorSpaceExportMode(int value) {#setImageColorSpaceExportMode-int-}
```
public void setImageColorSpaceExportMode(int value)
```


指定如何为 PDF 文档中的图像选择色彩空间。

默认值为[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO).

如果[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK)指定值，[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-)选项被忽略，Flate 压缩用于文档中的所有图像。

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK)保存为 PDF/A 时不支持 value。[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO) value 将被使用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode)常数。 |

### setImageCompression(int value) {#setImageCompression-int-}
```
public void setImageCompression(int value)
```


指定要用于文档中所有图像的压缩类型。

默认为[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO).

使用[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG)让您可以通过[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-)财产。

使用[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG)与其他压缩类型的性能相比，它提供了最快的转换速度，但在这种情况下，存在有损 JPEG 压缩。

使用[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO)让我们通过控制输出文档中 Jpeg 的质量[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-)属性，但对于其他格式，使用 Flate 压缩提取和保存原始像素数据。这种情况比 Jpeg 转换慢但无损。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PdfImageCompression](../../com.aspose.words/pdfimagecompression)常数。 |

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

### setInterpolateImages(boolean value) {#setInterpolateImages-boolean-}
```
public void setInterpolateImages(boolean value)
```


指示图像插值是否应由合格阅读器执行的标志。指定 false 时，该标志不会写入输出文档，而是使用 reader 的默认行为。

当源图像的分辨率明显低于输出设备的分辨率时，每个源样本会覆盖许多设备像素。因此，图像可能会出现锯齿状或块状。这些视觉伪影可以通过在渲染过程中应用图像插值算法来减少。图像插值不是用相同的颜色绘制源样本覆盖的所有像素，而是尝试在相邻样本值之间产生平滑过渡。

符合要求的阅读器可以选择不实现 PDF 的此功能，或者可以使用它希望的任何特定的插值实现。

默认值为 false 。

PDF/A 合规性禁止插值标志。保存为 PDF/A 时将自动使用 false 值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


设置确定 PDF 文档中 JPEG 图像质量的值。

默认值为 100。

此属性与[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-)选项。

仅当文档包含 JPEG 图像时才有效。

以 PDF 格式保存时，使用此属性可获取或设置文档中图像的质量。该值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。如果质量为 100 且源图像为 JPEG，则表示不压缩 - 将保存原始字节。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定 PDF 文档中 JPEG 图像质量的值。 |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


设置值确定是否应在保存文档之前执行内存优化。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的节省时间为代价来保存大型文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否应在保存文档之前执行内存优化的值。 |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


允许指定元文件渲染选项。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) | 相应的[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions)价值。 |

### setNumeralFormat(int value) {#setNumeralFormat-int-}
```
public void setNumeralFormat(int value)
```


套[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。默认使用欧洲数字。如果此属性的值已更改且页面布局已构建，则[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)自动调用以更新任何更改。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。该值必须是以下之一[NumeralFormat](../../com.aspose.words/numeralformat)常数。 |

### setOpenHyperlinksInNewWindow(boolean value) {#setOpenHyperlinksInNewWindow-boolean-}
```
public void setOpenHyperlinksInNewWindow(boolean value)
```


设置一个值，确定是否强制在浏览器的新窗口（或选项卡）中打开输出 Pdf 文档中的超链接。

默认值为 false 。当此值设置为 true 时，超链接将使用 JavaScript 代码保存。 JavaScript 代码是 app.launchURL("URL", true); ，其中 URL 是一个超链接。

请注意，如果此选项设置为 true，则超链接在某些 PDF 阅读器（例如 Chrome、Firefox）中无法使用。

PDF/A-1 和 PDF/A-2 合规性禁止 JavaScript 操作。保存到 PDF/A-1 和 PDF/A-2 时将自动使用 false。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定输出 Pdf 文档中的超链接是否强制在浏览器的新窗口（或选项卡）中打开的值。 |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Flag 表示是否需要优化输出。如果设置了此标志，则多余的嵌套画布和空画布被删除，具有相同格式的相邻字形也会被连接。注意：如果此属性设置为 true，可能会影响内容显示的准确性。默认为假。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPageMode(int value) {#setPageMode-int-}
```
public void setPageMode(int value)
```


指定 PDF 文档在 PDF 阅读器中打开时的显示方式。默认值为[PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode\#USE-OUTLINES).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PdfPageMode](../../com.aspose.words/pdfpagemode)常数。 |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback-}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


允许控制将文档导出为固定页面格式时如何保存单独的页面。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) | 相应的[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback)价值。 |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet-}
```
public void setPageSet(PageSet value)
```


设置要呈现的页面。默认为文档中的所有页面。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | 要呈现的页面。 |

### setPreblendImages(boolean value) {#setPreblendImages-boolean-}
```
public void setPreblendImages(boolean value)
```


设置一个值，确定是否将透明图像与黑色背景颜色预混合。

预混合图像可以改善 PDF 文档在 Adobe Reader 中的视觉外观并消除抗锯齿伪影。

为了正确显示预混合图像，PDF 查看器应用程序必须支持软掩模图像字典中的 /Matte 条目。此外，预混合图像可能会降低 PDF 渲染性能。

默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否将透明图像与黑色背景颜色预混合的值。 |

### setPreserveForm字段(boolean value) {#setPreserveForm字段-boolean-}
```
public void setPreserveForm字段(boolean value)
```


指定是将 Microsoft Word 表单域保留为 PDF 中的表单域还是将它们转换为文本。默认为 false 。

Microsoft Word 表单域包括文本输入、下拉和复选框控件。

当设置为 false 时，这些字段将作为文本导出为 PDF。设置为 true 时，这些字段将导出为 PDF 表单字段。

将表单域作为表单域导出为 PDF 时，可能会出现一些格式丢失，因为 PDF 表单域不支持 Microsoft Word 表单域的所有功能。

此外，输出大小取决于内容大小，因为 Microsoft Word 中的可编辑表单是内联对象。

PDF/A 合规性禁止可编辑表单。保存为 PDF/A 时将自动使用 false 值。

保存为 PDF/UA 时不支持表单域。 false 值将被自动使用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


如果使用此保存选项对象，则指定保存文档的格式。只能是[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[SaveFormat](../../com.aspose.words/saveformat)常数。 |

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

### setTextCompression(int value) {#setTextCompression-int-}
```
public void setTextCompression(int value)
```


指定要用于文档中所有文本内容的压缩类型。

默认为[PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression\#FLATE).

保存未压缩的文档时显着增加输出大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[PdfTextCompression](../../com.aspose.words/pdftextcompression)常数。 |

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

### setUseBookFoldPrintingSettings(boolean value) {#setUseBookFoldPrintingSettings-boolean-}
```
public void setUseBookFoldPrintingSettings(boolean value)
```


设置一个布尔值，指示是否应使用小册子打印布局保存文档，如果它是通过指定的[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).

如果指定了此选项，[FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions\#getPageSet--) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions\#setPageSet-com.aspose.words.PageSet-)保存时被忽略。此行为与 MS Word 匹配。如果页面设置中没有指定折页打印设置，此选项将无效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示是否应使用小册子打印布局保存文档（如果通过以下方式指定）[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |

### setUseCoreFonts(boolean value) {#setUseCoreFonts-boolean-}
```
public void setUseCoreFonts(boolean value)
```


设置一个值，确定是否将 True类型 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF 类型 1 字体。

默认值为 false 。当此值设置为真 Arial 时，Times New Roman、Courier New 和 Symbol 字体在 PDF 文档中被替换为对应的核心 类型 1 字体。

任何 PDF 查看器应用程序都需要核心 PDF 字体或其字体规格和合适的替代字体。

此设置仅适用于 ANSI (Windows-1252) 编码的文本。无论此设置如何，非 ANSI 文本都将使用嵌入的 True类型 字体写入。

PDF/A 和 PDF/UA 合规性要求嵌入所有字体。保存到 PDF/A 和 PDF/UA 时将自动使用 false 值。

保存为 PDF 2.0 格式时不支持核心字体。保存到 PDF 2.0 时将自动使用 false 值。

此选项具有更高的优先级[getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions\#getFontEmbeddingMode--) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions\#setFontEmbeddingMode-int-)选项。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否将 True类型 字体 Arial、Times New Roman、Courier New 和 Symbol 替换为核心 PDF 类型 1 字体的值。 |

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

### setZoomBehavior(int value) {#setZoomBehavior-int-}
```
public void setZoomBehavior(int value)
```


设置一个值，用于确定使用 PDF 查看器打开文档时应应用的缩放类型。默认值为[PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior\#NONE)，即不应用拟合。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一个值，用于确定使用 PDF 查看器打开文档时应应用哪种类型的缩放。该值必须是以下之一[PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior)常数。 |

### setZoomFactor(int value) {#setZoomFactor-int-}
```
public void setZoomFactor(int value)
```


设置确定文档缩放系数（以百分比为单位）的值。此值仅在以下情况下使用[getZoomBehavior()](../../com.aspose.words/pdfsaveoptions\#getZoomBehavior--) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions\#setZoomBehavior-int-)被设定为[PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior\#ZOOM-FACTOR).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定文档缩放系数（百分比）的值。 |

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
