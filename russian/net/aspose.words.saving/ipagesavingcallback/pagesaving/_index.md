---
title: IPageSavingCallback.PageSaving
linktitle: PageSaving
articleTitle: PageSaving
second_title: Aspose.Words для .NET
description: Откройте для себя метод iPageSavingCallback в Aspose.Words, разработанный для оптимизации сохранения страниц в фиксированные форматы. Улучшите управление документами сегодня!
type: docs
weight: 10
url: /ru/net/aspose.words.saving/ipagesavingcallback/pagesaving/
---
## IPageSavingCallback.PageSaving method

Вызывается, когда Aspose.Words сохраняет отдельную страницу в фиксированных форматах страниц.

```csharp
public void PageSaving(PageSavingArgs args)
```

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

* class [PageSavingArgs](../../pagesavingargs/)
* interface [IPageSavingCallback](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
