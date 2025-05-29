---
title: AsposeWordsPrintDocument.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words for .NET
description: 了解如何使用 AsposeWordsPrintDocument 的 ColorMode 属性优化打印。控制非彩色页面输出，增强彩色打印效果！
type: docs
weight: 20
url: /zh/net/aspose.words.rendering/asposewordsprintdocument/colormode/
---
## AsposeWordsPrintDocument.ColorMode property

如果设备支持彩色打印，则获取或设置如何打印非彩色页面。

```csharp
public ColorPrintMode ColorMode { get; set; }
```

## 评论

不影响小册子打印。

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

* enum [ColorPrintMode](../../colorprintmode/)
* class [AsposeWordsPrintDocument](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
