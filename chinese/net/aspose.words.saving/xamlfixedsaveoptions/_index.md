---
title: Class XamlFixedSaveOptions
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.XamlFixedSaveOptions 班级. 可用于在将文档保存到XamlFixed格式.
type: docs
weight: 5410
url: /zh/net/aspose.words.saving/xamlfixedsaveoptions/
---
## XamlFixedSaveOptions class

可用于在将文档保存到XamlFixed格式.

```csharp
public class XamlFixedSaveOptions : FixedPageSaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [XamlFixedSaveOptions](xamlfixedsaveoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，该值指示是否允许在保存文档中嵌入 TrueType 字体时使用 PostScript 轮廓嵌入字体 。 默认值为 **错误的**. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | 获取或设置一个值，确定如何呈现颜色。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串**(Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **真的**. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | 获取或设置值，确定允许映射哪些文档格式[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/). 仅默认FlatOpc允许映射文档格式。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | 获取或设置一个值，确定 Html 文档中 JPEG 图像的质量。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置值确定是否应在保存文档之前执行内存优化。 此属性的默认值为 **错误的**. |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | 允许指定元文件渲染选项。 |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | 获取或设置[`NumeralFormat`](../numeralformat/)用于渲染数字。 默认使用欧洲数字。 |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | 标志表示是否需要优化输出。 如果设置了这个标志，多余的嵌套画布和空的画布被删除， 也会连接具有相同格式的相邻字形。 注意：内容显示的准确性可能会受到影响，如果此属性设置为 true。 默认为 false。 |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | 允许控制在将文档导出为固定页面格式时如何保存单独的页面。 |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | 获取或设置要渲染的页面。 默认为文档中的所有页面。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 什么时候`真的` , 在适用的情况下输出漂亮的格式。 默认值为 **错误的**. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| [ResourceSavingCallback](../../aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/) { get; set; } | 允许控制在将文档导出为固定页面 Xaml 格式时如何保存资源（图像和字体）。 |
| [ResourcesFolder](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/) { get; set; } | 指定将文档导出为固定页面 Xaml 格式时保存资源（图像和字体）的物理文件夹。 默认为`无效的`. |
| [ResourcesFolderAlias](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/) { get; set; } | 指定用于构造写入固定页面 Xaml 文档的图像 URI 的文件夹的名称。 默认为`无效的`. |
| override [SaveFormat](../../aspose.words.saving/xamlfixedsaveoptions/saveformat/) { get; set; } | 指定使用此保存选项对象时文档将保存的格式。 只能是XamlFixed. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存前更新。 默认值为 false； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **真的**. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存之前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | 获取或设置值确定内容是否[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/)在保存之前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | 确定指定对象的值是否与当前对象相等。 |

### 例子

演示如何打印在将文档转换为固定格式 .xaml 时创建的链接资源的 URI。

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // 创建一个“XamlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们如何将文档保存为 XAML 保存格式。
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // 使用“ResourcesFolder”属性在本地文件系统中分配一个文件夹
    // Aspose.Words 将保存文档的所有链接资源，例如图像和字体。
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // 使用“ResourcesFolderAlias”属性来使用这个文件夹
    // 当构建图像 URI 而不是资源文件夹的名称时。
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // “ResourcesFolderAlias”指定的文件夹需要包含资源，而不是“ResourcesFolder”。
    // 我们必须确保该文件夹存在，然后回调的流才能将其资源放入其中。
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// 计算并打印在转换为固定 .xaml 期间创建的资源的 URI。
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // 如果我们指定了资源文件夹别名，我们还需要
        // 重定向每个流以将其资源放在别名文件夹中。
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### 也可以看看

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


