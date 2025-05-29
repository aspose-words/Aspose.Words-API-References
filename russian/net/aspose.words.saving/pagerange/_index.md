---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.PageRange для простого определения непрерывных диапазонов страниц. Улучшите обработку документов с точностью и эффективностью.
type: docs
weight: 6150
url: /ru/net/aspose.words.saving/pagerange/
---
## PageRange class

Представляет непрерывный диапазон страниц.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public sealed class PageRange
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Создает новый объект диапазона страниц. |

## Примеры

Показывает, как извлекать страницы на основе точных диапазонов страниц.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
