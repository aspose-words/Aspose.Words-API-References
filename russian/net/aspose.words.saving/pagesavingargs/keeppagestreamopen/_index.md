---
title: PageSavingArgs.KeepPageStreamOpen
second_title: Справочник по API Aspose.Words для .NET
description: PageSavingArgs свойство. Указывает должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения страницы документа.
type: docs
weight: 20
url: /ru/net/aspose.words.saving/pagesavingargs/keeppagestreamopen/
---
## PageSavingArgs.KeepPageStreamOpen property

Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения страницы документа.

```csharp
public bool KeepPageStreamOpen { get; set; }
```

### Примечания

По умолчанию`ЛОЖЬ` и Aspose.Words закроет предоставленный вами поток в[`PageStream`](../pagestream/) свойство после записи в него страницы документа. Указать`истинный` чтобы поток оставался открытым.

### Примеры

Показывает, как использовать обратный вызов для сохранения документа в формате HTML страница за страницей.

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

    // Создаем объект "HtmlFixedSaveOptions", который мы можем передать в метод документа "Сохранить"
    // чтобы изменить способ преобразования документа в HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Мы сохраним каждую страницу этого документа в отдельный файл HTML в локальной файловой системе.
    // Установите обратный вызов, который позволит нам назвать каждый выходной HTML-документ.
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
        // 1 - Установить имя файла для выходного файла страницы:
        args.PageFileName = outFileName;

        // 2 - Создайте собственный поток для выходного файла страницы:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Смотрите также

* class [PageSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../pagesavingargs/)
* сборка [Aspose.Words](../../../)


