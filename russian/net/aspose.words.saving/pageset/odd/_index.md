---
title: PageSet.Odd
linktitle: Odd
articleTitle: Odd
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSet Odd, которое позволит легко извлекать все нечетные страницы документа в их исходном порядке для эффективного управления документами.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/pageset/odd/
---
## PageSet.Odd property

Получает набор со всеми нечетными страницами документа в их исходном порядке.

```csharp
public static PageSet Odd { get; }
```

## Примечания

Нечетные страницы имеют четные индексы, поскольку индексы страниц начинаются с нуля.

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
