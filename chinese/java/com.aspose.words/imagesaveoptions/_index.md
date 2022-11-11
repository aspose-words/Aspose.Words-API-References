---
title: ImageSaveOptions
second_title: Aspose.Words for Java API Reference
description: 允许在将文档页面或形状渲染为图像时指定其他选项。
type: docs
weight: 340
url: /zh/java/com.aspose.words/imagesaveoptions/
---

**遗产:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)

**所有实现的接口:**
java.lang.Cloneable
```
public class ImageSaveOptions extends FixedPageSaveOptions implements Cloneable
```

允许在将文档页面或形状渲染为图像时指定其他选项。

要了解更多信息，请访问**Specify Save Options**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [ImageSaveOptions(int saveFormat)](#ImageSaveOptions-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | 创建适合给定文件名中指定的文件扩展名的类的保存选项对象。 |
| [deepClone()](#deepClone--) | 创建此对象的深层克隆。 |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | 获取一个布尔值，该值指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [get班级()](#get班级--) |  |
| [getColorMode()](#getColorMode--) | 获取一个值，该值确定如何呈现颜色。 |
| [getDefaultTemplate()](#getDefaultTemplate--) | 获取默认模板的路径（包括文件名）。 |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | 获取确定如何渲染 3D 效果的值。 |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | 获取一个值，该值确定如何呈现 DrawingML 效果。 |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | 获取一个值，该值确定如何呈现 DrawingML 形状。 |
| [getExportGeneratorName()](#getExportGeneratorName--) | 如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 |
| [getGraphicsQualityOptions()](#getGraphicsQualityOptions--) | 允许为 java.awt.Graphics2D 对象指定渲染模式和质量。 |
| [getHorizontalResolution()](#getHorizontalResolution--) | 获取生成图像的水平分辨率，以每英寸点数为单位。 |
| [getImageBrightness()](#getImageBrightness--) | 获取生成图像的亮度。 |
| [getImageColorMode()](#getImageColorMode--) | 获取生成图像的颜色模式。 |
| [getImageContrast()](#getImageContrast--) | 获取生成图像的对比度。 |
| [getImlRenderingMode()](#getImlRenderingMode--) | 获取一个值，该值确定如何呈现墨迹 (InkML) 对象。 |
| [getJpegQuality()](#getJpegQuality--) | 获取确定生成的 JPEG 图像质量的值。 |
| [getMemoryOptimization()](#getMemoryOptimization--) | 获取确定是否应在保存文档之前执行内存优化的值。 |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | 允许指定如何在渲染输出中处理元文件。 |
| [getNumeralFormat()](#getNumeralFormat--) | 获取[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。 |
| [getOptimizeOutput()](#getOptimizeOutput--) | Flag 表示是否需要优化输出。 |
| [getPageSavingCallback()](#getPageSavingCallback--) | 允许控制将文档导出为固定页面格式时如何保存单独的页面。 |
| [getPageSet()](#getPageSet--) | 获取要呈现的页面。 |
| [getPaperColor()](#getPaperColor--) | 获取生成图像的背景（纸张）颜色。 |
| [getPixelFormat()](#getPixelFormat--) | 获取生成图像的像素格式。 |
| [getPrettyFormat()](#getPrettyFormat--) | 如果为 true ，则在适用的情况下输出漂亮的格式。 |
| [getProgressCallback()](#getProgressCallback--) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [getSaveFormat()](#getSaveFormat--) | 如果使用此保存选项对象，则指定保存呈现的文档页面或形状的格式。 |
| [getScale()](#getScale--) | 获取生成图像的缩放系数。 |
| [getTempFolder()](#getTempFolder--) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [getThresholdForFloydSteinbergDithering()](#getThresholdForFloydSteinbergDithering--) | 获取确定 Floyd-Steinberg 方法中二值化误差值的阈值。 |
| [getTiffBinarization方法()](#getTiffBinarization方法--) | 获取将图像转换为 1 bpp 格式时使用的方法[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-)是 SaveFormat.Tiff 和[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-)等于 TiffCompression.Ccitt3 或 TiffCompression.Ccitt4。 |
| [getTiffCompression()](#getTiffCompression--) | 获取将生成的图像保存为 TIFF 格式时应用的压缩类型。 |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdate字段()](#getUpdate字段--) | 获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateSdtContent()](#getUpdateSdtContent--) | 获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | 获取一个值，该值确定是否使用抗锯齿进行渲染。 |
| [getUseGdiEmfRenderer()](#getUseGdiEmfRenderer--) | 获取一个值，用于确定在保存到 EMF 时是使用 GDI+ 还是 Aspose.Words 图元文件渲染器。 |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | 获取确定是否使用高质量的值（即 |
| [getVerticalResolution()](#getVerticalResolution--) | 获取生成图像的垂直分辨率，以每英寸点数为单位。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | 设置一个布尔值，指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [setColorMode(int value)](#setColorMode-int-) | 设置一个值来确定如何呈现颜色。 |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | 设置默认模板的路径（包括文件名）。 |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | 设置确定如何渲染 3D 效果的值。 |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 效果。 |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 形状。 |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | 如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 |
| [setGraphicsQualityOptions(GraphicsQualityOptions value)](#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions-) | 允许为 java.awt.Graphics2D 对象指定渲染模式和质量。 |
| [setHorizontalResolution(float value)](#setHorizontalResolution-float-) | 设置生成图像的水平分辨率，以每英寸点数为单位。 |
| [setImageBrightness(float value)](#setImageBrightness-float-) | 设置生成图像的亮度。 |
| [setImageColorMode(int value)](#setImageColorMode-int-) | 设置生成图像的颜色模式。 |
| [setImageContrast(float value)](#setImageContrast-float-) | 设置生成图像的对比度。 |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | 设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [setJpegQuality(int value)](#setJpegQuality-int-) | 设置确定生成的 JPEG 图像质量的值。 |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | 设置值确定是否应在保存文档之前执行内存优化。 |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | 允许指定元文件渲染选项。 |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) | 套[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。 |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Flag 表示是否需要优化输出。 |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | 允许控制将文档导出为固定页面格式时如何保存单独的页面。 |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | 设置要呈现的页面。 |
| [setPaperColor(Color value)](#setPaperColor-java.awt.Color-) | 为生成的图像设置背景（纸张）颜色。 |
| [setPixelFormat(int value)](#setPixelFormat-int-) | 设置生成图像的像素格式。 |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | 如果为 true ，则在适用的情况下输出漂亮的格式。 |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [setResolution(float value)](#setResolution-float-) | 为生成的图像设置水平和垂直分辨率，以每英寸点数为单位。 |
| [setSaveFormat(int value)](#setSaveFormat-int-) | 如果使用此保存选项对象，则指定保存呈现的文档页面或形状的格式。 |
| [setScale(float value)](#setScale-float-) | 设置生成图像的缩放系数。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [setThresholdForFloydSteinbergDithering(byte value)](#setThresholdForFloydSteinbergDithering-byte-) | 设置确定 Floyd-Steinberg 方法中二值化误差值的阈值。 |
| [setTiffBinarization方法(int value)](#setTiffBinarization方法-int-) | 设置将图像转换为 1 bpp 格式时使用的方法[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-)是 SaveFormat.Tiff 和[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-)等于 TiffCompression.Ccitt3 或 TiffCompression.Ccitt4。 |
| [setTiffCompression(int value)](#setTiffCompression-int-) | 设置将生成的图像保存为 TIFF 格式时应用的压缩类型。 |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdate字段(boolean value)](#setUpdate字段-boolean-) | 设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) | 设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)保存前更新。 |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | 设置一个值，确定是否使用抗锯齿进行渲染。 |
| [setUseGdiEmfRenderer(boolean value)](#setUseGdiEmfRenderer-boolean-) | 设置一个值，确定在保存到 EMF 时是否使用 GDI+ 或 Aspose.Words 图元文件渲染器。 |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | 设置一个值来确定是否使用高质量（即 |
| [setVerticalResolution(float value)](#setVerticalResolution-float-) | 设置生成图像的垂直分辨率，以每英寸点数为单位。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ImageSaveOptions(int saveFormat) {#ImageSaveOptions-int-}
```
public ImageSaveOptions(int saveFormat)
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
### deepClone() {#deepClone--}
```
public ImageSaveOptions deepClone()
```


创建此对象的深层克隆。

**退货:**
[ImageSaveOptions](../../com.aspose.words/imagesaveoptions)
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
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


获取一个布尔值，该值指示在保存文档时在文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。默认值为**false**.

请注意，Word 不嵌入 PostScript 字体，但可以打开嵌入了这种类型字体的文档。

此选项仅在以下情况下有效[FontInfoCollection.getEmbedTrue类型Fonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrue类型Fonts--) / [FontInfoCollection.setEmbedTrue类型Fonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrue类型Fonts-boolean-)的[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--)属性设置为 true 。

**退货:**
boolean - 一个布尔值，指示在保存文档中嵌入 True类型 字体时是否允许嵌入带有 PostScript 轮廓的字体。
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
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。默认值为**true**.

**退货:**
boolean - 对应的布尔值。
### getGraphicsQualityOptions() {#getGraphicsQualityOptions--}
```
public GraphicsQualityOptions getGraphicsQualityOptions()
```


允许为 java.awt.Graphics2D 对象指定渲染模式和质量。

使用此属性覆盖 Aspose.Words 引擎默认提供的图形设置。

只有在将文档保存为类似图像的格式时才会生效。

**退货:**
[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) - 相应的[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions)价值。
### getHorizontalResolution() {#getHorizontalResolution--}
```
public float getHorizontalResolution()
```


获取生成图像的水平分辨率，以每英寸点数为单位。

此属性仅在保存为光栅图像格式时有效，并影响以像素为单位的输出大小。

默认值为 96。

**退货:**
float - 生成图像的水平分辨率，以每英寸点数为单位。
### getImageBrightness() {#getImageBrightness--}
```
public float getImageBrightness()
```


获取生成图像的亮度。

此属性仅在保存为光栅图像格式时有效。

默认值为 0.5。该值必须在 0 和 1 之间的范围内。

**退货:**
float - 生成图像的亮度。
### getImageColorMode() {#getImageColorMode--}
```
public int getImageColorMode()
```


获取生成图像的颜色模式。

此属性仅在保存为光栅图像格式时有效。

默认值为[ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**退货:**
 int - 生成图像的颜色模式。返回值是以下之一[ImageColorMode](../../com.aspose.words/imagecolormode)常数。
### getImageContrast() {#getImageContrast--}
```
public float getImageContrast()
```


获取生成图像的对比度。

此属性仅在保存为光栅图像格式时有效。

默认值为 0.5。该值必须在 0 和 1 之间的范围内。

**退货:**
float - 生成图像的对比度。
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


获取一个值，该值确定如何呈现墨迹 (InkML) 对象。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**退货:**
int - 确定如何呈现墨水 (InkML) 对象的值。返回值是以下之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。
### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


获取确定生成的 JPEG 图像质量的值。

仅在保存为 JPEG 时有效。

以 JPEG 格式保存时，使用此属性获取或设置生成图像的质量。该值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。

默认值为 95。

**退货:**
int - 确定生成的 JPEG 图像质量的值。
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


允许指定如何在渲染输出中处理元文件。

什么时候[MetafileRenderingMode.VECTOR](../../com.aspose.words/metafilerenderingmode\#VECTOR)指定时，Aspose.Words 先使用自己的图元文件渲染引擎将图元文件渲染为矢量图形，然后再将矢量图形渲染为图像。

什么时候[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP)指定时，Aspose.Words 使用 GDI+ 图元文件渲染引擎将图元文件直接渲染到图像。

GDI+ 图元文件渲染引擎运行速度更快，支持几乎所有图元文件功能，但与页面上的其余矢量图形（尤其是文本）相比，在低分辨率下可能会产生不一致的结果。 Aspose.Words 元文件渲染引擎即使在低分辨率下也会产生更一致的结果，但工作速度较慢，并且可能不准确地渲染复杂的元文件。

默认值为[MetafileRenderingMode](../../com.aspose.words/metafilerenderingmode)是[MetafileRenderingMode.BITMAP](../../com.aspose.words/metafilerenderingmode\#BITMAP).

**退货:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - 相应的[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions)价值。
### getNumeralFormat() {#getNumeralFormat--}
```
public int getNumeralFormat()
```


获取[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。默认使用欧洲数字。如果此属性的值已更改且页面布局已构建，则[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--)自动调用以更新任何更改。

**退货:**
诠释 -\{[NumeralFormat](../../com.aspose.words/numeralformat)用于渲染数字。返回值是以下之一[NumeralFormat](../../com.aspose.words/numeralformat)常数。
### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Flag 表示是否需要优化输出。如果设置了此标志，则多余的嵌套画布和空画布被删除，具有相同格式的相邻字形也会被连接。注意：如果此属性设置为 true，可能会影响内容显示的准确性。默认为假。

**退货:**
boolean - 对应的布尔值。
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

此属性仅在呈现文档页面时有效。将形状渲染到图像时会忽略此属性。

**退货:**
[PageSet](../../com.aspose.words/pageset) - 要呈现的页面。
### getPaperColor() {#getPaperColor--}
```
public Color getPaperColor()
```


获取生成图像的背景（纸张）颜色。

默认值为 。

当呈现指定了自己的背景颜色的文档页面时，文档背景颜色将覆盖此属性指定的颜色。

**退货:**
java.awt.Color - 生成图像的背景（纸张）颜色。
### getPixelFormat() {#getPixelFormat--}
```
public int getPixelFormat()
```


获取生成图像的像素格式。

此属性仅在保存为光栅图像格式时有效。

默认值为[ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

由于 GDI+ 的工作，输出图像的像素格式可能与设定值不同。

**退货:**
int - 生成图像的像素格式。返回值是以下之一[ImagePixelFormat](../../com.aspose.words/imagepixelformat)常数。
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


如果使用此保存选项对象，则指定保存呈现的文档页面或形状的格式。可以是栅格[SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG)或矢量[SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

在不同的平台上，支持的格式可能不同。其他选项的数量取决于所选格式。

此外，可以通过 ImageSaveOptions 和通过[SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**退货:**
int - 对应的 int 值。返回值是以下之一[SaveFormat](../../com.aspose.words/saveformat)常数。
### getScale() {#getScale--}
```
public float getScale()
```


获取生成图像的缩放系数。默认值为 1.0。该值必须大于 0。

**退货:**
float - 生成图像的缩放系数。
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
### getThresholdForFloydSteinbergDithering() {#getThresholdForFloydSteinbergDithering--}
```
public byte getThresholdForFloydSteinbergDithering()
```


获取确定 Floyd-Steinberg 方法中二值化误差值的阈值。什么时候[ImageBinarization方法](../../com.aspose.words/imagebinarizationmethod)是 ImageBinarization方法.FloydSteinbergDithering。

默认值为 128。

**退货:**
byte - 确定 Floyd-Steinberg 方法中二值化误差值的阈值。
### getTiffBinarization方法() {#getTiffBinarization方法--}
```
public int getTiffBinarization方法()
```


获取将图像转换为 1 bpp 格式时使用的方法[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-)是 SaveFormat.Tiff 和[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-)等于 TiffCompression.Ccitt3 或 TiffCompression.Ccitt4。

默认值为 ImageBinarization方法.Threshold。

**退货:**
int - 将图像转换为 1 bpp 格式时使用的方法[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-)是 SaveFormat.Tiff 和[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-)等于 TiffCompression.Ccitt3 或 TiffCompression.Ccitt4。返回值是以下之一[ImageBinarization方法](../../com.aspose.words/imagebinarizationmethod)常数。
### getTiffCompression() {#getTiffCompression--}
```
public int getTiffCompression()
```


获取将生成的图像保存为 TIFF 格式时应用的压缩类型。

仅在保存到 TIFF 时有效。

默认值为[TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**退货:**
 int - 将生成的图像保存为 TIFF 格式时应用的压缩类型。返回值是以下之一[TiffCompression](../../com.aspose.words/tiffcompression)常数。
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
### getUseGdiEmfRenderer() {#getUseGdiEmfRenderer--}
```
public boolean getUseGdiEmfRenderer()
```


获取一个值，用于确定在保存到 EMF 时是使用 GDI+ 还是 Aspose.Words 图元文件渲染器。

如果设置为 true，则使用 GDI+ 图元文件渲染器。即内容写入 GDI+ 图形对象并保存到元文件。

如果设置为 false，则使用 Aspose.Words 图元文件渲染器。即内容使用Aspose.Words 直接写入元文件格式。

仅在保存到 EMF 时有效。

GDI+ 保存仅适用于 .NET。

默认值是true 。

**退货:**
boolean - 一个值，用于确定在保存到 EMF 时是否使用 GDI+ 或 Aspose.Words 图元文件渲染器。
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


获取确定是否使用高质量（即慢速）渲染算法的值。默认值为 false 。

当文档导出为图像格式时使用此属性：[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**退货:**
boolean - 确定是否使用高质量的值（即
### getVerticalResolution() {#getVerticalResolution--}
```
public float getVerticalResolution()
```


获取生成图像的垂直分辨率，以每英寸点数为单位。

此属性仅在保存为光栅图像格式时有效，并影响以像素为单位的输出大小。

默认值为 96。

**退货:**
float - 生成图像的垂直分辨率，以每英寸点数为单位。
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

### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


设置一个值来确定如何呈现颜色。默认值为[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定如何呈现颜色的值。该值必须是以下之一[ColorMode](../../com.aspose.words/colormode)常数。 |

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

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


如果为 true，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。默认值为**true**.

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setGraphicsQualityOptions(GraphicsQualityOptions value) {#setGraphicsQualityOptions-com.aspose.words.GraphicsQualityOptions-}
```
public void setGraphicsQualityOptions(GraphicsQualityOptions value)
```


允许为 java.awt.Graphics2D 对象指定渲染模式和质量。

使用此属性覆盖 Aspose.Words 引擎默认提供的图形设置。

只有在将文档保存为类似图像的格式时才会生效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions) | 相应的[GraphicsQualityOptions](../../com.aspose.words/graphicsqualityoptions)价值。 |

### setHorizontalResolution(float value) {#setHorizontalResolution-float-}
```
public void setHorizontalResolution(float value)
```


设置生成图像的水平分辨率，以每英寸点数为单位。

此属性仅在保存为光栅图像格式时有效，并影响以像素为单位的输出大小。

默认值为 96。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 生成图像的水平分辨率，以每英寸点数为单位。 |

### setImageBrightness(float value) {#setImageBrightness-float-}
```
public void setImageBrightness(float value)
```


设置生成图像的亮度。

此属性仅在保存为光栅图像格式时有效。

默认值为 0.5。该值必须在 0 和 1 之间的范围内。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 生成图像的亮度。 |

### setImageColorMode(int value) {#setImageColorMode-int-}
```
public void setImageColorMode(int value)
```


设置生成图像的颜色模式。

此属性仅在保存为光栅图像格式时有效。

默认值为[ImageColorMode.NONE](../../com.aspose.words/imagecolormode\#NONE).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 生成图像的颜色模式。该值必须是以下之一[ImageColorMode](../../com.aspose.words/imagecolormode)常数。 |

### setImageContrast(float value) {#setImageContrast-float-}
```
public void setImageContrast(float value)
```


设置生成图像的对比度。

此属性仅在保存为光栅图像格式时有效。

默认值为 0.5。该值必须在 0 和 1 之间的范围内。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 生成图像的对比度。 |

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

### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


设置确定生成的 JPEG 图像质量的值。

仅在保存为 JPEG 时有效。

以 JPEG 格式保存时，使用此属性获取或设置生成图像的质量。该值可能在 0 到 100 之间变化，其中 0 表示质量最差但压缩最大，100 表示质量最好但压缩最小。

默认值为 95。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 确定生成的 JPEG 图像质量的值。 |

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

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Flag 表示是否需要优化输出。如果设置了此标志，则多余的嵌套画布和空画布被删除，具有相同格式的相邻字形也会被连接。注意：如果此属性设置为 true，可能会影响内容显示的准确性。默认为假。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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

此属性仅在呈现文档页面时有效。将形状渲染到图像时会忽略此属性。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | 要呈现的页面。 |

### setPaperColor(Color value) {#setPaperColor-java.awt.Color-}
```
public void setPaperColor(Color value)
```


为生成的图像设置背景（纸张）颜色。

默认值为 。

当呈现指定了自己的背景颜色的文档页面时，文档背景颜色将覆盖此属性指定的颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 生成图像的背景（纸张）颜色。 |

### setPixelFormat(int value) {#setPixelFormat-int-}
```
public void setPixelFormat(int value)
```


设置生成图像的像素格式。

此属性仅在保存为光栅图像格式时有效。

默认值为[ImagePixelFormat.FORMAT\_32\_BPP\_ARGB](../../com.aspose.words/imagepixelformat\#FORMAT-32-BPP-ARGB).

由于 GDI+ 的工作，输出图像的像素格式可能与设定值不同。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 生成图像的像素格式。该值必须是以下之一[ImagePixelFormat](../../com.aspose.words/imagepixelformat)常数。 |

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

### setResolution(float value) {#setResolution-float-}
```
public void setResolution(float value)
```


为生成的图像设置水平和垂直分辨率，以每英寸点数为单位。

此属性仅在保存为光栅图像格式时有效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 生成图像的水平和垂直分辨率，以每英寸点数为单位。 |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


如果使用此保存选项对象，则指定保存呈现的文档页面或形状的格式。可以是栅格[SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG)或矢量[SaveFormat.SVG](../../com.aspose.words/saveformat\#SVG).

在不同的平台上，支持的格式可能不同。其他选项的数量取决于所选格式。

此外，可以通过 ImageSaveOptions 和通过[SvgSaveOptions](../../com.aspose.words/svgsaveoptions).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[SaveFormat](../../com.aspose.words/saveformat)常数。 |

### setScale(float value) {#setScale-float-}
```
public void setScale(float value)
```


设置生成图像的缩放系数。默认值为 1.0。该值必须大于 0。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 生成图像的缩放系数。 |

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

### setThresholdForFloydSteinbergDithering(byte value) {#setThresholdForFloydSteinbergDithering-byte-}
```
public void setThresholdForFloydSteinbergDithering(byte value)
```


设置确定 Floyd-Steinberg 方法中二值化误差值的阈值。什么时候[ImageBinarization方法](../../com.aspose.words/imagebinarizationmethod)是 ImageBinarization方法.FloydSteinbergDithering。

默认值为 128。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte | 确定 Floyd-Steinberg 方法中二值化误差值的阈值。 |

### setTiffBinarization方法(int value) {#setTiffBinarization方法-int-}
```
public void setTiffBinarization方法(int value)
```


设置将图像转换为 1 bpp 格式时使用的方法[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-)是 SaveFormat.Tiff 和[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-)等于 TiffCompression.Ccitt3 或 TiffCompression.Ccitt4。

默认值为 ImageBinarization方法.Threshold。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 将图像转换为 1 bpp 格式时使用的方法[getSaveFormat()](../../com.aspose.words/imagesaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/imagesaveoptions\#setSaveFormat-int-)是 SaveFormat.Tiff 和[getTiffCompression()](../../com.aspose.words/imagesaveoptions\#getTiffCompression--) / [setTiffCompression(int)](../../com.aspose.words/imagesaveoptions\#setTiffCompression-int-)等于 TiffCompression.Ccitt3 或 TiffCompression.Ccitt4。该值必须是以下之一[ImageBinarization方法](../../com.aspose.words/imagebinarizationmethod)常数。 |

### setTiffCompression(int value) {#setTiffCompression-int-}
```
public void setTiffCompression(int value)
```


设置将生成的图像保存为 TIFF 格式时应用的压缩类型。

仅在保存到 TIFF 时有效。

默认值为[TiffCompression.CCITT\_4](../../com.aspose.words/tiffcompression\#CCITT-4).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 将生成的图像保存为 TIFF 格式时应用的压缩类型。该值必须是以下之一[TiffCompression](../../com.aspose.words/tiffcompression)常数。 |

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

### setUseGdiEmfRenderer(boolean value) {#setUseGdiEmfRenderer-boolean-}
```
public void setUseGdiEmfRenderer(boolean value)
```


设置一个值，确定在保存到 EMF 时是否使用 GDI+ 或 Aspose.Words 图元文件渲染器。

如果设置为 true，则使用 GDI+ 图元文件渲染器。即内容写入 GDI+ 图形对象并保存到元文件。

如果设置为 false，则使用 Aspose.Words 图元文件渲染器。即内容使用Aspose.Words 直接写入元文件格式。

仅在保存到 EMF 时有效。

GDI+ 保存仅适用于 .NET。

默认值是true 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，用于确定在保存到 EMF 时是使用 GDI+ 还是 Aspose.Words 图元文件渲染器。 |

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

### setVerticalResolution(float value) {#setVerticalResolution-float-}
```
public void setVerticalResolution(float value)
```


设置生成图像的垂直分辨率，以每英寸点数为单位。

此属性仅在保存为光栅图像格式时有效，并影响以像素为单位的输出大小。

默认值为 96。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | float | 生成图像的垂直分辨率，以每英寸点数为单位。 |

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
