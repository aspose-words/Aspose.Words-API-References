---
title: DocSaveOptions
second_title: Aspose.Words for Java API 参考
description: 将文档保存为 或 格式时，可用于指定附加选项。
type: docs
weight: 119
url: /zh/java/com.aspose.words/docsaveoptions/
---

**遗产：**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)
```
public class DocSaveOptions extends SaveOptions
```

可用于在将文档保存到[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC)或者[SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT)格式。

要了解更多信息，请访问**Specify Save Options**文档文章。

目前只提供[getSaveFormat()](../../com.aspose.words/docsaveoptions\#getSaveFormat--) / [setSaveFormat(int)](../../com.aspose.words/docsaveoptions\#setSaveFormat-int-)属性，但将来会添加其他选项，例如加密密码或数字签名设置。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [DocSaveOptions()](#DocSaveOptions--) | 初始化此类的一个新实例，该实例可用于将文档保存在[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC)格式。 |
| [DocSaveOptions(int saveFormat)](#DocSaveOptions-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | 创建适合给定文件名中指定的文件扩展名的类的保存选项对象。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | 获取一个布尔值，指示在保存文档时在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [getAlwaysCompressMetafiles()](#getAlwaysCompressMetafiles--) | 当为 false 时，出于性能原因不压缩小图元文件。 |
| [getClass()](#getClass--) |  |
| [getDefaultTemplate()](#getDefaultTemplate--) | 获取默认模板的路径（包括文件名）。 |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | 获取确定如何呈现 3D 效果的值。 |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | 获取确定如何呈现 DrawingML 效果的值。 |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | 获取确定如何呈现 DrawingML 形状的值。 |
| [getExportGeneratorName()](#getExportGeneratorName--) | 当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。 |
| [getImlRenderingMode()](#getImlRenderingMode--) | 获取确定如何呈现墨迹 (InkML) 对象的值。 |
| [getMemoryOptimization()](#getMemoryOptimization--) | 获取确定在保存文档之前是否应执行内存优化的值。 |
| [getPassword()](#getPassword--) | 获取/设置密码以使用 RC4 加密方法加密文档。 |
| [getPrettyFormat()](#getPrettyFormat--) | 当 true 时，漂亮的格式输出适用。 |
| [getProgressCallback()](#getProgressCallback--) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [getSaveFormat()](#getSaveFormat--) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [getSavePictureBullet()](#getSavePictureBullet--) | 当为 false 时，PictureBullet 数据不会保存到输出文档中。 |
| [getSaveRoutingSlip()](#getSaveRoutingSlip--) | 当为 false 时，RoutingSlip 数据不会保存到输出文档。 |
| [getTempFolder()](#getTempFolder--) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateFields()](#getUpdateFields--) | 获取一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) | 获取一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [getUpdateSdtContent()](#getUpdateSdtContent--) | 获取确定内容是否为[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。 |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | 获取一个值，该值确定是否对渲染使用抗锯齿。 |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | 获取确定是否使用高质量的值（即 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | 设置一个布尔值，指示在保存文档时在文档中嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体。 |
| [setAlwaysCompressMetafiles(boolean value)](#setAlwaysCompressMetafiles-boolean-) | 当为 false 时，出于性能原因不压缩小图元文件。 |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | 将路径设置为默认模板（包括文件名）。 |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | 设置确定 3D 效果呈现方式的值。 |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 效果。 |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | 设置一个值，确定如何呈现 DrawingML 形状。 |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | 当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。 |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | 设置一个值，确定如何呈现墨迹 (InkML) 对象。 |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | 设置确定在保存文档之前是否应执行内存优化的值。 |
| [setPassword(String value)](#setPassword-java.lang.String-) | 获取/设置密码以使用 RC4 加密方法加密文档。 |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | 当 true 时，漂亮的格式输出适用。 |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | 在保存文档期间调用并接受有关保存进度的数据。 |
| [setSaveFormat(int value)](#setSaveFormat-int-) | 如果使用此保存选项对象，则指定保存文档的格式。 |
| [setSavePictureBullet(boolean value)](#setSavePictureBullet-boolean-) | 当为 false 时，PictureBullet 数据不会保存到输出文档中。 |
| [setSaveRoutingSlip(boolean value)](#setSaveRoutingSlip-boolean-) | 当为 false 时，RoutingSlip 数据不会保存到输出文档。 |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | 设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-)属性在保存前更新。 |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) | 设置一个值，确定是否[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-)属性在保存前更新。 |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) | 设置值确定内容是否[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)在保存之前更新。 |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | 设置一个值，确定是否使用抗锯齿进行渲染。 |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | 设置一个值确定是否使用高质量（即 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DocSaveOptions() {#DocSaveOptions--}
```
public DocSaveOptions()
```


初始化此类的一个新实例，该实例可用于将文档保存在[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC)格式。

### DocSaveOptions(int saveFormat) {#DocSaveOptions-int-}
```
public DocSaveOptions(int saveFormat)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

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
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

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
### getAlwaysCompressMetafiles() {#getAlwaysCompressMetafiles--}
```
public boolean getAlwaysCompressMetafiles()
```


当为 false 时，出于性能原因不压缩小图元文件。默认值为**true**所有图元文件都被压缩，无论其大小如何。

**退货：**
boolean - 相应的布尔值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
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
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。默认值为**true**.

**退货：**
boolean - 相应的布尔值。
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


获取确定如何呈现墨迹 (InkML) 对象的值。默认值为[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

当文档导出为固定页面格式时使用此属性。

**退货：**
int - 确定如何呈现墨迹 (InkML) 对象的值。返回值是其中之一[ImlRenderingMode](../../com.aspose.words/imlrenderingmode)常数。
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


获取确定在保存文档之前是否应执行内存优化的值。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的保存时间为代价保存大型文档。

**退货：**
布尔值 - 确定在保存文档之前是否应执行内存优化的值。
### getPassword() {#getPassword--}
```
public String getPassword()
```


获取/设置密码以使用 RC4 加密方法加密文档。

为了在不加密的情况下保存文档，此属性应为 null 或空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
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
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


如果使用此保存选项对象，则指定保存文档的格式。可[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC)或者[SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT).

**退货：**
int - 相应的 int 值。返回值是其中之一[SaveFormat](../../com.aspose.words/saveformat)常数。
### getSavePictureBullet() {#getSavePictureBullet--}
```
public boolean getSavePictureBullet()
```


当为 false 时，PictureBullet 数据不会保存到输出文档中。默认值为**true**.

此选项是为 Word 97 提供的，它不能正确处理 PictureBullet 数据。要删除 PictureBullet 数据，请将选项设置为“false”。

**退货：**
boolean - 相应的布尔值。
### getSaveRoutingSlip() {#getSaveRoutingSlip--}
```
public boolean getSaveRoutingSlip()
```


当为 false 时，RoutingSlip 数据不会保存到输出文档。默认值为**true**.

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

### setAlwaysCompressMetafiles(boolean value) {#setAlwaysCompressMetafiles-boolean-}
```
public void setAlwaysCompressMetafiles(boolean value)
```


当为 false 时，出于性能原因不压缩小图元文件。默认值为**true**所有图元文件都被压缩，无论其大小如何。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


当为真时，导致 Aspose.Words 的名称和版本被嵌入到生成的文件中。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


设置确定在保存文档之前是否应执行内存优化的值。此属性的默认值为**false**.将此选项设置为 true 可以显着减少内存消耗，同时以较慢的保存时间为代价保存大型文档。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 确定在保存文档之前是否应执行内存优化的值。 |

### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


获取/设置密码以使用 RC4 加密方法加密文档。

为了在不加密的情况下保存文档，此属性应为 null 或空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

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

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


如果使用此保存选项对象，则指定保存文档的格式。可[SaveFormat.DOC](../../com.aspose.words/saveformat\#DOC)或者[SaveFormat.DOT](../../com.aspose.words/saveformat\#DOT).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[SaveFormat](../../com.aspose.words/saveformat)常数。 |

### setSavePictureBullet(boolean value) {#setSavePictureBullet-boolean-}
```
public void setSavePictureBullet(boolean value)
```


当为 false 时，PictureBullet 数据不会保存到输出文档中。默认值为**true**.

此选项是为 Word 97 提供的，它不能正确处理 PictureBullet 数据。要删除 PictureBullet 数据，请将选项设置为“false”。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setSaveRoutingSlip(boolean value) {#setSaveRoutingSlip-boolean-}
```
public void setSaveRoutingSlip(boolean value)
```


当为 false 时，RoutingSlip 数据不会保存到输出文档。默认值为**true**.

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
