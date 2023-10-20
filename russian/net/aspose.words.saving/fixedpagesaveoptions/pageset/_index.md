---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words для .NET
description: FixedPageSaveOptions PageSet свойство. Получает или задает страницы для рендеринга. По умолчанию  все страницы в документе на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

Получает или задает страницы для рендеринга. По умолчанию — все страницы в документе.

```csharp
public PageSet PageSet { get; set; }
```

## Примеры

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

Показывает, как преобразовать в PDF только некоторые страницы документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
    // чтобы изменить способ преобразования этого метода в .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // Установите для «PageIndex» значение «1», чтобы отобразить часть документа, начиная со второй страницы.
    options.PageSet = new PageSet(1);

    // Этот документ будет содержать одну страницу, начиная со второй страницы, которая будет содержать только вторую страницу.
    doc.Save(stream, options);
}
```

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

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ниже приведены три свойства PageSet, которые мы можем использовать для фильтрации набора страниц из
// наш документ для сохранения в выходном PDF-документе на основе четности номеров страниц.
// 1 - Сохраняем только четные страницы:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - Сохраняем только нечетные страницы:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - Сохраняем каждую страницу:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### Смотрите также

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
