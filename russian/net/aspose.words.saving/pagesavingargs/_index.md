---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.PageSavingArgs, необходимый для оптимизации обработки документов с подробными данными событий PageSaving. Улучшите свой рабочий процесс!
type: docs
weight: 6160
url: /ru/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Предоставляет данные для[`PageSaving`](../ipagesavingcallback/pagesaving/) событие.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

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
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Указывает, должен ли Aspose.Words держать поток открытым или закрыть его после сохранения страницы документа. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Возвращает или задает имя файла, в котором будет сохранена страница документа. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Текущая страница index. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Позволяет указать поток, в который будет сохранена страница документа. |

## Примеры

Показывает, как использовать обратный вызов для постраничного сохранения документа в формате HTML.

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

    // Создаем объект "HtmlFixedSaveOptions", который можно передать методу "Save" документа
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
/// Сохраняет все страницы в указанном файле и каталоге.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Ниже приведены два способа указать, где Aspose.Words будет сохранять каждую страницу документа.
        // 1 — Задайте имя файла для выходного файла страницы:
        args.PageFileName = outFileName;

        // 2 — Создать пользовательский поток для выходного файла страницы:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
