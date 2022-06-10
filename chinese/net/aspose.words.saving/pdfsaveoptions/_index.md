---
title: PdfSaveOptions
second_title: Aspose.Words for .NET API 参考
description: 可用于在将文档保存为Pdf格式时指定附加选项
type: docs
weight: 5190
url: /zh/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

可用于在将文档保存为Pdf格式时指定附加选项。

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions)() | 初始化此类的新实例，该实例可用于将文档保存在 Pdf格式。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning) { get; set; } | 指定是否编写附加文本定位操作符的标志。 |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | 获取或设置一个布尔值，指示是否允许在保存文档时嵌入带有 PostScript 轮廓的字体 。 默认值为 **false** 。 |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | 获取或设置一个值，确定如何呈现颜色。 |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance) { get; set; } | 指定输出文档的 PDF 标准合规级别。 |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks) { get; set; } | 指定是否将正文故事中的脚注/尾注引用转换为活动超链接。 当点击超链接时，将指向相应的脚注/尾注。 默认为` false` 。 |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport) { get; set; } | 获取或设置一个值，确定[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties)导出到 PDF 文件的方式。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为 **空字符串** (Empty)。 |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails) { get; set; } | 获取或设置用于签署输出 PDF 文档的详细信息。 |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle) { get; set; } | 一个标志，指定窗口的标题栏是否应显示取自文档信息字典的标题条目 的文档标题。 |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何渲染 3D 效果。 |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions) { get; set; } | 允许指定下采样选项。 |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts) { get; set; } | 控制字体如何嵌入到生成的 PDF 文档中。 |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails) { get; set; } | 获取或设置加密输出 PDF 文档的详细信息。 |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure) { get; set; } | 获取或设置确定是否导出文档结构的值。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | 如果为真，则将 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为 **true** 。 |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag) { get; set; } | 获取或设置一个值，确定是否在文档结构中创建“Span”标签以导出文本语言。 |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | 获取或设置值，确定允许通过[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping)映射哪些文档格式。 默认只允许映射FlatOpc文档格式。 |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode) { get; set; } | 指定字体嵌入模式。 |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode) { get; set; } | 确定如何导出页眉/页脚中的书签。 |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode) { get; set; } | 指定如何为 PDF 文档中的图像选择色彩空间。 |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression) { get; set; } | 指定要用于文档中所有图像的压缩类型。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | 获取或设置一个值，确定如何呈现墨水 (InkML) 对象。 |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages) { get; set; } | 指示图像插值是否应由合格阅读器执行的标志。 当` false` 指定时，标志不会写入输出文档和 reader 的默认行为改为使用。 |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality) { get; set; } | 获取或设置确定 PDF 文档中 JPEG 图像质量的值。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为 **false** 。 |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | 允许指定元文件渲染选项。 |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | 获取或设置[`NumeralFormat`](../numeralformat)用于呈现数字。 默认使用欧洲数字。 |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow) { get; set; } | 获取或设置一个值，确定输出 Pdf 文档 中的超链接是否强制在新窗口（或选项卡）中打开浏览器。 |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Flag 表示是否需要优化输出。 如果设置了这个标志，多余的嵌套画布和空画布被删除， 也会连接具有相同格式的相邻字形。 注意:如果该属性设置为true，可能会影响内容显示的准确性。 默认为假。 |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions) { get; } | 允许指定大纲选项。 |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode) { get; set; } | 指定 PDF 文档在 PDF 阅读器中打开时的显示方式。 |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | 允许控制在将文档导出为固定页面格式时如何保存单独的页面。 |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | 获取或设置要呈现的页面。 默认是文档中的所有页面。 |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages) { get; set; } | 获取或设置一个值，确定是否将透明图像与黑色背景颜色预混合。 |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields) { get; set; } | 指定是否将 Microsoft Word 表单域保留为 PDF 中的表单域或将其转换为文本。 默认为` false` 。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | 当` true` 时，在适用的情况下输出漂亮的格式。 默认值为 **false** 。 |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat) { get; set; } | 如果使用此保存选项对象，则指定保存文档的格式。 只能是Pdf。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | 指定保存到 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为` null` 并且不使用临时文件。 |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression) { get; set; } | 指定用于文档中所有文本内容的压缩类型。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime)属性是否在保存之前更新。 默认值为假； |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为 **true** 。 |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | 获取或设置一个值，该值确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted)属性是否在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | 获取或设置一个值，该值确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime)属性是否在保存前更新。 |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | 获取或设置确定[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag)的内容是否在保存前更新的值。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings) { get; set; } | 获取或设置一个布尔值，指示是否应使用小册子打印布局保存文档，如果是通过:::R5 指定的 :P:Aspose.Words.PageSetup.MultiplePages:::。 |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts) { get; set; } | 获取或设置一个值，确定是否用核心 PDF 类型 1 替换 TrueType 字体 Arial、Times New Roman、 Courier New 和 Symbol字体。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | 获取或设置一个确定是否使用高质量（即慢速）渲染算法的值。 |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior) { get; set; } | 获取或设置一个值，该值确定使用 PDF 查看器打开文档时应应用的缩放类型。 |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor) { get; set; } | 获取或设置确定文档缩放因子（以百分比为单位）的值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone)() | 创建此对象的深层克隆。 |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | 确定指定对象的值是否与当前对象相等。 |

### 例子

显示如何使用保存选项属性更改图像颜色。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入级别 1 到 5 的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是一个目录，列出了文档正文中的标题。
// 单击此大纲中的条目会将我们带到其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“4”，从大纲中排除所有级别高于4的标题。
options.OutlineOptions.HeadingsOutlineLevels = 4;

// 如果一个大纲条目在其自身和下一个相同或更低级别的条目之间有更高级别的后续条目，
// 条目左侧会出现一个箭头。这个条目是几个这样的“子条目”的“所有者”。
// 在我们的文档中，第 5 级标题的大纲条目是第二个 4 级大纲条目的子条目，
 // 第 4 和第 5 级标题条目是第二个 3 级条目的子条目，依此类推。
// 在大纲中，我们可以单击“所有者”条目的箭头来折叠/展开其所有子条目。
// 将“ExpandedOutlineLevels”属性设置为“2”以自动展开所有标题级别 2 和更低的大纲条目
// 并在我们打开文档时折叠所有级别和 3 及更高级别的条目。
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

显示将文档保存为 PDF 时如何应用文本压缩。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入级别 1 到 5 的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是一个目录，列出了文档正文中的标题。
// 单击此大纲中的条目会将我们带到其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“4”，从大纲中排除所有级别高于4的标题。
options.OutlineOptions.HeadingsOutlineLevels = 4;

// 如果一个大纲条目在其自身和下一个相同或更低级别的条目之间有更高级别的后续条目，
// 条目左侧会出现一个箭头。这个条目是几个这样的“子条目”的“所有者”。
// 在我们的文档中，第 5 级标题的大纲条目是第二个 4 级大纲条目的子条目，
 // 第 4 和第 5 级标题条目是第二个 3 级条目的子条目，依此类推。
// 在大纲中，我们可以单击“所有者”条目的箭头来折叠/展开其所有子条目。
// 将“ExpandedOutlineLevels”属性设置为“2”以自动展开所有标题级别 2 和更低的大纲条目
// 并在我们打开文档时折叠所有级别和 3 及更高级别的条目。
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

显示如何将整个文档转换为文档大纲中的三个级别的 PDF。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入级别 1 到 5 的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions options = new PdfSaveOptions();

// 输出的 PDF 文档将包含一个大纲，它是一个目录，列出了文档正文中的标题。
// 单击此大纲中的条目会将我们带到其各自标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“4”，从大纲中排除所有级别高于4的标题。
options.OutlineOptions.HeadingsOutlineLevels = 4;

// 如果一个大纲条目在其自身和下一个相同或更低级别的条目之间有更高级别的后续条目，
// 条目左侧会出现一个箭头。这个条目是几个这样的“子条目”的“所有者”。
// 在我们的文档中，第 5 级标题的大纲条目是第二个 4 级大纲条目的子条目，
 // 第 4 和第 5 级标题条目是第二个 3 级条目的子条目，依此类推。
// 在大纲中，我们可以单击“所有者”条目的箭头来折叠/展开其所有子条目。
// 将“ExpandedOutlineLevels”属性设置为“2”以自动展开所有标题级别 2 和更低的大纲条目
// 并在我们打开文档时折叠所有级别和 3 及更高级别的条目。
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### 也可以看看

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
