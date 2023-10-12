---
title: Class PageSavingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.PageSavingArgs сорт. Предоставляет данные дляPageSaving событие.
type: docs
weight: 5380
url: /ru/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Предоставляет данные для[`PageSaving`](../ipagesavingcallback/pagesaving/) событие.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public class PageSavingArgs
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Указывает, должен ли Aspose.Words сохранять поток открытым или закрывать его после сохранения страницы документа. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Получает или задает имя файла, в котором будет сохранена страница документа. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Индекс текущей страницы. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Позволяет указать поток, в котором будет сохранена страница документа. |

### Примеры

Показывает, как использовать обратный вызов для сохранения документа в формате HTML постранично.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Создаем объект HtmlFixedSaveOptions, который мы можем передать методу Save документа.
    // чтобы изменить способ преобразования документа в HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Мы сохраним каждую страницу этого документа в отдельный HTML-файл в локальной файловой системе.
    // Устанавливаем обратный вызов, который позволяет нам присваивать имя каждому выходному HTML-документу.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Сохраняет все страницы в файл и каталог, указанные внутри.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую страницу документа.
        // 1 - Установить имя файла выходной страницы:
        args.PageFileName = outFileName;

        // 2 — Создать собственный поток для выходного файла страницы:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


