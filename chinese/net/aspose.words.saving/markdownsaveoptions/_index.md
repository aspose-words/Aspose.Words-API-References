---
title: MarkdownSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 类在将文档保存为Markdown格式时指定其他选项
type: docs
weight: 4950
url: /zh/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

类在将文档保存为Markdown格式时指定其他选项。

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions)() | 初始化此类的新实例，该实例可用于在:::R5:F:Aspose.Words 中保存文档 。 SaveFormat.Markdown:::格式。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，指示是否允许在保存文档时嵌入带有 PostScript 轮廓的字体 。 默认值为 **false** 。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串** (Empty)。 |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding) { get; set; } | 指定以文本格式导出时要使用的编码。 默认值为 **Encoding.UTF8** 。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **true** 。 |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode) { get; set; } | 指定页眉和页脚导出为文本格式的方式。 默认值为PrimaryOnly。 |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64) { get; set; } | 指定图像是否以 Base64 格式保存到输出文件。 默认为` false` 。 |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许通过[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping)映射哪些文档格式。 默认只允许映射FlatOpc文档格式。 |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks) { get; set; } | 允许指定在导出期间是否应保留分页符。 |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback) { get; set; } | 允许控制将文档保存到 Markdown时图像的保存方式格式。 |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder) { get; set; } | 指定将文档导出到 Markdown时保存图像的物理文件夹格式。默认为空字符串。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为 **false** 。 |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak) { get; set; } | 指定以文本格式导出时用作分节符的字符串。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 当` true` 时，在适用的情况下输出漂亮的格式。 默认值为 **false** 。 |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat) { get; set; } | 如果使用此保存选项对象，则指定保存文档的格式。 只能是Markdown。 |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment) { get; set; } | 获取或设置一个值，该值指定在导出到:::R5:F:Aspose.Words 时如何对齐表 中的内容。 SaveFormat.Markdown:::格式。 默认值为Auto。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为` null` 并且不使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性是否在保存之前更新。 默认值为假； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **true** 。 |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，该值确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性是否在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性是否在保存前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置确定[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)的内容是否在保存前更新的值。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |

### 也可以看看

* class [TxtSaveOptionsBase](../txtsaveoptionsbase)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
