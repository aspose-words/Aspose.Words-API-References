---
title: TxtLoadOptions Class
linktitle: TxtLoadOptions
articleTitle: TxtLoadOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TxtLoadOptions，增强文本文档加载功能。使用灵活的选项自定义您的 Document 对象，以获得最佳性能。
type: docs
weight: 4190
url: /zh/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

允许在加载时指定附加选项Text文档变成[`Document`](../../aspose.words/document/)对象.

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
| [AutoNumberingDetection](../../aspose.words.loading/txtloadoptions/autonumberingdetection/) { get; set; } | 获取或设置一个布尔值，指示在加载文档时是否执行自动编号检测。 默认值为`真的`. |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | 获取或设置用于在需要时将文档中找到的相对 URI 解析为绝对 URI 的字符串。 可以`无效的`或空字符串。默认为`无效的`. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | 获取或设置是否转换图元文件（Wmf或者Emf ) 图像到Png图像格式. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | 获取或设置是否将带有 EquationXML 的形状转换为 Office Math 对象。 |
| [DetectHyperlinks](../../aspose.words.loading/txtloadoptions/detecthyperlinks/) { get; set; } | 指定检测文本中的超链接。 默认值为`错误的`. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | 允许指定从纯文本格式导入文档时如何识别编号列表项。 默认值为`真的`。 |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | 获取或设置文档方向。 默认值为LeftToRight. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | 获取或设置用于加载 HTML、TXT 或 CHM 文档的编码（如果未在文档中指定编码）。 可以是`无效的` 默认为`无效的`. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | 允许指定文档字体设置。 |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | 指定是否忽略 OLE 数据。 |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | 获取文档加载时将使用的语言首选项。 |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | 获取或设置前导空格处理的首选选项。 默认值为ConvertToIndent. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | 指定要加载的文档的格式。 默认值为Auto. |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | 允许指定文档加载过程应与特定的 MS Word 版本匹配。 默认值为Word2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | 获取或设置打开加密文档的密码。 可以是`无效的`或空字符串。默认为`无效的`. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | 获取或设置读取 Microsoft Word 格式时是否保留 INCLUDEPICTURE 字段。 默认值为`错误的`. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | 在加载文档期间调用并接受有关加载进度的数据。 |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | 允许控制从 HTML、MHTML 导入文档时如何加载外部资源（图像、样式表）。 |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | 允许在读取文档时使用临时文件。 默认情况下，此属性为`无效的`并且不使用临时文件。 |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | 获取或设置尾随空格处理的首选选项。 默认值为Trim. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | 指定是否使用`肮脏的`属性. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | 获取或设置是否使用从 Windows 注册表获取的 LCID 值来确定页面设置默认边距。 |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | 在加载操作期间调用，当检测到可能导致数据或格式保真度损失的问题时。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | 确定指定对象的值是否等于当前对象。 |

## 例子

展示如何读取和显示超链接。

```csharp
const string inputText = "Some links in TXT:\n" +
        "https://www.aspose.com/\n" +
        "https://docs.aspose.com/words/net/\n”；

using (Stream stream = new MemoryStream())
{
    byte[] buf = Encoding.ASCII.GetBytes(inputText);
    stream.Write(buf, 0, buf.Length);

    // 加载带有超链接的文档。
    Document doc = new Document(stream, new TxtLoadOptions() { DetectHyperlinks = true });

    // 打印超链接文本。
    foreach (Field field in doc.Range.Fields)
        Console.WriteLine(field.Result);

    Assert.AreEqual(doc.Range.Fields[0].Result.Trim(), "https://www.aspose.com/”);
    Assert.AreEqual(doc.Range.Fields[1].Result.Trim(), "https://docs.aspose.com/words/net/”);
}
```

### 也可以看看

* class [LoadOptions](../loadoptions/)
* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
