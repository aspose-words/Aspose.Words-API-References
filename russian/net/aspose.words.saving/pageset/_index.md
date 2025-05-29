---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.PageSet для эффективного управления документами. Легко определяйте случайные наборы страниц и улучшайте свой рабочий процесс уже сегодня!
type: docs
weight: 6170
url: /ru/net/aspose.words.saving/pageset/
---
## PageSet class

Описывает случайный набор страниц.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Создает одностраничный набор на основе точного индекса страницы. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Создает набор страниц на основе точных индексов страниц. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Создает набор страниц на основе диапазонов. |

## Характеристики

| Имя | Описание |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Получает набор со всеми страницами документа в их исходном порядке. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Получает набор со всеми четными страницами документа в их исходном порядке. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Получает набор со всеми нечетными страницами документа в их исходном порядке. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Примеры

Показывает, как преобразовать одну страницу документа в изображение JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Создаем объект "ImageSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ, которым этот метод преобразует документ в изображение.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Установите "PageSet" на "1", чтобы выбрать вторую страницу через
// индекс (начиная с нуля), с которого начинается рендеринг документа.
options.PageSet = new PageSet(1);

// Когда мы сохраняем документ в формате JPEG, Aspose.Words отображает только одну страницу.
// Это изображение будет содержать одну страницу, начиная со второй страницы,
// которая будет просто второй страницей исходного документа.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
