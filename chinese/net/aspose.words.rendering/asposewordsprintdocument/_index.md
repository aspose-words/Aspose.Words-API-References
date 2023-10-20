---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Rendering.AsposeWordsPrintDocument 班级. 为打印Documentinside .NET 打印框架 在 C#.
type: docs
weight: 4530
url: /zh/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

为打印[`Document`](../../aspose.words/document/)inside .NET 打印框架。

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | 初始化这个类的一个新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } |  |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } |  |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | 读取并缓存PrinterSettings 以减少打印时间。 |

## 评论

`AsposeWordsPrintDocument`覆盖PrintEventArgs) 打印指定的页面范围PrinterSettings.

一个 Word 文档可以由多个部分组成，这些部分指定具有不同大小、 方向和纸盘的页面。`AsposeWordsPrintDocument`覆盖 QueryPageSettingsEventArgs)在打印 Word 文档时正确选择纸张尺寸、orientation 和纸张来源。

Microsoft Word 将纸盘的打印机特定值存储在 Word 文档中，因此， 仅在与用户指定纸盘时选择的打印机型号相同的打印机型号上打印 将导致从正确的纸盘打印。如果您在不同的打印机上打印文档，则很可能 将使用默认纸盘，而不是文档中指定的纸盘。

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
