---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words для .NET
description: Aspose.Words.Rendering.AsposeWordsPrintDocument сорт. Предоставляет реализацию по умолчанию для печатиDocument внутри среды печати .NET на С#.
type: docs
weight: 4530
url: /ru/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Предоставляет реализацию по умолчанию для печати[`Document`](../../aspose.words/document/) внутри среды печати .NET.

Чтобы узнать больше, посетите[Печать документа программно или с использованием диалоговых окон](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) статья документации.

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
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Получает или задает способ печати нецветных страниц, если устройство поддерживает цветную печать. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Получает количество страниц, напечатанных в цвете (т. е. сColor установлено значение true). |

## Методы

| Имя | Описание |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Считывает и кэширует некоторые поляPrinterSettings для сокращения времени печати. |

## Примечания

`AsposeWordsPrintDocument` переопределяетPrintEventArgs) для печати диапазона страниц, указанного вPrinterSettings.

Один документ Word может состоять из нескольких разделов, в которых указаны страницы разных размеров, ориентации и лотков для бумаги.`AsposeWordsPrintDocument` overrides QueryPageSettingsEventArgs) чтобы правильно выбрать размер бумаги, ориентацию и источник бумаги при печати документа Word.

Microsoft Word хранит специфичные для принтера значения для лотков для бумаги в документе Word, поэтому печать только на той модели принтера, которая была выбрана, когда пользователь указал лотки для бумаги , приведет к печати из правильных лотков. Если вы распечатываете документ на другом принтере, то скорее всего будет использоваться лоток для бумаги по умолчанию, а не лотки, указанные в документе.

### Смотрите также

* пространство имен [Aspose.Words.Rendering](../../aspose.words.rendering/)
* сборка [Aspose.Words](../../)
