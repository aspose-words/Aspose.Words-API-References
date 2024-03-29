---
title: AsposeWordsPrintDocument
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words для .NET
description: AsposeWordsPrintDocument строитель. Инициализирует новый экземпляр этого класса на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.rendering/asposewordsprintdocument/asposewordsprintdocument/
---
## AsposeWordsPrintDocument constructor

Инициализирует новый экземпляр этого класса.

```csharp
public AsposeWordsPrintDocument(Document document)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| document | Document | Документ для печати. |

## Примеры

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

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
