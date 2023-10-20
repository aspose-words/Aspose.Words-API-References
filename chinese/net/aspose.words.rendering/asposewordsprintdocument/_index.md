---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Rendering.AsposeWordsPrintDocument 班级. 提供打印的默认实现Document在 .NET 打印框架内 在 C#.
type: docs
weight: 4530
url: /zh/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

提供打印的默认实现[`Document`](../../aspose.words/document/)在 .NET 打印框架内。

要了解更多信息，请访问[以编程方式或使用对话框打印文档](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/)文档文章。

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | 获取或设置如果设备支持彩色打印，如何打印非彩色页面。 |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | 获取彩色打印的页数（即带有Color设置为 true). |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | 读取并缓存一些字段PrinterSettings 减少打印时间。 |

## 评论

`AsposeWordsPrintDocument`覆盖PrintEventArgs) 打印指定的页面范围PrinterSettings。

单个 Word 文档可以由多个部分组成，这些部分指定不同尺寸、 方向和纸盘的页面。`AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs)打印 Word 文档时正确选择纸张尺寸、方向 和纸张来源。

Microsoft Word 在 Word 文档中存储纸盘的打印机特定值，因此， 仅在与用户指定纸盘 时选择的打印机型号相同的打印机型号上进行打印，才会从正确的纸盘进行打印。如果您在不同的打印机上打印文档，则很可能 将使用默认纸盘，而不是文档中指定的纸盘。

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
