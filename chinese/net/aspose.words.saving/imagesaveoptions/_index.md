---
title: ImageSaveOptions Class
linktitle: ImageSaveOptions
articleTitle: ImageSaveOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.ImageSaveOptions。使用可自定义的选项轻松渲染文档，实现高质量的图像输出。
type: docs
weight: 5980
url: /zh/net/aspose.words.saving/imagesaveoptions/
---
## ImageSaveOptions class

允许在将文档页面或形状渲染为图像时指定其他选项。

要了解更多信息，请访问[指定保存选项](https://docs.aspose.com/words/net/specify-save-options/)文档文章。

```csharp
public class ImageSaveOptions : FixedPageSaveOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ImageSaveOptions](imagesaveoptions/)(*[SaveFormat](../../aspose.words/saveformat/)*) | 初始化此类的新实例，可用于保存渲染图像Tiff，Png，Bmp , Jpeg，Emf，Eps , WebP或者Svg格式. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | 获取或设置一个布尔值，指示在保存文档时嵌入 TrueType 字体时是否允许嵌入带有 PostScript 轮廓的字体 。 默认值为`错误的`. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | 获取或设置确定如何呈现颜色的值。 |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | 获取或设置用于日期/时间字段的自定义本地时区。 |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | 获取或设置默认模板的路径（包括文件名）。 此属性的默认值为**空字符串**(Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 3D 效果。 |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 效果。 |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 DrawingML 形状。 |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | 当`真的` ，导致 Aspose.Words 的名称和版本嵌入到生成的文件中。 默认值为`真的`. |
| [GraphicsQualityOptions](../../aspose.words.saving/imagesaveoptions/graphicsqualityoptions/) { get; set; } | 允许指定渲染模式和质量Graphics对象. |
| [HorizontalResolution](../../aspose.words.saving/imagesaveoptions/horizontalresolution/) { get; set; } | 获取或设置生成图像的水平分辨率（以每英寸点数为单位）。 |
| [ImageBrightness](../../aspose.words.saving/imagesaveoptions/imagebrightness/) { get; set; } | 获取或设置生成图像的亮度。 |
| [ImageColorMode](../../aspose.words.saving/imagesaveoptions/imagecolormode/) { get; set; } | 获取或设置生成图像的颜色模式。 |
| [ImageContrast](../../aspose.words.saving/imagesaveoptions/imagecontrast/) { get; set; } | 获取或设置生成图像的对比度。 |
| [ImageSize](../../aspose.words.saving/imagesaveoptions/imagesize/) { get; set; } | 获取或设置生成的图像的大小（以像素为单位）。 |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | 获取或设置一个值，该值确定如何呈现墨水（InkML）对象。 |
| [JpegQuality](../../aspose.words.saving/imagesaveoptions/jpegquality/) { get; set; } | 获取或设置确定生成的 JPEG 图像质量的值。 |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | 获取或设置确定是否应在保存文档之前执行内存优化的值。 此属性的默认值为`错误的`. |
| [MetafileRenderingOptions](../../aspose.words.saving/imagesaveoptions/metafilerenderingoptions/) { get; } | 允许指定如何在渲染输出中处理元文件。 |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | 获取或设置[`NumeralFormat`](../numeralformat/)用于渲染数字。 默认使用欧洲数字。 |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | 标志指示是否需要优化输出。 如果设置了此标志，则会删除多余的嵌套画布和空画布， 还会连接具有相同格式的相邻字形。 注意：如果将此属性设置为`真的`. 默认为`错误的`. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | 允许控制将文档导出为固定页面格式时如何保存单独的页面。 |
| [PageSet](../../aspose.words.saving/imagesaveoptions/pageset/) { get; set; } | 获取或设置要呈现的页面。 默认为文档中的所有页面。 |
| [PaperColor](../../aspose.words.saving/imagesaveoptions/papercolor/) { get; set; } | 获取或设置生成图像的背景（纸张）颜色。 |
| [PixelFormat](../../aspose.words.saving/imagesaveoptions/pixelformat/) { get; set; } | 获取或设置生成图像的像素格式。 |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | 当`真的` ，在适用的情况下以漂亮的格式输出。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | 在保存文档期间调用并接受有关保存进度的数据。 |
| [Resolution](../../aspose.words.saving/imagesaveoptions/resolution/) { set; } | 设置生成图像的水平和垂直分辨率，以每英寸点数为单位。 |
| override [SaveFormat](../../aspose.words.saving/imagesaveoptions/saveformat/) { get; set; } | 如果使用此保存选项对象，则指定渲染的文档页面或形状的保存格式。 可以是光栅 Tiff，Png，Bmp , Jpeg或向量Emf，Eps , WebP，Svg. |
| [Scale](../../aspose.words.saving/imagesaveoptions/scale/) { get; set; } | 获取或设置生成图像的缩放系数。 |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | 指定保存为 DOC 或 DOCX 文件时使用的临时文件的文件夹。 默认情况下，此属性为`无效的`并且不使用临时文件。 |
| [ThresholdForFloydSteinbergDithering](../../aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/) { get; set; } | 获取或设置确定 Floyd-Steinberg 方法中的二值化误差值的阈值。 当[`ImageBinarizationMethod`](../imagebinarizationmethod/)是FloydSteinbergDithering. |
| [TiffBinarizationMethod](../../aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/) { get; set; } | 获取或设置将图像转换为 1 bpp 格式时使用的方法 [`SaveFormat`](./saveformat/)是Tiffand [`TiffCompression`](./tiffcompression/)等于Ccitt3或者Ccitt4. |
| [TiffCompression](../../aspose.words.saving/imagesaveoptions/tiffcompression/) { get; set; } | 获取或设置在将生成的图像保存为 TIFF 格式时应用的压缩类型。 |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | 确定字体属性是否根据所使用的字符代码进行更改。 |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/)属性在保存之前更新。 默认值是`错误的`; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | 获取或设置一个值，该值确定在将文档保存为固定页面格式之前是否应更新某些类型的字段。 此属性的默认值为`真的`. |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | 获取或设置一个值，确定[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/)属性在保存之前更新。 |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | 获取或设置一个值，确定[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/)属性在保存之前更新。 |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | 获取或设置一个值，确定是否使用抗锯齿进行渲染。 |
| [UseGdiEmfRenderer](../../aspose.words.saving/imagesaveoptions/usegdiemfrenderer/) { get; set; } | 获取或设置一个值，确定保存到 EMF 时是否使用 GDI+ 或 Aspose.Words 图元文件渲染器。 |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | 获取或设置一个值，确定是否使用高质量（即慢速）渲染算法。 |
| [VerticalResolution](../../aspose.words.saving/imagesaveoptions/verticalresolution/) { get; set; } | 获取或设置生成图像的垂直分辨率（以每英寸点数为单位）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.saving/imagesaveoptions/clone/)() | 创建此对象的深度克隆。 |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | 确定指定对象的值是否等于当前对象。 |

## 例子

展示如何在将文档渲染为 PNG 时指定分辨率。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);

// 将“分辨率”属性设置为“72”以 72dpi 呈现文档。
options.Resolution = 72;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.72dpi.png", options);

// 将“分辨率”属性设置为“300”以 300dpi 呈现文档。
options.Resolution = 300;
doc.Save(ArtifactsDir + "ImageSaveOptions.Resolution.300dpi.png", options);
```

展示如何在将文档保存为 JPEG 时配置压缩。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Jpeg);
// 将“JpegQuality”属性设置为“10”以在呈现文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像将显示更明显的压缩伪影。
imageOptions.JpegQuality = 10;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// 将“JpegQuality”属性设置为“100”以在渲染文档时使用较弱的压缩。
// 这将提高图像的质量，但会增加文件大小。
imageOptions.JpegQuality = 100;
doc.Save(ArtifactsDir + "ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

将 Word 文档的一页呈现为具有透明或彩色背景的图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Times New Roman";
builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertImage(ImageDir + "Logo.jpg");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions imgOptions = new ImageSaveOptions(SaveFormat.Png);
// 将“PaperColor”属性设置为透明颜色以应用透明
// 在将其渲染为图像时将其背景添加到文档中。
imgOptions.PaperColor = Color.Transparent;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// 将“PaperColor”属性设置为不透明颜色以应用该颜色
// 作为文档的背景，我们将其渲染为图像。
imgOptions.PaperColor = Color.LightCoral;

doc.Save(ArtifactsDir + "ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

### 也可以看看

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
