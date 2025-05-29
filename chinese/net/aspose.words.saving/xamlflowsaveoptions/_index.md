---
title: XamlFlowSaveOptions Class
linktitle: XamlFlowSaveOptions
articleTitle: XamlFlowSaveOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.XamlFlowSaveOptions，增强 XamlFlow 格式文档保存功能。解锁高级功能，实现无缝集成！
type: docs
weight: 6500
url: /zh/net/aspose.words.saving/xamlflowsaveoptions/
---
## XamlFlowSaveOptions class

可用于在将文档保存到 时指定附加选项XamlFlow或者XamlFlowPack格式.

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public class XamlFlowSaveOptions : SaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [XamlFlowSaveOptions](xamlflowsaveoptions/#constructor)() | 初始化此类的新实例，可用于将文档保存在XamlFlow格式. |
| [XamlFlowSaveOptions](xamlflowsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | 初始化此类的新实例，可用于将文档保存在XamlFlow 或XamlFlowPack格式. |

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
| [ImageSavingCallback](../../aspose.words.saving/xamlflowsaveoptions/imagesavingcallback/) { get; set; } | 允许控制将文档保存为 XAML 时如何保存图像。 |
| [ImagesFolder](../../aspose.words.saving/xamlflowsaveoptions/imagesfolder/) { get; set; } | 指定将文档导出为 XAML 格式时保存图像的物理文件夹。 默认值为空字符串。 |
| [ImagesFolderAlias](../../aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/) { get; set; } | 指定用于构建写入 XAML 文档的图像 URI 的文件夹的名称。 默认值为空字符串。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，该值确定如何呈现墨水（InkML）对象。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为`错误的`. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的` ，在适用的情况下以漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/xamlflowsaveoptions/replacebackslashwithyensign/) { get; set; } | 指定是否应将反斜杠字符替换为日元符号。 默认值为`错误的`. |
| override [SaveFormat](../../aspose.words.saving/xamlflowsaveoptions/saveformat/) { get; set; } | 指定如果使用此保存选项对象，文档将以哪种格式保存。 只能是XamlFlow. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存为 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且不使用临时文件。 |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | 确定字体属性是否根据所使用的字符代码进行更改。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存之前更新。 默认值是`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存之前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |

## 例子

展示如何打印将文档转换为流式 .xaml 时创建的链接图像的文件名。

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // 创建一个“XamlFlowSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档保存为 XAML 保存格式的方式。
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // 使用“ImagesFolder”属性在本地文件系统中分配一个文件夹，
    // Aspose.Words 将保存文档的所有链接图像。
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // 使用“ImagesFolderAlias”属性来使用此文件夹
    // 构建图像 URI 时，而不是图像文件夹的名称。
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // 由“ImagesFolderAlias”指定的文件夹将需要包含资源，而不是“ImagesFolder”。
    // 我们必须确保该文件夹存在，然后回调的流才能将其资源放入其中。
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// 在将图像的父文档转换为流形式 .xaml 时，计算并打印图像的文件名。
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // 如果我们指定了图像文件夹别名，我们还需要
        // 重定向每个流以将其图像放入别名文件夹中。
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### 也可以看看

* class [SaveOptions](../saveoptions/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
