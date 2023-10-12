---
title: PageSet.PageSet
second_title: Справочник по API Aspose.Words для .NET
description: PageSet строитель. Создает одностраничный набор на основе точного индекса страниц.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/pageset/pageset/
---
## PageSet(int) {#constructor_1}

Создает одностраничный набор на основе точного индекса страниц.

```csharp
public PageSet(int page)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| page | Int32 | Индекс страницы, начинающийся с нуля. |

### Примечания

Если встречается страница, которой нет в документе, во время рендеринга будет выдано исключение. MaxValue означает последнюю страницу документа.

### Смотрите также

* class [PageSet](../)
* пространство имен [Aspose.Words.Saving](../../pageset/)
* сборка [Aspose.Words](../../../)

---

## PageSet(params int[]) {#constructor_2}

Создает набор страниц на основе точных индексов страниц.

```csharp
public PageSet(params int[] pages)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pages | Int32[] | Индексы страниц начинаются с нуля. |

### Примечания

Если встречается страница, которой нет в документе, во время рендеринга будет выдано исключение. MaxValue означает последнюю страницу документа.

### Примеры

Показывает, как извлекать страницы на основе точных индексов страниц.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем пять страниц в документ.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Создаем объект «XpsSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в документ .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Используйте свойство «PageSet», чтобы выбрать набор страниц документа для сохранения в формате XPS.
// В этом случае мы выберем с помощью индекса, начинающегося с нуля, только три страницы: страницу 1, страницу 2 и страницу 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Смотрите также

* class [PageSet](../)
* пространство имен [Aspose.Words.Saving](../../pageset/)
* сборка [Aspose.Words](../../../)

---

## PageSet(params PageRange[]) {#constructor}

Создает набор страниц на основе диапазонов.

```csharp
public PageSet(params PageRange[] ranges)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| ranges | PageRange[] | Массив диапазонов страниц. |

### Примечания

Если обнаружен диапазон, который начинается после последней страницы документа, во время рендеринга будет выдано исключение. Все диапазоны, заканчивающиеся после последней страницы, усекаются, чтобы соответствовать размеру документа.

### Примеры

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
* пространство имен [Aspose.Words.Saving](../../pageset/)
* сборка [Aspose.Words](../../../)


