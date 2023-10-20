---
title: FixedPageSaveOptions Class
linktitle: FixedPageSaveOptions
articleTitle: FixedPageSaveOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.FixedPageSaveOptions 班级. 包含将文档保存为固定页面格式PDFXPS 图像等时可以指定的常用选项 在 C#.
type: docs
weight: 5020
url: /zh/net/aspose.words.saving/fixedpagesaveoptions/
---
## FixedPageSaveOptions class

包含将文档保存为固定页面格式（PDF、XPS、 图像等）时可以指定的常用选项。

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public abstract class FixedPageSaveOptions : SaveOptions
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，指示在保存的文档中嵌入 TrueType 字体时是否允许使用 PostScript 轮廓嵌入字体。 默认值为`错误的`. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | 获取或设置一个确定颜色呈现方式的值。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**（Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个确定如何渲染 3D 效果的值。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现墨迹 (InkML) 对象。 |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | 获取或设置决定 Html 文档内 JPEG 图像质量的值。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定在保存文档之前是否应执行内存优化的值。 此属性的默认值为`错误的`. |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | 允许指定图元文件渲染选项。 |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | 获取或设置[`NumeralFormat`](../numeralformat/)用于呈现数字。 默认使用欧洲数字。 |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | 标志指示是否需要优化输出。 如果设置此标志，则冗余嵌套画布并删除空画布， 还将连接具有相同格式的相邻字形。 注意：如果出现以下情况，内容显示的准确性可能会受到影响该属性设置为`真的`. 默认为`错误的`. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | 允许控制将文档导出为固定页面格式时如何保存单独的页面。 |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | 获取或设置要呈现的页面。 默认为文档中的所有页面。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的`，在适用的情况下漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| abstract [SaveFormat](../../aspose.words.saving/saveoptions/saveformat/) { get; set; } | 指定使用此保存选项对象时保存文档的格式。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存前更新。 默认值为`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | 确定指定对象的值是否等于当前对象。 |

## 例子

演示如何将文档的每一页渲染为单独的 TIFF 图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // 将“PageSet”属性设置为第一页的页码
    // 从哪个开始渲染文档。
    options.PageSet = new PageSet(i);
    // 以 2325x5325 像素和 600 dpi 导出页面。
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

演示如何将文档中的一页渲染为 JPEG 图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// 将“PageSet”设置为“1”以通过以下方式选择第二页
// 开始渲染文档的从零开始的索引。
options.PageSet = new PageSet(1);

// 当我们将文档保存为 JPEG 格式时，Aspose.Words 只渲染一页。
// 该图像将包含从第二页开始的一页，
// 这只是原始文档的第二页。
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### 也可以看看

* class [SaveOptions](../saveoptions/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
