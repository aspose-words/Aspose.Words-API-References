---
title: HtmlFixedSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 可用于在将文档保存为HtmlFixed格式时指定附加选项
type: docs
weight: 4770
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

可用于在将文档保存为HtmlFixed格式时指定附加选项。

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，指示是否允许在保存文档时嵌入带有 PostScript 轮廓的字体 。 默认值为 **false** 。 |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | 获取或设置一个值，确定如何呈现颜色。 |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix) { get; set; } | 指定添加到 style.css 文件中所有类名的前缀。 默认值为` "aw"` 。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串** (Empty)。 |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding) { get; set; } | 指定导出到 HTML 时使用的编码。 默认值为` new UTF8Encoding(true)` （带有 BOM 的 UTF-8）。 |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss) { get; set; } | 指定是否应将 CSS（层叠样式表）嵌入到 Html 文档中。 |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts) { get; set; } | 指定字体是否应该嵌入到 Base64 格式的 Html 文档中。 注意设置这个标志可以显着增加输出 Html 文件的大小。 |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages) { get; set; } | 指定图像是否应嵌入到 Base64 格式的 Html 文档中。 注意设置这个标志可以显着增加输出 Html 文件的大小。 |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg) { get; set; } | 指定是否应将 SVG 资源嵌入到 Html 文档中。 默认值为` true` 。 |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields) { get; set; } | 获取或设置表单字段是否导出为交互式 项目（作为“输入”标签）而不是转换为文本或图形的指示。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **true** 。 |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许通过[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping)映射哪些文档格式。 默认只允许映射FlatOpc文档格式。 |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat) { get; set; } | 获取或设置[`ExportFontFormat`](../exportfontformat)用于字体导出。 默认值为Woff。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | 获取或设置确定 Html 文档中 JPEG 图像质量的值。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为 **false** 。 |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | 允许指定元文件渲染选项。 |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | 获取或设置[`NumeralFormat`](../numeralformat)用于呈现数字。 默认使用欧洲数字。 |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput) { get; set; } | Flag 表示是否需要优化输出。 如果设置了此标志，则多余的嵌套画布和空画布被删除， 也将连接具有相同格式的相邻字形。 注意:如果该属性设置为true，可能会影响内容显示的准确性。 默认为真。 |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment) { get; set; } | 指定 HTML 文档中页面的水平对齐方式。 默认值为` HtmlFixedHorizontalPageAlignment.Center` 。 |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins) { get; set; } | 指定 HTML 文档中页面周围的边距。 边距值以磅为单位，应等于或大于 0。 默认值为 10 磅。 |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | 允许控制在将文档导出为固定页面格式时如何保存单独的页面。 |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | 获取或设置要呈现的页面。 默认是文档中的所有页面。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 当` true` 时，在适用的情况下输出漂亮的格式。 默认值为 **false** 。 |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback) { get; set; } | 允许控制在将文档导出为固定页面 Html 格式时如何保存资源（图像、字体和 css）。 |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder) { get; set; } | 指定将文档导出为 Html 格式时保存资源（图像、字体、css）的物理文件夹。 默认为` null` 。 |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias) { get; set; } | 指定用于构造写入 Html 文档的图像 URI 的文件夹的名称。 默认为` null` 。 |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately) { get; set; } | 标志指示是否应将“@font-face” CSS 规则放入单独的文件“fontFaces.css” 当文档正在使用外部样式表保存（即，当[`ExportEmbeddedCss`](./exportembeddedcss) 为` false` ）。 默认值为` false` ，所有 CSS 规则都写入单个文件“styles.css”。 |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat) { get; set; } | 如果使用此保存选项对象，则指定保存文档的格式。 只能是HtmlFixed。 |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder) { get; set; } | 指定是否应显示页面边框。 默认为` true` 。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为` null` 并且不使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性是否在保存之前更新。 默认值为假； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **true** 。 |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，该值确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性是否在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性是否在保存前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置确定[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)的内容是否在保存前更新的值。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts) { get; set; } | 标志指示是否必须使用来自目标机器的字体来显示文档。 如果此标志设置为 true，则[`FontFormat`](./fontformat)和HtmlFixedSaveOptions。ExportEmbeddedFonts属性无效， 也[`ResourceSavingCallback`](./resourcesavingcallback)不会为字体触发。 默认为假。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | 确定指定对象的值是否与当前对象相等。 |

### 例子

展示如何使用回调来打印在将文档转换为 HTML 时创建的外部资源的 URI。

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

     // ResourcesFolderAlias 指定的文件夹将包含资源而不是 ResourcesFolder.
     // 我们必须确保文件夹存在，然后流才能将其资源放入其中。
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
 /// 在转换为固定的 HTML 时计算并打印包含的资源的 URI。
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
         // 如果我们在 SaveOptions 对象中设置一个文件夹别名，我们将能够从这里打印它。
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                 // 默认情况下，'ResourceFileUri' 使用字体的系统文件夹。
                // 为了避免在其他平台上出现问题，您必须明确指定字体的路径。
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

         // 如果我们在“ResourcesFolderAlias”属性中指定了一个文件夹，
         // 我们还需要重定向每个流以将其资源放入该文件夹中。
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### 也可以看看

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
