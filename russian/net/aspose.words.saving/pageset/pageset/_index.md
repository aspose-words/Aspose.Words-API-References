---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words для .NET
description: Создавайте индивидуальные одностраничные наборы без особых усилий с помощью конструктора PageSet, разработанного для точной индексации страниц и удобного взаимодействия с пользователем.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Создает одностраничный набор на основе точного индекса страницы.

```csharp
public PageSet(int page)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| page | Int32 | Индекс страницы, отсчитываемый от нуля. |

## Примечания

Если обнаружена страница, которой нет в документе, во время рендеринга будет выдано исключение. MaxValue означает последнюю страницу в документе.

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

* class [PageSet](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Создает набор страниц на основе точных индексов страниц.

```csharp
public PageSet(params int[] pages)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pages | Int32[] | Индексы страниц начинаются с нуля. |

## Примечания

Если обнаружена страница, которой нет в документе, во время рендеринга будет выдано исключение. MaxValue означает последнюю страницу в документе.

## Примеры

Показывает, как извлекать страницы на основе точных индексов страниц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавить пять страниц в документ.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Создаем объект "XpsSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Используйте свойство «PageSet», чтобы выбрать набор страниц документа для сохранения в выходном XPS-файле.
// В этом случае мы выберем с помощью индекса, начинающегося с нуля, только три страницы: страницу 1, страницу 2 и страницу 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Смотрите также

* class [PageSet](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Создает набор страниц на основе диапазонов.

```csharp
public PageSet(params PageRange[] ranges)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| ranges | PageRange[] | Массив диапазонов страниц. |

## Примечания

Если обнаружен диапазон, начинающийся после последней страницы в документе, во время рендеринга будет сгенерировано исключение. Все диапазоны, заканчивающиеся после последней страницы, обрезаются, чтобы поместиться в документе.

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
