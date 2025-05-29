---
title: MarkdownSaveOptions Class
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.MarkdownSaveOptions，增强 Markdown 格式文档保存功能。立即使用高级选项自定义您的输出！
type: docs
weight: 6060
url: /zh/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

类用于在将文档保存到Markdown格式.

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | 初始化此类的新实例，可用于保存 document 在Markdown格式. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，指示在保存文档时嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体 。 默认值为`错误的`. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**(Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [EmptyParagraphExportMode](../../aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/) { get; set; } | 指定如何将空段落导出到 Markdown。 默认值为EmptyLine. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | 指定以文本格式导出时使用的编码。 默认值为**编码.UTF8**. |
| [ExportAsHtml](../../aspose.words.saving/markdownsaveoptions/exportashtml/) { get; set; } | 允许指定要作为原始 HTML 导出到 Markdown 的元素。 默认值为None. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`. |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | 指定页眉和页脚导出为文本格式的方式。 默认值为PrimaryOnly. |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | 指定是否将图像以 Base64 格式保存到输出文件。 默认值为`错误的`. |
| [ExportUnderlineFormatting](../../aspose.words.saving/markdownsaveoptions/exportunderlineformatting/) { get; set; } | 获取或设置一个布尔值，指示将下划线 文本格式导出为两个加号字符“++”的序列。 默认值为`错误的`. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | 允许指定在导出期间是否保留分页符。 |
| [ImageResolution](../../aspose.words.saving/markdownsaveoptions/imageresolution/) { get; set; } | 指定导出到 Markdown 时图像的输出分辨率。 默认值为`96 dpi`. |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | 允许控制将文档保存到 时如何保存图像Markdown格式. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | 指定将文档导出到时保存图像的物理文件夹Markdown格式。默认为空字符串。 |
| [ImagesFolderAlias](../../aspose.words.saving/markdownsaveoptions/imagesfolderalias/) { get; set; } | 指定用于构建写入文档的图像 URI 的文件夹的名称。 默认值为空字符串。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，该值确定如何呈现墨水（InkML）对象。 |
| [LinkExportMode](../../aspose.words.saving/markdownsaveoptions/linkexportmode/) { get; set; } | 指定如何将链接写入输出文件。 默认值为Auto. |
| [ListExportMode](../../aspose.words.saving/markdownsaveoptions/listexportmode/) { get; set; } | 指定列表项如何写入输出文件。 默认值为MarkdownSyntax. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为`错误的`. |
| [OfficeMathExportMode](../../aspose.words.saving/markdownsaveoptions/officemathexportmode/) { get; set; } | 指定 OfficeMath 如何写入输出文件。 默认值为Text. |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | 指定以文本格式导出时用作段落分隔符的字符串。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的` ，在适用的情况下以漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | 指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是Markdown. |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | 获取或设置一个值，该值指定在导出到表 时如何对齐表中的内容Markdown格式. 默认值为Auto. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存为 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且不使用临时文件。 |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | 确定字体属性是否根据所使用的字符代码进行更改。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存之前更新。 默认值是`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存之前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |

## 例子

展示如何在保存到 Markdown 文档时重命名图像名称。

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // 如果我们将包含图像的文档转换为 Markdown，我们最终会得到一个链接到多个图像的 Markdown 文件。
    // 每个图像都将以文件的形式存储在本地文件系统中。
    // 还有一个回调可以自定义每个图像的名称和文件系统位置。
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // 此时我们的回调的 ImageSaving() 方法将会运行。
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// 重命名保存 Markdown 文档时生成的已保存图像。
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        args.ImageFileName = imageFileName;
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### 也可以看看

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
