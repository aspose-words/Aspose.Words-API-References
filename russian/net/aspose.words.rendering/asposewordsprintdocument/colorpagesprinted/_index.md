---
title: AsposeWordsPrintDocument.ColorPagesPrinted
linktitle: ColorPagesPrinted
articleTitle: ColorPagesPrinted
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Aspose.Words PrintDocument ColorPagesPrinted для эффективного отслеживания количества страниц, напечатанных в ярких цветах. Максимизируйте свои идеи печати!
type: docs
weight: 30
url: /ru/net/aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/
---
## AsposeWordsPrintDocument.ColorPagesPrinted property

Получает количество страниц, напечатанных в цвете (т.е. сColor установлено значение true).

```csharp
public int ColorPagesPrinted { get; }
```

## Примеры

Показывает, как выбрать диапазон страниц и принтер для печати документа, а затем вызвать предварительный просмотр печати.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Вызовите метод «Показать», чтобы отобразить форму предварительного просмотра печати сверху.
previewDlg.Show();

// Инициализируем диалоговое окно печати с указанием количества страниц в документе.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// Создаем реализацию "Aspose.Words" для документа печати .NET,
// а затем передайте настройки принтера из диалогового окна.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Укажите новый режим цветной печати.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// Используйте метод «CachePrinterSettings» для сокращения времени первого вызова метода «Print».
awPrintDoc.CachePrinterSettings();

// Вызовите методы «Hide», а затем «InvalidatePreview», чтобы отобразить предварительный просмотр печати поверх остальных.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// Передаем печатный документ «Aspose.Words» в диалоговое окно предварительного просмотра печати .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Смотрите также

* class [AsposeWordsPrintDocument](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
