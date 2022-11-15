---
title: HtmlFixedSaveOptions
second_title: Aspose.Words for Java API 参考
description: 可用于在将文档保存为格式时指定附加选项。
type: docs
weight: 326
url: /zh/java/com.aspose.words/htmlfixedsaveoptions/
---

**遗产：**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class HtmlFixedSaveOptions extends FixedPageSaveOptions
```

可用于在将文档保存到[SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED)格式。

要了解更多信息，请访问**Specify Save Options**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | 创建适合给定文件名中指定的文件扩展名的类的保存选项对象。 |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | 获取一个布尔值，指示在保存文档时在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [getClass()](#getClass--) |  |
| [getColorMode()](#getColorMode--) | 获取确定颜色呈现方式的值。 |
| [getCssClassNamesPrefix()](#getCssClassNamesPrefix--) | 指定添加到 style.css 文件中所有类名称的前缀。 |
| [getDefaultTemplate()](#getDefaultTemplate--) | 获取默认模板的路径（包括文件名）。 |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | 获取确定如何呈现 3D 效果的值。 |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | 获取确定如何呈现 DrawingML 效果的值。 |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | 获取确定如何呈现 DrawingML 形状的值。 |
| [getEncoding()](#getEncoding--) |  |
| [getExportEmbeddedCss()](#getExportEmbeddedCss--) | 指定 CSS（级联样式表）是否应嵌入到 Html 文档中。 |
| [getExportEmbeddedFonts()](#getExportEmbeddedFonts--) | 指定字体是否应以 Base64 格式嵌入到 Html 文档中。 |
| [getExportEmbeddedImages()](#getExportEmbeddedImages--) | 指定图像是否应以 Base64 格式嵌入到 Html 文档中。 |
| [getExportEmbeddedSvg()](#getExportEmbeddedSvg--) | 指定是否应将 SVG 资源嵌入到 Html 文档中。 |
| [getExportFormFields()](#getExportFormFields--) | 获取是否将表单字段导出为交互式项目（作为“输入”标签）而不是转换为文本或图形的指示。 |
| [getExportGeneratorName()](#getExportGeneratorName--) | 当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。 |
| [getFontFormat()](#getFontFormat--) | 得到[ExportFontFormat](../../com.aspose.words/exportfontformat)用于字体导出。 |
| [getImlRenderingMode()](#getImlRenderingMode--) | 获取确定如何呈现墨迹 (InkML) 对象的值。 |
| [getJpegQuality()](#getJpegQuality--) | 获取确定 Html 文档中 JPEG 图像质量的值。 |
| [getMemoryOptimization()](#getMemoryOptimization--) | 获取确定在保存文档之前是否应执行内存优化的值。 |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | 允许指定图元文件渲染选项。 |
| [getNumeralFormat()](#getNumeralFormat--) | 得到[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。 |
| [getOptimizeOutput()](#getOptimizeOutput--) | Flag 表示是否需要优化输出。 |
| [getPageHorizontalAlignment()](#getPageHorizontalAlignment--) | 指定 HTML 文档中页面的水平对齐方式。 |
| [getPageMargins()](#getPageMargins--) | 指定 HTML 文档中页面周围的边距。 |
| [getPageSavingCallback()](#getPageSavingCallback--) | 允许控制在将文档导出为固定页面格式时如何保存单独的页面。 |
| [getPageSet()](#getPageSet--) | 获取要呈现的页面。 |
| [getPrettyFormat()](#getPrettyFormat--) | 当 true 时，漂亮的格式输出适用。 |
| [getProgressCallback()](#getProgressCallback--) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [getResourceSavingCallback()](#getResourceSavingCallback--) | 允许控制在将文档导出为固定页面 Html 格式时如何保存资源（图像、字体和 css）。 |
| [getResourcesFolder()](#getResourcesFolder--) | 指定将文档导出为 Html 格式时保存资源（图像、字体、css）的物理文件夹。 |
| [getResourcesFolderAlias()](#getResourcesFolderAlias--) | 指定用于构造写入 Html 文档的图像 URI 的文件夹的名称。 |
| [getSaveFontFaceCssSeparately()](#getSaveFontFaceCssSeparately--) |  Flag 指示当使用外部样式表保存文档时（即，当[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-)是假的）。 |
| [getSaveFormat()](#getSaveFormat--) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [getShowPageBorder()](#getShowPageBorder--) | 指定是否应显示页面周围的边框。 |
| [getTempFolder()](#getTempFolder--) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateFields()](#getUpdateFields--) | 获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateSdtContent()](#getUpdateSdtContent--) | 获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。 |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | 获取一个值，该值确定是否对渲染使用抗锯齿。 |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | 获取确定是否使用高质量的值（即 |
| [getUseTargetMachineFonts()](#getUseTargetMachineFonts--) | 标志指示是否必须使用来自目标机器的字体来显示文档。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | 设置一个布尔值，指示在保存文档时在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [setColorMode(int value)](#setColorMode-int-) | 设置确定颜色呈现方式的值。 |
| [setCssClassNamesPrefix(String value)](#setCssClassNamesPrefix-java.lang.String-) | 指定添加到 style.css 文件中所有类名称的前缀。 |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | 将路径设置为默认模板（包括文件名）。 |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | 设置确定 3D 效果呈现方式的值。 |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 效果。 |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 形状。 |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [setExportEmbeddedCss(boolean value)](#setExportEmbeddedCss-boolean-) | 指定 CSS（级联样式表）是否应嵌入到 Html 文档中。 |
| [setExportEmbeddedFonts(boolean value)](#setExportEmbeddedFonts-boolean-) | 指定字体是否应以 Base64 格式嵌入到 Html 文档中。 |
| [setExportEmbeddedImages(boolean value)](#setExportEmbeddedImages-boolean-) | 指定图像是否应以 Base64 格式嵌入到 Html 文档中。 |
| [setExportEmbeddedSvg(boolean value)](#setExportEmbeddedSvg-boolean-) | 指定是否应将 SVG 资源嵌入到 Html 文档中。 |
| [setExportFormFields(boolean value)](#setExportFormFields-boolean-) | 设置是否将表单字段导出为交互式项目（作为“输入”标签）而不是转换为文本或图形的指示。 |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | 当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。 |
| [setFontFormat(int value)](#setFontFormat-int-) | 套[ExportFontFormat](../../com.aspose.words/exportfontformat)用于字体导出。 |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | 设置一个值，确定如何呈现墨迹 (InkML) 对象。 |
| [setJpegQuality(int value)](#setJpegQuality-int-) | 设置一个值，确定 Html 文档中 JPEG 图像的质量。 |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | 设置确定在保存文档之前是否应执行内存优化的值。 |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | 允许指定图元文件渲染选项。 |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) | 套[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。 |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Flag 表示是否需要优化输出。 |
| [setPageHorizontalAlignment(int value)](#setPageHorizontalAlignment-int-) | 指定 HTML 文档中页面的水平对齐方式。 |
| [setPageMargins(double value)](#setPageMargins-double-) | 指定 HTML 文档中页面周围的边距。 |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | 允许控制在将文档导出为固定页面格式时如何保存单独的页面。 |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | 设置要呈现的页面。 |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | 当 true 时，漂亮的格式输出适用。 |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) | 允许控制在将文档导出为固定页面 Html 格式时如何保存资源（图像、字体和 css）。 |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String-) | 指定将文档导出为 Html 格式时保存资源（图像、字体、css）的物理文件夹。 |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String-) | 指定用于构造写入 Html 文档的图像 URI 的文件夹的名称。 |
| [setSaveFontFaceCssSeparately(boolean value)](#setSaveFontFaceCssSeparately-boolean-) |  Flag 指示当使用外部样式表保存文档时（即，当[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-)是假的）。 |
| [setSaveFormat(int value)](#setSaveFormat-int-) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [setShowPageBorder(boolean value)](#setShowPageBorder-boolean-) | 指定是否应显示页面周围的边框。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | 设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) | 设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。 |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | 设置一个值，确定是否使用抗锯齿进行渲染。 |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | 设置一个值确定是否使用高质量（即 |
| [setUseTargetMachineFonts(boolean value)](#setUseTargetMachineFonts-boolean-) | 标志指示是否必须使用来自目标机器的字体来显示文档。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### createSaveOptions(int saveFormat) {#createSaveOptions-int-}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货：**
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String-}
```
public static SaveOptions createSaveOptions(String fileName)
```


创建适合给定文件名中指定的文件扩展名的类的保存选项对象。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 此文件名的扩展名决定了要创建的保存选项对象的类。 |

**退货：**
[SaveOptions](../../com.aspose.words/saveoptions) - 派生自的类的对象[SaveOptions](../../com.aspose.words/saveoptions).
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


确定指定对象的值是否与当前对象相等。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货：**
布尔值
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


获取一个布尔值，指示在保存文档时在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值为**false**.

请注意，Word 不嵌入 PostScript 字体，但可以打开带有此类嵌入字体的文档。

此选项仅在[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-)的[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性设置为 true 。

**退货：**
boolean - 一个布尔值，指示在保存文档时是否允许在文档中嵌入 TrueType 字体时嵌入具有 PostScript 轮廓的字体。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getColorMode() {#getColorMode--}
```
public int getColorMode()
```


获取确定颜色呈现方式的值。默认值为[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**退货：**
int - 确定颜色呈现方式的值。返回值是其中之一[ColorMode](../../com.aspose.words/colormode)常数。
### getCssClassNamesPrefix() {#getCssClassNamesPrefix--}
```
public String getCssClassNamesPrefix()
```


指定添加到 style.css 文件中所有类名称的前缀。默认值为 "aw" 。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


获取默认模板的路径（包括文件名）。此属性的默认值为**empty string**.如果指定，此路径用于加载模板时[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-)是真的，但是[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)是空的。

**退货：**
java.lang.String - 默认模板的路径（包括文件名）。
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode--}
```
public int getDml3DEffectsRenderingMode()
```


获取确定如何呈现 3D 效果的值。默认值为[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**退货：**
int - 决定如何呈现 3D 效果的值。返回值是其中之一[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode)常数。
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


获取确定如何呈现 DrawingML 效果的值。默认值为[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

当文档导出为固定页面格式时使用此属性。

**退货：**
 int - 确定如何呈现 DrawingML 效果的值。返回值是其中之一[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode)常数。
### getDmlRenderingMode() {#getDmlRenderingMode--}
```
public int getDmlRenderingMode()
```


获取确定如何呈现 DrawingML 形状的值。默认值为[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

当文档导出为固定页面格式时使用此属性。

**退货：**
int - 确定 DrawingML 形状如何呈现的值。返回值是其中之一[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode)常数。
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**退货：**
java.nio.charset.字符集
### getExportEmbeddedCss() {#getExportEmbeddedCss--}
```
public boolean getExportEmbeddedCss()
```


指定 CSS（级联样式表）是否应嵌入到 Html 文档中。

**退货：**
boolean - 相应的布尔值。
### getExportEmbeddedFonts() {#getExportEmbeddedFonts--}
```
public boolean getExportEmbeddedFonts()
```


指定字体是否应以 Base64 格式嵌入到 Html 文档中。注意设置此标志可以显着增加输出 Html 文件的大小。

**退货：**
boolean - 相应的布尔值。
### getExportEmbeddedImages() {#getExportEmbeddedImages--}
```
public boolean getExportEmbeddedImages()
```


指定图像是否应以 Base64 格式嵌入到 Html 文档中。注意设置此标志可以显着增加输出 Html 文件的大小。

**退货：**
boolean - 相应的布尔值。
### getExportEmbeddedSvg() {#getExportEmbeddedSvg--}
```
public boolean getExportEmbeddedSvg()
```


指定是否应将 SVG 资源嵌入到 Html 文档中。默认值为 true 。

**退货：**
boolean - 相应的布尔值。
### getExportFormFields() {#getExportFormFields--}
```
public boolean getExportFormFields()
```


获取是否将表单字段导出为交互式项目（作为“输入”标签）而不是转换为文本或图形的指示。

**退货：**
boolean - 指示表单字段是否导出为交互式项目（作为“输入”标签）而不是转换为文本或图形。
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。默认值为**true**.

**退货：**
boolean - 相应的布尔值。
### getFontFormat() {#getFontFormat--}
```
public int getFontFormat()
```


得到[ExportFontFormat](../../com.aspose.words/exportfontformat)用于字体导出。默认值为[ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat\#WOFF).

**退货：**
整数 -\{[ExportFontFormat](../../com.aspose.words/exportfontformat)用于字体导出。返回值是其中之一[ExportFontFormat](../../com.aspose.words/exportfontformat)常数。
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


获取确定如何呈现墨迹 (InkML) 对象的值。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**退货：**
int - 确定如何呈现墨迹 (InkML) 对象的值。返回值是其中之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。
### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


获取确定 Html 文档中 JPEG 图像质量的值。

仅当文档包含 JPEG 图像时才有效。

使用此属性获取或设置以固定页面格式保存时文档内图像的质量。该值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。

默认值为 95。

**退货：**
int - 确定 Html 文档中 JPEG 图像质量的值。
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


获取确定在保存文档之前是否应执行内存优化的值。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的保存时间为代价保存大型文档。

**退货：**
布尔值 - 确定在保存文档之前是否应执行内存优化的值。
### getMetafileRenderingOptions() {#getMetafileRenderingOptions--}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


允许指定图元文件渲染选项。

**退货：**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - 相应的[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions)价值。
### getNumeralFormat() {#getNumeralFormat--}
```
public int getNumeralFormat()
```


得到[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。默认使用欧洲数字。如果此属性的值已更改且页面布局已构建，则[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)被自动调用以更新任何更改。

**退货：**
整数 -\{[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。返回值是其中之一[NumeralFormat](../../com.aspose.words/numeralformat)常数。
### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Flag 表示是否需要优化输出。如果设置了此标志，则多余的嵌套画布和空画布被删除，具有相同格式的相邻字形也会被连接。注意：如果此属性设置为 true，可能会影响内容显示的准确性。默认为真。

**退货：**
boolean - 相应的布尔值。
### getPageHorizontalAlignment() {#getPageHorizontalAlignment--}
```
public int getPageHorizontalAlignment()
```


指定 HTML 文档中页面的水平对齐方式。默认值为 HtmlFixedHorizontalPageAlignment.Center 。

**退货：**
int - 相应的 int 值。返回值是其中之一[HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment)常数。
### getPageMargins() {#getPageMargins--}
```
public double getPageMargins()
```


指定 HTML 文档中页面周围的边距。边距值以磅为单位，应等于或大于 0。默认值为 10 磅。

取决于价值[getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions\#getPageHorizontalAlignment--) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions\#setPageHorizontalAlignment-int-)财产：

 *  如果值为[HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#LEFT).
 *  如果值为[HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#RIGHT).
 *  如果值为[HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment\#CENTER).

**退货：**
double - 相应的双精度值。
### getPageSavingCallback() {#getPageSavingCallback--}
```
public IPageSavingCallback getPageSavingCallback()
```


允许控制在将文档导出为固定页面格式时如何保存单独的页面。

**退货：**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) - 相应的[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback)价值。
### getPageSet() {#getPageSet--}
```
public PageSet getPageSet()
```


获取要呈现的页面。默认为文档中的所有页面。

**退货：**
[PageSet](../../com.aspose.words/pageset) - 要呈现的页面。
### getPrettyFormat() {#getPrettyFormat--}
```
public boolean getPrettyFormat()
```


当 true 时，漂亮的格式输出适用。默认值为**false**.

调成**true**使 HTML、MHTML、EPUB、WordML、RTF、DOCX 和 ODT 输出人类可读。用于测试或调试。

**退货：**
boolean - 相应的布尔值。
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentSavingCallback getProgressCallback()
```


在保存文档期间调用并接受有关保存进度的数据。

保存到时报告进度[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW)， 或者[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**退货：**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - 相应的[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback)价值。
### getResourceSavingCallback() {#getResourceSavingCallback--}
```
public IResourceSavingCallback getResourceSavingCallback()
```


允许控制在将文档导出为固定页面 Html 格式时如何保存资源（图像、字体和 css）。

**退货：**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) - 相应的[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback)价值。
### getResourcesFolder() {#getResourcesFolder--}
```
public String getResourcesFolder()
```


指定将文档导出为 Html 格式时保存资源（图像、字体、css）的物理文件夹。默认为空。

只有当[getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedImages-boolean-)财产是假的。

当你保存一个[Document](../../com.aspose.words/document)在 Html 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)允许您指定图像的保存位置和[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-)允许指定图像 URI 的构建方式。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认情况下会将图像保存在保存文档文件的同一文件夹中。利用[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)覆盖此行为。

如果将文档保存到流中，Aspose.Words 没有保存图像的文件夹，但仍需要将图像保存在某个位置。在这种情况下，您需要使用[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)财产

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getResourcesFolderAlias() {#getResourcesFolderAlias--}
```
public String getResourcesFolderAlias()
```


指定用于构造写入 Html 文档的图像 URI 的文件夹的名称。默认为空。

当你保存一个[Document](../../com.aspose.words/document)在 Html 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)允许您指定图像的保存位置和[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-)允许指定图像 URI 的构建方式。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getSaveFontFaceCssSeparately() {#getSaveFontFaceCssSeparately--}
```
public boolean getSaveFontFaceCssSeparately()
```


 Flag 指示当使用外部样式表保存文档时（即，当[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-)是假的）。默认值为 false ，所有 CSS 规则都写入单个文件“styles.css”。将此属性设置为 true 会恢复旧行为（单独的文件）以与旧代码兼容。

**退货：**
boolean - 相应的布尔值。
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


如果使用此保存选项对象，则指定保存文档的格式。只能是[SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED).

**退货：**
int - 相应的 int 值。返回值是其中之一[SaveFormat](../../com.aspose.words/saveformat)常数。
### getShowPageBorder() {#getShowPageBorder--}
```
public boolean getShowPageBorder()
```


指定是否应显示页面周围的边框。默认为 true 。

**退货：**
boolean - 相应的布尔值。
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。默认情况下，此属性为 null 且不使用临时文件。

当Aspose.Words 保存文档时，它需要创建临时的内部结构。默认情况下，这些内部结构是在内存中创建的，并且在保存文档时内存使用会在短时间内出现峰值。保存完成后，内存将被垃圾收集器释放和回收。

如果您正在保存非常大的文档（数千页）和/或同时处理许多文档，那么保存期间的内存峰值可能会非常大，足以导致系统抛出 java.lang.IndexOutOfBoundsException。使用指定临时文件夹[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)将导致 Aspose.Words 将内部结构保存在临时文件而不是内存中。它会减少保存期间的内存使用量，但会降低保存性能。

该文件夹必须存在且可写，否则会抛出异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty--}
```
public boolean getUpdateCreatedTimeProperty()
```


获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。默认值为假；

**退货：**
 boolean - 确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。
### getUpdateFields() {#getUpdateFields--}
```
public boolean getUpdateFields()
```


获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为**true**.允许指定是否模仿 MS Word 行为。

**退货：**
boolean - 确定在将文档保存为固定页面格式之前是否应更新某些类型的字段的值。
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty--}
```
public boolean getUpdateLastPrintedProperty()
```


获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。

**退货：**
 boolean - 确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty--}
```
public boolean getUpdateLastSavedTimeProperty()
```


获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。

**退货：**
 boolean - 确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。
### getUpdateSdtContent() {#getUpdateSdtContent--}
```
public boolean getUpdateSdtContent()
```


获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。默认值为 false 。

**退货：**
 boolean - 确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。
### getUseAntiAliasing() {#getUseAntiAliasing--}
```
public boolean getUseAntiAliasing()
```


获取一个值，该值确定是否对渲染使用抗锯齿。

默认值为 false 。当此值设置为 true 时，将使用抗锯齿进行渲染。

当文档导出为以下格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) .当文档导出到[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)和[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式 此选项用于光栅图像。

**退货：**
布尔值 - 确定是否使用抗锯齿进行渲染的值。
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


获取一个值，该值确定是否使用高质量（即慢速）渲染算法。默认值为 false 。

当文档导出为图像格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**退货：**
布尔值 - 确定是否使用高质量的值（即
### getUseTargetMachineFonts() {#getUseTargetMachineFonts--}
```
public boolean getUseTargetMachineFonts()
```


标志指示是否必须使用来自目标机器的字体来显示文档。如果此标志设置为真，[getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions\#getFontFormat--) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions\#setFontFormat-int-)和[getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedFonts--) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedFonts-boolean-)属性也没有效果[getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions\#getResourceSavingCallback--) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-)不会因字体而被解雇。默认为假。

**退货：**
boolean - 相应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
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


设置一个布尔值，指示在保存文档时在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值为**false**.

请注意，Word 不嵌入 PostScript 字体，但可以打开带有此类嵌入字体的文档。

此选项仅在[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-)的[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性设置为 true 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 保存一个布尔值，指示在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |

### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


设置确定颜色呈现方式的值。默认值为[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定颜色呈现方式的值。该值必须是其中之一[ColorMode](../../com.aspose.words/colormode)常数。 |

### setCssClassNamesPrefix(String value) {#setCssClassNamesPrefix-java.lang.String-}
```
public void setCssClassNamesPrefix(String value)
```


指定添加到 style.css 文件中所有类名称的前缀。默认值为 "aw" 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


将路径设置为默认模板（包括文件名）。此属性的默认值为**empty string**.如果指定，此路径用于加载模板时[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-)是真的，但是[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)是空的。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 默认模板的路径（包括文件名）。 |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int-}
```
public void setDml3DEffectsRenderingMode(int value)
```


设置确定 3D 效果呈现方式的值。默认值为[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现 3D 效果的值。该值必须是其中之一[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode)常数。 |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


设置一个值，确定如何呈现 DrawingML 效果。默认值为[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

当文档导出为固定页面格式时使用此属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现 DrawingML 效果的值。该值必须是其中之一[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode)常数。 |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int-}
```
public void setDmlRenderingMode(int value)
```


设置一个值，确定如何呈现 DrawingML 形状。默认值为[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

当文档导出为固定页面格式时使用此属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现 DrawingML 形状的值。该值必须是其中之一[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode)常数。 |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setExportEmbeddedCss(boolean value) {#setExportEmbeddedCss-boolean-}
```
public void setExportEmbeddedCss(boolean value)
```


指定 CSS（级联样式表）是否应嵌入到 Html 文档中。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportEmbeddedFonts(boolean value) {#setExportEmbeddedFonts-boolean-}
```
public void setExportEmbeddedFonts(boolean value)
```


指定字体是否应以 Base64 格式嵌入到 Html 文档中。注意设置此标志可以显着增加输出 Html 文件的大小。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportEmbeddedImages(boolean value) {#setExportEmbeddedImages-boolean-}
```
public void setExportEmbeddedImages(boolean value)
```


指定图像是否应以 Base64 格式嵌入到 Html 文档中。注意设置此标志可以显着增加输出 Html 文件的大小。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportEmbeddedSvg(boolean value) {#setExportEmbeddedSvg-boolean-}
```
public void setExportEmbeddedSvg(boolean value)
```


指定是否应将 SVG 资源嵌入到 Html 文档中。默认值为 true 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExportFormFields(boolean value) {#setExportFormFields-boolean-}
```
public void setExportFormFields(boolean value)
```


设置是否将表单字段导出为交互式项目（作为“输入”标签）而不是转换为文本或图形的指示。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示表单字段是否导出为交互式项目（作为“输入”标签）而不是转换为文本或图形。 |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFontFormat(int value) {#setFontFormat-int-}
```
public void setFontFormat(int value)
```


套[ExportFontFormat](../../com.aspose.words/exportfontformat)用于字体导出。默认值为[ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat\#WOFF).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | \{[ExportFontFormat](../../com.aspose.words/exportfontformat)用于字体导出。该值必须是其中之一[ExportFontFormat](../../com.aspose.words/exportfontformat)常数。 |

### setImlRenderingMode(int value) {#setImlRenderingMode-int-}
```
public void setImlRenderingMode(int value)
```


设置一个值，确定如何呈现墨迹 (InkML) 对象。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现墨迹 (InkML) 对象的值。该值必须是其中之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。 |

### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


设置一个值，确定 Html 文档中 JPEG 图像的质量。

仅当文档包含 JPEG 图像时才有效。

使用此属性获取或设置以固定页面格式保存时文档内图像的质量。该值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。

默认值为 95。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定 Html 文档中 JPEG 图像质量的值。 |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的保存时间为代价保存大型文档。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定在保存文档之前是否应执行内存优化的值。 |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


允许指定图元文件渲染选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) | 相应的[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions)价值。 |

### setNumeralFormat(int value) {#setNumeralFormat-int-}
```
public void setNumeralFormat(int value)
```


套[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。默认使用欧洲数字。如果此属性的值已更改且页面布局已构建，则[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)被自动调用以更新任何更改。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。该值必须是其中之一[NumeralFormat](../../com.aspose.words/numeralformat)常数。 |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Flag 表示是否需要优化输出。如果设置了此标志，则多余的嵌套画布和空画布被删除，具有相同格式的相邻字形也会被连接。注意：如果此属性设置为 true，可能会影响内容显示的准确性。默认为真。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setPageHorizontalAlignment(int value) {#setPageHorizontalAlignment-int-}
```
public void setPageHorizontalAlignment(int value)
```


指定 HTML 文档中页面的水平对齐方式。默认值为 HtmlFixedHorizontalPageAlignment.Center 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment)常数。 |

### setPageMargins(double value) {#setPageMargins-double-}
```
public void setPageMargins(double value)
```


指定 HTML 文档中页面周围的边距。边距值以磅为单位，应等于或大于 0。默认值为 10 磅。

取决于价值[getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions\#getPageHorizontalAlignment--) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions\#setPageHorizontalAlignment-int-)财产：

 *  如果值为[HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#LEFT).
 *  如果值为[HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#RIGHT).
 *  如果值为[HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment\#CENTER).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对应的双精度值。 |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback-}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


允许控制在将文档导出为固定页面格式时如何保存单独的页面。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) | 相应的[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback)价值。 |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet-}
```
public void setPageSet(PageSet value)
```


设置要呈现的页面。默认为文档中的所有页面。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | 要呈现的页面。 |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean-}
```
public void setPrettyFormat(boolean value)
```


当 true 时，漂亮的格式输出适用。默认值为**false**.

调成**true**使 HTML、MHTML、EPUB、WordML、RTF、DOCX 和 ODT 输出人类可读。用于测试或调试。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback-}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


在保存文档期间调用并接受有关保存进度的数据。

保存到时报告进度[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW)， 或者[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) | 相应的[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback)价值。 |

### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


允许控制在将文档导出为固定页面 Html 格式时如何保存资源（图像、字体和 css）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) | 相应的[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback)价值。 |

### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String-}
```
public void setResourcesFolder(String value)
```


指定将文档导出为 Html 格式时保存资源（图像、字体、css）的物理文件夹。默认为空。

只有当[getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedImages-boolean-)财产是假的。

当你保存一个[Document](../../com.aspose.words/document)在 Html 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)允许您指定图像的保存位置和[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-)允许指定图像 URI 的构建方式。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认情况下会将图像保存在保存文档文件的同一文件夹中。利用[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)覆盖此行为。

如果将文档保存到流中，Aspose.Words 没有保存图像的文件夹，但仍需要将图像保存在某个位置。在这种情况下，您需要使用[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)财产

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String-}
```
public void setResourcesFolderAlias(String value)
```


指定用于构造写入 Html 文档的图像 URI 的文件夹的名称。默认为空。

当你保存一个[Document](../../com.aspose.words/document)在 Html 格式中，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-)允许您指定图像的保存位置和[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-)允许指定图像 URI 的构建方式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setSaveFontFaceCssSeparately(boolean value) {#setSaveFontFaceCssSeparately-boolean-}
```
public void setSaveFontFaceCssSeparately(boolean value)
```


 Flag 指示当使用外部样式表保存文档时（即，当[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-)是假的）。默认值为 false ，所有 CSS 规则都写入单个文件“styles.css”。将此属性设置为 true 会恢复旧行为（单独的文件）以与旧代码兼容。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


如果使用此保存选项对象，则指定保存文档的格式。只能是[SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[SaveFormat](../../com.aspose.words/saveformat)常数。 |

### setShowPageBorder(boolean value) {#setShowPageBorder-boolean-}
```
public void setShowPageBorder(boolean value)
```


指定是否应显示页面周围的边框。默认为 true 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。默认情况下，此属性为 null 且不使用临时文件。

当Aspose.Words 保存文档时，它需要创建临时的内部结构。默认情况下，这些内部结构是在内存中创建的，并且在保存文档时内存使用会在短时间内出现峰值。保存完成后，内存将被垃圾收集器释放和回收。

如果您正在保存非常大的文档（数千页）和/或同时处理许多文档，那么保存期间的内存峰值可能会非常大，足以导致系统抛出 java.lang.IndexOutOfBoundsException。使用指定临时文件夹[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)将导致 Aspose.Words 将内部结构保存在临时文件而不是内存中。它会减少保存期间的内存使用量，但会降低保存性能。

该文件夹必须存在且可写，否则会抛出异常。

保存完成后，Aspose.Words 会自动删除所有临时文件。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean-}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。默认值为假；

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值决定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |

### setUpdateFields(boolean value) {#setUpdateFields-boolean-}
```
public void setUpdateFields(boolean value)
```


设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。此属性的默认值为**true**.允许指定是否模仿 MS Word 行为。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定在将文档保存为固定页面格式之前是否应更新某些类型的字段的值。 |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean-}
```
public void setUpdateLastPrintedProperty(boolean value)
```


设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值决定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean-}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值决定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean-}
```
public void setUpdateSdtContent(boolean value)
```


设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 值决定是否内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。 |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean-}
```
public void setUseAntiAliasing(boolean value)
```


设置一个值，确定是否使用抗锯齿进行渲染。

默认值为 false 。当此值设置为 true 时，将使用抗锯齿进行渲染。

当文档导出为以下格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) .当文档导出到[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB)和[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3)格式 此选项用于光栅图像。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否使用抗锯齿进行渲染的值。 |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean-}
```
public void setUseHighQualityRendering(boolean value)
```


设置一个值以确定是否使用高质量（即慢速）渲染算法。默认值为 false 。

当文档导出为图像格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定是否使用高质量的值（即 |

### setUseTargetMachineFonts(boolean value) {#setUseTargetMachineFonts-boolean-}
```
public void setUseTargetMachineFonts(boolean value)
```


标志指示是否必须使用来自目标机器的字体来显示文档。如果此标志设置为真，[getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions\#getFontFormat--) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions\#setFontFormat-int-)和[getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedFonts--) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedFonts-boolean-)属性也没有效果[getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions\#getResourceSavingCallback--) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-)不会因字体而被解雇。默认为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
