---
title: PageSet.Even
linktitle: Even
articleTitle: Even
second_title: Aspose.Words для .NET
description: Извлеките набор всех четных страниц из вашего документа в их исходном порядке с помощью PageSet Even. Оптимизируйте свой рабочий процесс и улучшите управление документами!
type: docs
weight: 30
url: /ru/net/aspose.words.saving/pageset/even/
---
## PageSet.Even property

Получает набор со всеми четными страницами документа в их исходном порядке.

```csharp
public static PageSet Even { get; }
```

## Примечания

Четные страницы имеют нечетные индексы, поскольку индексы страниц начинаются с нуля.

## Примеры

Показывает, как экспортировать нечетные страницы из документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ниже приведены три свойства PageSet, которые мы можем использовать для фильтрации набора страниц из
// наш документ для сохранения в выходном PDF-документе на основе четности номеров страниц.
// 1 — Сохранить только четные страницы:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Сохранить только нечетные страницы:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Сохранить каждую страницу:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Смотрите также

* class [PageSet](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
