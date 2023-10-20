---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Loading.HtmlLoadOptions 班级. 允许在将 HTML 文档加载到Document对象 在 C#.
type: docs
weight: 3620
url: /zh/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

允许在将 HTML 文档加载到[`Document`](../../aspose.words/document/)对象.

要了解更多信息，请访问[指定加载选项](https://docs.aspose.com/words/net/specify-load-options/)文档文章。

```csharp
public class HtmlLoadOptions : LoadOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | 使用默认值初始化此类的新实例。 |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | 使用指定的密码初始化此类的新实例以加载加密文档的快捷方式。 |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | 初始化此类新实例并将属性设置为指定值的快捷方式。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | 获取或设置用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 可以`无效的`或空字符串。默认为`无效的`. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | 获取或设置一个值，该值指定如何导入块级元素的属性。 默认值为Merge. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | 获取或设置是否转换元文件（Wmf或者Emf ) 图像到Png图像格式. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | 获取或设置是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | 获取或设置一个值，该值指示是否将加载的 SVG 图像转换为 EMF 格式。 默认值为`错误的`并且，如果可能，加载的 SVG 图像将按原样存储，无需转换。 |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | 获取或设置将用于加载 HTML、TXT 或 CHM 文档的编码（如果未指定编码） 在文档内部。 可以`无效的`。默认为`无效的`. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | 允许指定文档字体设置。 |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | 获取或设置一个值，该值指示是否忽略 &lt;noscript&gt; HTML 元素。 默认值为`错误的`. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | 指定是否忽略 OLE 数据。 |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | 获取加载文档时将使用的语言首选项。 |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | 指定要加载的文档的格式。 默认为Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | 允许指定文档加载过程应与特定的 MS Word 版本匹配。 默认值为Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | 获取或设置打开加密文档的密码。 可以`无效的`或空字符串。默认为`无效的`. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | 获取或设置表示导入的 &lt;input&gt; 和 &lt;select&gt; 元素的文档节点的首选类型。 默认值为FormField. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | 获取或设置读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | 在加载文档期间调用并接受有关加载进度的数据。 |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | 允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。 |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | 获取或设置一个值，指示是否支持 VML 图像。 |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | 允许在读取文档时使用临时文件。 默认情况下此属性为`无效的`并且没有使用临时文件。 |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | 指定是否更新字段`肮脏的`属性. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | 在加载操作期间检测到可能导致数据或格式保真度损失的问题时调用。 |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Web 请求超时之前等待的毫秒数。默认值为 100000 毫秒 （100 秒）. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) |  |

### 也可以看看

* class [LoadOptions](../loadoptions/)
* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
