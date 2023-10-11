---
title: AsposeWordsPrintDocument.CachePrinterSettings
second_title: Справочник по API Aspose.Words для .NET
description: AsposeWordsPrintDocument метод. Считывает и кэширует некоторые поляPrinterSettings для сокращения времени печати.
type: docs
weight: 40
url: /ru/net/aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/
---
## AsposeWordsPrintDocument.CachePrinterSettings method

Считывает и кэширует некоторые поляPrinterSettings для сокращения времени печати.

```csharp
public void CachePrinterSettings()
```

### Примечания

Этот метод вызывается перед началом печати, если он не выполнялся ранее.

### Примеры

Показывает, как выбрать диапазон страниц и принтер для печати документа, а затем вызвать предварительный просмотр печати.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Вызовите метод «Show», чтобы форма предварительного просмотра отображалась сверху.
previewDlg.Show();

// Инициализируем диалоговое окно печати, указав количество страниц в документе.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Создаем реализацию Aspose.Words документа печати .NET,
// а затем передаем настройки принтера из диалогового окна.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Указываем новый режим цветной печати.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Используйте метод «CachePrinterSettings», чтобы сократить время первого вызова метода «Печать».
awPrintDoc.CachePrinterSettings();

// Вызовите методы «Hide», а затем «InvalidatePreview», чтобы предварительный просмотр печати отображался сверху.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Передаем документ для печати Aspose.Words в диалоговое окно предварительного просмотра печати .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Смотрите также

* class [AsposeWordsPrintDocument](../)
* пространство имен [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* сборка [Aspose.Words](../../../)


