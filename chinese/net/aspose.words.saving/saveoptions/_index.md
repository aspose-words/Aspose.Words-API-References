---
title: SaveOptions Class
linktitle: SaveOptions
articleTitle: SaveOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.SaveOptions 类，它是您自定义文档保存的关键，提供各种格式的高级选项。立即增强您的工作流程！
type: docs
weight: 6380
url: /zh/net/aspose.words.saving/saveoptions/
---
## SaveOptions class

这是一个抽象基类，允许用户在将文档保存为特定格式时指定附加 选项。

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public abstract class SaveOptions
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，指示在保存文档时嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体 。 默认值为`错误的`. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**(Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，该值确定如何呈现墨水（InkML）对象。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为`错误的`. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的` ，在适用的情况下以漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | 如果使用此保存选项对象，则指定将保存文档的格式。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存为 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且不使用临时文件。 |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | 确定字体属性是否根据所使用的字符代码进行更改。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存之前更新。 默认值是`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存之前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [CreateSaveOptions](../../aspose.words.saving/saveoptions/createsaveoptions/#createsaveoptions)(*[SaveFormat](../../aspose.words/saveformat/)*) | 创建适合指定保存格式的类的保存选项对象。 |
| static [CreateSaveOptions](../../aspose.words.saving/saveoptions/createsaveoptions/#createsaveoptions_1)(*string*) | 创建适合给定文件名中指定的文件扩展名的类的保存选项对象。 |

## 评论

的一个实例`SaveOptions`类或任何派生类被传递到流[`Save`](../../aspose.words/document/save/) 或字符串[`Save`](../../aspose.words/document/save/)为用户在保存文档时定义自定义选项而增加的重载。

## 例子

展示如何在将文档保存为 .epub 时使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出的 .epub 文档的所有内容都包含在一个 HTML 部分中。
// 拆分标准允许我们将文档分成几个 HTML 部分。
// 我们将设置标准将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们想要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
