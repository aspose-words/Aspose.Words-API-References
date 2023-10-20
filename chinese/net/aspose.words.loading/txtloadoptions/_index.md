---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Loading.TxtLoadOptions 班级. 允许在加载时指定附加选项Text文档成Document对象 在 C#.
type: docs
weight: 3730
url: /zh/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

允许在加载时指定附加选项Text文档成[`Document`](../../aspose.words/document/)对象.

要了解更多信息，请访问[指定加载选项](https://docs.aspose.com/words/net/specify-load-options/)文档文章。

```csharp
public class TxtLoadOptions : LoadOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | 使用默认值初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | 获取或设置一个布尔值，指示加载文档时是否执行自动编号检测 。 默认值为`真的`. |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | 获取或设置用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 可以`无效的`或空字符串。默认为`无效的`. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | 获取或设置是否转换元文件（Wmf或者Emf ) 图像到Png图像格式. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | 获取或设置是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | 允许指定从纯文本格式导入文档时如何识别编号列表项。 默认值为`真的`。 |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | 获取或设置文档方向。 默认值为LeftToRight. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | 获取或设置将用于加载 HTML、TXT 或 CHM 文档的编码（如果未指定编码） 在文档内部。 可以`无效的`。默认为`无效的`. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | 允许指定文档字体设置。 |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | 指定是否忽略 OLE 数据。 |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | 获取加载文档时将使用的语言首选项。 |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | 获取或设置前导空格处理的首选选项。 默认值为ConvertToIndent. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | 指定要加载的文档的格式。 默认为Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | 允许指定文档加载过程应与特定的 MS Word 版本匹配。 默认值为Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | 获取或设置打开加密文档的密码。 可以`无效的`或空字符串。默认为`无效的`. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | 获取或设置读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | 在加载文档期间调用并接受有关加载进度的数据。 |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | 允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。 |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | 允许在读取文档时使用临时文件。 默认情况下此属性为`无效的`并且没有使用临时文件。 |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | 获取或设置尾随空格处理的首选选项。 默认值为Trim. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | 指定是否更新字段`肮脏的`属性. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | 在加载操作期间检测到可能导致数据或格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) |  |

### 也可以看看

* class [LoadOptions](../loadoptions/)
* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
