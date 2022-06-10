---
title: SvgSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 可用于在将文档保存为Svg格式时指定其他选项
type: docs
weight: 5270
url: /zh/net/aspose.words.saving/svgsaveoptions/
---
## SvgSaveOptions class

可用于在将文档保存为Svg格式时指定其他选项。

```csharp
public class SvgSaveOptions : FixedPageSaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SvgSaveOptions](svgsaveoptions)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，指示是否允许在保存文档时嵌入带有 PostScript 轮廓的字体 。 默认值为 **false** 。 |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | 获取或设置一个值，确定如何呈现颜色。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串** (Empty)。 |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportEmbeddedImages](../../aspose.words.saving/svgsaveoptions/exportembeddedimages) { get; set; } | 指定图像是否应该作为base64嵌入到SVG文档中。 注意设置此标志可以显着增加输出 SVG 文件的大小。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **true** 。 |
| [FitToViewPort](../../aspose.words.saving/svgsaveoptions/fittoviewport) { get; set; } | 指定输出 SVG 是否应填充可用视口区域（浏览器窗口或容器）。 当设置为真时，输出 SVG 的宽度和高度设置为 100%。 |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许通过[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping)映射哪些文档格式。 默认只允许映射FlatOpc文档格式。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | 获取或设置确定 Html 文档中 JPEG 图像质量的值。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为 **false** 。 |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | 允许指定元文件渲染选项。 |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | 获取或设置[`NumeralFormat`](../numeralformat)用于呈现数字。 默认使用欧洲数字。 |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Flag 表示是否需要优化输出。 如果设置了这个标志，多余的嵌套画布和空画布被删除， 也会连接具有相同格式的相邻字形。 注意:如果该属性设置为true，可能会影响内容显示的准确性。 默认为假。 |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | 允许控制在将文档导出为固定页面格式时如何保存单独的页面。 |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | 获取或设置要呈现的页面。 默认是文档中的所有页面。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 当` true` 时，在适用的情况下输出漂亮的格式。 默认值为 **false** 。 |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| [ResourceSavingCallback](../../aspose.words.saving/svgsaveoptions/resourcesavingcallback) { get; set; } | 允许控制在将文档导出为 SVG 格式时如何保存资源（图像）。 |
| [ResourcesFolder](../../aspose.words.saving/svgsaveoptions/resourcesfolder) { get; set; } | 指定将文档导出为 Svg 格式时保存资源（图像）的物理文件夹。 默认为` null` 。 |
| [ResourcesFolderAlias](../../aspose.words.saving/svgsaveoptions/resourcesfolderalias) { get; set; } | 指定用于构造写入 SVG 文档的图像 URI 的文件夹的名称。 默认为` null` 。 |
| override [SaveFormat](../../aspose.words.saving/svgsaveoptions/saveformat) { get; set; } | 如果使用此保存选项对象，则指定保存文档的格式。 只能是Svg。 |
| [ShowPageBorder](../../aspose.words.saving/svgsaveoptions/showpageborder) { get; set; } | 控制是否在页面轮廓中添加边框。 默认为` true` 。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为` null` 并且不使用临时文件。 |
| [TextOutputMode](../../aspose.words.saving/svgsaveoptions/textoutputmode) { get; set; } | 获取或设置一个值，确定文本在 SVG 中的呈现方式。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性是否在保存之前更新。 默认值为假； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **true** 。 |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，该值确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性是否在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性是否在保存前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置确定[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)的内容是否在保存前更新的值。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | 确定指定对象的值是否与当前对象相等。 |

### 例子

显示如何操作和打印在将文档转换为 .svg 时创建的链接资源的 URI。

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// 在转换为 .svg.
 时计算并打印包含的资源的 URI
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### 也可以看看

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
