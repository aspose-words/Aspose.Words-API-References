---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words для .NET
description: Оптимизируйте печать документов с помощью Aspose.Words.Rendering. Наш класс AsposeWordsPrintDocument обеспечивает бесшовную интеграцию для приложений .NET.
type: docs
weight: 5260
url: /ru/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Предоставляет реализацию по умолчанию для печати[`Document`](../../aspose.words/document/)within фреймворк печати .NET.

Чтобы узнать больше, посетите[Печать документа программным способом или с использованием диалогов](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) документальная статья.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Инициализирует новый экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Возвращает или задает способ печати нецветных страниц, если устройство поддерживает цветную печать. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Получает количество страниц, напечатанных в цвете (т.е. сColor установлено значение true). |

## Методы

| Имя | Описание |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Читает и кэширует некоторые поляPrinterSettings для сокращения времени печати. |

## Примечания

`AsposeWordsPrintDocument` переопределяетPrintEventArgs) для печати диапазона страниц, указанного вPrinterSettings.

Один документ Word может состоять из нескольких разделов, в которых указаны страницы разных размеров, ориентации и лотки для бумаги.`AsposeWordsPrintDocument` переопределения QueryPageSettingsEventArgs) для правильного выбора размера бумаги, ориентации и источника бумаги при печати документа Word.

Microsoft Word сохраняет специфические для принтера значения для лотков для бумаги в документе Word, и поэтому только печать на той же модели принтера, которая была выбрана, когда пользователь указал лотки для бумаги приведет к печати из правильных лотков. Если вы печатаете документ на другом принтере, то, скорее всего будет использоваться лоток для бумаги по умолчанию, а не лотки, указанные в документе.

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
