---
title: IFontSavingCallback.FontSaving
second_title: Справочник по API Aspose.Words для .NET
description: IFontSavingCallback метод. Вызывается когда Aspose.Words собирается сохранить ресурс шрифта.
type: docs
weight: 10
url: /ru/net/aspose.words.saving/ifontsavingcallback/fontsaving/
---
## IFontSavingCallback.FontSaving method

Вызывается, когда Aspose.Words собирается сохранить ресурс шрифта.

```csharp
public void FontSaving(FontSavingArgs args)
```

### Примеры

Показывает, как определить пользовательскую логику для экспорта шрифтов при сохранении в HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Настройте объект SaveOptions для экспорта шрифтов в отдельные файлы.
    // Установите обратный вызов, который будет обрабатывать сохранение шрифта в пользовательском порядке.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Обратный вызов экспортирует файлы .ttf и сохраняет их вместе с выходным документом.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

/// <summary>
/// Выводит информацию об экспортированных шрифтах и сохраняет их в той же локальной системной папке, что и их выходной .html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Мы также можем получить доступ к исходному документу отсюда.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Есть два способа сохранить экспортированный шрифт.
        // 1 - Сохраните его в локальной файловой системе:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Сохраняем в поток:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Смотрите также

* class [FontSavingArgs](../../fontsavingargs/)
* interface [IFontSavingCallback](../)
* пространство имен [Aspose.Words.Saving](../../ifontsavingcallback/)
* сборка [Aspose.Words](../../../)


