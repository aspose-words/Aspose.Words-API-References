---
title: PdfLoadOptions Class
linktitle: PdfLoadOptions
articleTitle: PdfLoadOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.PdfLoadOptions，增强 PDF 加载功能。使用灵活的选项自定义文档转换，以获得最佳效果。
type: docs
weight: 4130
url: /zh/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

允许在将 PDF 文档加载到[`Document`](../../aspose.words/document/)对象.

要了解更多信息，请访问[指定加载选项](https://docs.aspose.com/words/net/specify-load-options/)文档文章。

```csharp
public class PdfLoadOptions : LoadOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [PdfLoadOptions](pdfloadoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | 获取或设置用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 可以`无效的`或空字符串。默认为`无效的`. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | 获取或设置是否转换图元文件（Wmf或者Emf ) 图像到Png图像格式. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | 获取或设置是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | 获取或设置用于加载 HTML、TXT 或 CHM 文档的编码（如果未在文档中指定编码）。 可以是`无效的` 默认为`无效的`. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | 允许指定文档字体设置。 |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | 指定是否忽略 OLE 数据。 |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | 获取文档加载时将使用的语言首选项。 |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | 指定要加载的文档的格式。 默认值为Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | 允许指定文档加载过程应与特定的 MS Word 版本匹配。 默认值为Word2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | 获取或设置要读取的页数。默认值为 MaxValue，表示将读取文档的所有页面。 |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | 获取或设置要读取的第一个页面的从 0 开始的索引。默认值为 0。 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | 获取或设置打开加密文档的密码。 可以是`无效的`或空字符串。默认为`无效的`. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | 获取或设置读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | 在加载文档期间调用并接受有关加载进度的数据。 |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | 允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。 |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | 获取或设置标志，指示加载 PDF 文档时是否必须跳过图像。默认值为`错误的`. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | 允许在读取文档时使用临时文件。 默认情况下，此属性为`无效的`并且不使用临时文件。 |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | 指定是否使用`肮脏的`属性. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | 获取或设置是否使用从 Windows 注册表获取的 LCID 值来确定页面设置默认边距。 |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | 在加载操作期间调用，当检测到可能导致数据或格式保真度损失的问题时。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | 确定指定对象的值是否等于当前对象。 |

## 例子

展示如何在加载 PDF 文件时跳过图像。

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### 也可以看看

* class [LoadOptions](../loadoptions/)
* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
