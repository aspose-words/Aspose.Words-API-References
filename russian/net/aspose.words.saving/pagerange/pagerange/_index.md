---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words для .NET
description: PageRange строитель. Создает новый объект диапазона страниц на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Создает новый объект диапазона страниц.

```csharp
public PageRange(int from, int to)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| from | Int32 | Индекс начальной страницы, отсчитываемый от нуля. |
| to | Int32 | Индекс конечной страницы, отсчитываемый от нуля. Если он превышает индекс последней страницы документа, он усекается, чтобы поместиться в документе при рендеринге. |

## Примечания

MaxValue означает последнюю страницу документа.

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

* class [PageRange](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
