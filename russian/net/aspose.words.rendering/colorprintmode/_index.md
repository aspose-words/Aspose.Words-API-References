---
title: ColorPrintMode Enum
linktitle: ColorPrintMode
articleTitle: ColorPrintMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Rendering.ColorPrintMode для оптимизированной цветной печати. Управляйте печатью нецветных страниц для повышения качества документа.
type: docs
weight: 5270
url: /ru/net/aspose.words.rendering/colorprintmode/
---
## ColorPrintMode enumeration

Указывает, как будут печататься нецветные страницы, если устройство поддерживает цветную печать.

```csharp
public enum ColorPrintMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Normal | `0` | Все страницы печатаются в соответствии с возможностями и настройками принтера. |
| GrayscaleAuto | `1` | Нецветные страницы, если они обнаружены, печатаются в оттенках серого. |

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

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)
