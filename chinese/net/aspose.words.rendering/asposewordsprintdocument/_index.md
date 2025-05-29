---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.Rendering 简化文档打印。我们的 AsposeWordsPrintDocument 类可与 .NET 应用程序无缝集成。
type: docs
weight: 5260
url: /zh/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

提供打印的默认实现[`Document`](../../aspose.words/document/)在 .NET 打印框架内。

要了解更多信息，请访问[通过编程或对话框打印文档](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/)文档文章。

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
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | 如果设备支持彩色打印，则获取或设置如何打印非彩色页面。 |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | 获取彩色打印的页数（即Color设置为 true)。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | 读取并缓存PrinterSettings 以减少打印时间。 |

## 评论

`AsposeWordsPrintDocument`覆盖PrintEventArgs) 打印指定的页面范围PrinterSettings。

单个 Word 文档可以由多个部分组成，这些部分指定具有不同大小、方向和纸盘的页面。`AsposeWordsPrintDocument`覆盖 QueryPageSettingsEventArgs)在打印 Word 文档时正确选择纸张尺寸、orientation 和纸张来源。

Microsoft Word 会在 Word 文档中存储打印机特定的纸盘值，因此，只有在用户指定纸盘时所选的打印机型号相同的情况下，才会从正确的纸盘打印。如果您在其他打印机上打印文档，则很可能使用默认纸盘，而不是文档中指定的纸盘。

## 例子

显示如何选择页面范围和打印机来打印文档，然后调出打印预览。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// 调用“Show”方法让打印预览表单显示在顶部。
previewDlg.Show();

// 使用文档中的页数初始化打印对话框。
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// 创建.NET打印文档的“Aspose.Words”实现，
// 然后从对话框中传递打印机设置。
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// 指定新的彩色打印模式。
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// 使用“CachePrinterSettings”方法来减少第一次调用“Print”方法的时间。
awPrintDoc.CachePrinterSettings();

// 调用“Hide”，然后调用“InvalidatePreview”方法以使打印预览显示在顶部。
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// 将“Aspose.Words”打印文档传递到.NET 打印预览对话框。
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### 也可以看看

* 命名空间 [Aspose.Words.Rendering](../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../)
