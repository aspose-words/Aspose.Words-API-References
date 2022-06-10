---
title: TxtSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 可用于在将文档保存为Text格式时指定其他选项
type: docs
weight: 5330
url: /zh/net/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class

可用于在将文档保存为Text格式时指定其他选项。

```csharp
public class TxtSaveOptions : TxtSaveOptionsBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [TxtSaveOptions](txtsaveoptions)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AddBidiMarks](../../aspose.words.saving/txtsaveoptions/addbidimarks) { get; set; } | 指定以纯文本格式导出时是否在每次 BiDi 运行之前添加双向标记。 |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，指示是否允许在保存文档时嵌入带有 PostScript 轮廓的字体 。 默认值为 **false** 。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串** (Empty)。 |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding) { get; set; } | 指定以文本格式导出时要使用的编码。 默认值为 **Encoding.UTF8** 。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **true** 。 |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode) { get; set; } | 指定页眉和页脚导出为文本格式的方式。 默认值为PrimaryOnly。 |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许通过[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping)映射哪些文档格式。 默认只允许映射FlatOpc文档格式。 |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks) { get; set; } | 允许指定在导出期间是否应保留分页符。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [ListIndentation](../../aspose.words.saving/txtsaveoptions/listindentation) { get; } | 获取一个 ListIndentation 对象，该对象指定用于列表级别缩进的字符数和字符数。 默认情况下，字符 '\0' 的计数为零，这意味着没有缩进。 |
| [MaxCharactersPerLine](../../aspose.words.saving/txtsaveoptions/maxcharactersperline) { get; set; } | 获取或设置指定每行最大字符数的整数值。 默认值为 0，表示没有限制。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为 **false** 。 |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak) { get; set; } | 指定以文本格式导出时用作分节符的字符串。 |
| [PreserveTableLayout](../../aspose.words.saving/txtsaveoptions/preservetablelayout) { get; set; } | 指定程序在以纯文本格式保存时是否应尝试保留表格布局。 默认值为 **false** 。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 当` true` 时，在适用的情况下输出漂亮的格式。 默认值为 **false** 。 |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/txtsaveoptions/saveformat) { get; set; } | 如果使用此保存选项对象，则指定保存文档的格式。 只能是Text。 |
| [SimplifyListLabels](../../aspose.words.saving/txtsaveoptions/simplifylistlabels) { get; set; } | 指定程序是否应在 复杂的标签格式不能用纯文本充分表示的情况下简化列表标签。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为` null` 并且不使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性是否在保存之前更新。 默认值为假； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **true** 。 |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，该值确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性是否在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性是否在保存前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置确定[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)的内容是否在保存前更新的值。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |

### 例子

显示如何使用自定义分节符保存 .txt 文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

 // 创建一个“TxtSaveOptions”对象，我们可以将它传递给文档的“Save”方法
 // 修改我们如何将文档保存为纯文本。
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

 // 将“ParagraphBreak”设置为我们希望放在每个段落末尾的自定义值。
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### 也可以看看

* class [TxtSaveOptionsBase](../txtsaveoptionsbase)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
