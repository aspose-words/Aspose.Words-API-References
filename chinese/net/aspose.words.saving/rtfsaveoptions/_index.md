---
title: RtfSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 可用于在将文档保存为Rtf格式时指定附加选项
type: docs
weight: 5240
url: /zh/net/aspose.words.saving/rtfsaveoptions/
---
## RtfSaveOptions class

可用于在将文档保存为Rtf格式时指定附加选项。

```csharp
public class RtfSaveOptions : SaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [RtfSaveOptions](rtfsaveoptions)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，指示是否允许在保存文档时嵌入带有 PostScript 轮廓的字体 。 默认值为 **false** 。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串** (Empty)。 |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportCompactSize](../../aspose.words.saving/rtfsaveoptions/exportcompactsize) { get; set; } | 允许使输出 RTF 文档的大小更小，但如果它们包含 RTL（从右到左）文本，则不会正确显示。 默认值为` false` 。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **true** 。 |
| [ExportImagesForOldReaders](../../aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders) { get; set; } | 指定“老读者”的关键字是否写入 RTF。 这会显着影响 RTF 文档的大小。 默认值为` true` 。 |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许通过[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping)映射哪些文档格式。 默认只允许映射FlatOpc文档格式。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为 **false** 。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 当` true` 时，在适用的情况下输出漂亮的格式。 默认值为 **false** 。 |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/rtfsaveoptions/saveformat) { get; set; } | 如果使用此保存选项对象，则指定保存文档的格式。 只能是Rtf。 |
| [SaveImagesAsWmf](../../aspose.words.saving/rtfsaveoptions/saveimagesaswmf) { get; set; } | 如果为真，所有图像都将保存为 WMF。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为` null` 并且不使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性是否在保存之前更新。 默认值为假； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **true** 。 |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，该值确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性是否在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性是否在保存前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置确定[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)的内容是否在保存前更新的值。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |

### 例子

显示如何使用自定义选项将文档保存为 .rtf。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

 // 创建一个“RtfSaveOptions”对象以传递给文档的“Save”方法来修改我们如何将其保存到 RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// 将“ExportCompactSize”属性设置为“true” to
 // 以从右到左的文本兼容性为代价减小保存文档的大小。
options.ExportCompactSize = true;

 // 将“ExportImagesFotOldReaders”属性设置为“true”以使用额外的关键字来确保我们的文档是
 // 与 Microsoft Word 97 之前的阅读器和写字板兼容。
 // 将“ExportImagesFotOldReaders”属性设置为“false”以减小文档的大小，
 // 但要防止老读者能够读取文档可能包含的任何非元文件或 BMP 图像。
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### 也可以看看

* class [SaveOptions](../saveoptions)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
