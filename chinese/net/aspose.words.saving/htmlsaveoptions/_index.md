---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.HtmlSaveOptions 班级. 可用于在将文档保存到 时指定附加选项HtmlMhtmlEpub Azw3或者Mobi格式 在 C#.
type: docs
weight: 5110
url: /zh/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

可用于在将文档保存到 时指定附加选项Html,Mhtml,Epub, Azw3或者Mobi格式.

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public class HtmlSaveOptions : SaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | 初始化此类的一个新实例，该实例可用于将 document 保存在Html格式. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | 初始化此类的一个新实例，该实例可用于将 document 保存在Html,Mhtml,Epub, Azw3或者Mobi格式. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，指示在保存的文档中嵌入 TrueType 字体时是否允许使用 PostScript 轮廓嵌入字体。 默认值为`错误的`. |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | 指定保存为 HTML、MHTML 或 EPUB 时段落的左右负缩进是否标准化 。默认值为`错误的`. |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | 指定添加到所有 CSS 类名称的前缀。 默认值为空字符串，生成的 CSS 类名称没有公共前缀。 |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | 允许控制将文档保存为 HTML、MHTML 或 EPUB 时 CSS 样式的保存方式。 |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | 指定将文档 导出为 HTML 时写入的级联样式表 (CSS) 文件的路径和名称。 默认为空字符串。 |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | 指定如何将 CSS（层叠样式表）样式导出为 HTML、MHTML 或 EPUB。 默认值为Inline对于 HTML/MHTML 和 External对于 EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**（Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个确定如何渲染 3D 效果的值。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | 允许控制将文档保存为 HTML 或 EPUB 时如何保存文档部分。 |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | 指定保存时文档应如何分割Html, Epub或者Azw3格式。 默认为None对于 HTML 和 HeadingParagraph适用于 EPUB 和 AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | 指定分割文档的最大标题级别。 默认值为`2`. |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | 指定导出为 HTML、MHTML 或 EPUB 时使用的编码。 默认值为`新的 UTF8 编码（假）`（UTF-8 无 BOM）. |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | 指定是否使用 CID (Content-ID) URL 来引用 MHTML 文档中包含的资源（图像、字体、CSS）。默认值为`错误的`. |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | 指定是否将内置和自定义文档属性导出为 HTML、MHTML 或 EPUB。 默认值为`错误的`. |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | 控制如何将下拉表单字段保存为 HTML 或 MHTML。 默认值为`错误的`. |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | 指定是否应将字体资源导出为 HTML、MHTML 或 EPUB。 默认为`错误的`. |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | 指定字体资源是否应以 Base64 编码嵌入到 HTML 中。 默认为`错误的`. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`. |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | 指定页眉和页脚如何输出为 HTML、MHTML 或 EPUB。 默认值为PerSection对于 HTML/MHTML 和None对于 EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | 指定图像是否以 Base64 格式保存到输出 HTML、MHTML 或 EPUB。 默认为`错误的`. |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | 指定是否将语言信息导出为 HTML、MHTML 或 EPUB。 默认为`错误的`. |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | 控制列表标签如何输出为 HTML、MHTML 或 EPUB。 默认值为Auto. |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | 指定是否应使用原始 URL 作为链接图像的 URL。 默认值为`错误的`. |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | 指定页边距是否导出为 HTML、MHTML 或 EPUB。 默认为`错误的`. |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | 指定是否将页面设置导出为 HTML、MHTML 或 EPUB。 默认为`错误的`. |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | 指定保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。 默认为`错误的`. |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | 指定保存为 HTML、MHTML 或 EPUB 时是否写入往返信息。 默认值为`真的`对于 HTML 和`错误的`适用于 MHTML 和 EPUB。 |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | 控制是否[`Shape`](../../aspose.words.drawing/shape/)将 保存为 HTML、MHTML、EPUB 或 AZW3 时，节点将转换为 SVG 图像。 默认值为`错误的`. |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | 控制如何将文本输入表单字段保存为 HTML 或 MHTML。 默认值为`错误的`. |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | 指定保存 HTML、MHTML 和 EPUB 时是否将页码写入目录。 默认值为`错误的`. |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | 指定保存为 HTML 或 MHTML 时是否写入 DOCTYPE 声明。 当`真的`，在文档中的根元素之前写入 DOCTYPE 声明。 默认值为`错误的`. 保存到 EPUB 或 HTML5 时（Html5 ) 始终写入 DOCTYPE 声明。 |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | 控制保存到 HTML、MHTML 或 EPUB 时哪些字体资源需要子集化。 默认为`0`. |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | 允许控制将文档保存为 HTML、MHTML 或 EPUB 时如何保存字体。 |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | 指定将文档导出为 HTML 时保存字体的物理文件夹。 默认为空字符串。 |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | 指定用于构建写入 HTML 文档的字体 URI 的文件夹名称。 默认为空字符串。 |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | 指定将文档保存为 HTML 或 MHTML 时应使用的 HTML 标准版本。 默认值为Xhtml. |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | 指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。 默认为`96 dpi`. |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | 允许控制将文档保存为 HTML、MHTML 或 EPUB 时图像的保存方式。 |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | 指定将文档导出为 HTML 格式时保存图像的物理文件夹。 默认为空字符串。 |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | 指定用于构建写入 HTML 文档的图像 URI 的文件夹名称。 默认为空字符串。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现墨迹 (InkML) 对象。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定在保存文档之前是否应执行内存优化的值。 此属性的默认值为`错误的`. |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | 指定导出为 HTML、MHTML 或 EPUB 时保存图元文件的格式。 默认值为Png，这意味着图元文件被渲染为光栅 PNG 图像。 |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | 指定导出为 EPUB、MOBI 或 AZW3 格式时填充到导航地图的标题的最大级别。默认值为`3`. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | 控制如何将 OfficeMath 对象导出为 HTML、MHTML 或 EPUB。 默认值为Image. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的`，在适用的情况下漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | 指定是否根据 解析和替换文档中使用的字体系列名称[`FontSettings`](../../aspose.words/document/fontsettings/)当写入基于 HTML 的格式时。 |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | 指定一个物理文件夹，当 document 导出为 HTML 时，所有资源（如图像、字体和外部 CSS）都保存在其中。默认为空字符串。 |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | 指定用于构建写入 HTML 文档的所有资源的 URI 的文件夹名称。 默认为空字符串。 |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | 指定使用此保存选项对象时保存文档的格式。 可以Html,Mhtml,Epub, Azw3或者Mobi. |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | 指定在导出为 HTML、MHTML 或 EPUB 时，Aspose.Words 是否将图像缩放至边界形状大小。 默认值为`真的`. |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | 控制如何将表格、行和单元格宽度导出为 HTML、MHTML 或 EPUB。 默认值为All. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且没有使用临时文件。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存前更新。 默认值为`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定是否[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |

## 例子

显示如何在保存到 .html 后指定用于存储链接图像的文件夹。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// 设置一个选项，将表单字段导出为纯文本而不是 HTML 输入元素。
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

演示将文档保存为 .epub 时如何使用特定编码。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 使用 SaveOptions 对象指定我们将保存的文档的编码。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// 默认情况下，输出 .epub 文档的所有内容都位于一个 HTML 部分中。
// 分割标准允许我们将文档分割成几个 HTML 部分。
// 我们将设置将文档拆分为标题段落的标准。
// 这对于无法读取大于特定大小的 HTML 文件的读者很有用。
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// 指定我们要导出文档属性。
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

演示如何将文档拆分为多个部分并保存它们。

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档转换为 HTML 的方式。
    HtmlSaveOptions options = new HtmlSaveOptions();

    // 如果我们正常保存文档，将会有一个输出 HTML
    // 包含所有源文档内容的文档。
    // 将“DocumentSplitCriteria”属性设置为“DocumentSplitCriteria.SectionBreak”
    // 将我们的文档保存到多个 HTML 文件：每个部分一个。
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // 将自定义回调分配给“DocumentPartSavingCallback”属性以更改文档部分保存逻辑。
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // 如果我们将包含图像的文档转换为 html，我们最终会得到一个链接到多个图像的 html 文件。
    // 每个图像将以文件的形式存在于本地文件系统中。
    // 还有一个回调可以自定义每个图像的名称和文件系统位置。
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// 设置保存操作将文档分割成的输出文档的自定义文件名。
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // 我们可以通过“Document”属性访问整个源文档。
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // 以下是指定 Aspose.Words 保存文档各部分的位置的两种方法。
        // 1 - 设置输出零件文件的文件名：
        args.DocumentPartFileName = partFileName;

        // 2 - 为输出零件文件创建自定义流：
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// 为 HTML 转换创建的图像文件设置自定义文件名。
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

        // 以下是指定 Aspose.Words 保存文档各部分的位置的两种方法。
        // 1 - 设置输出图像文件的文件名：
        args.ImageFileName = imageFileName;

        // 2 - 为输出图像文件创建自定义流：
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

* class [SaveOptions](../saveoptions/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
