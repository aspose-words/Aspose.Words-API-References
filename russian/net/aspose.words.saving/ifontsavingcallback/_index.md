---
title: Interface IFontSavingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.IFontSavingCallback интерфейс. Реализуйте этот интерфейс если хотите получать уведомления и контролировать как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML.
type: docs
weight: 5160
url: /ru/net/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface

Реализуйте этот интерфейс, если хотите получать уведомления и контролировать, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML.

```csharp
public interface IFontSavingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [FontSaving](../../aspose.words.saving/ifontsavingcallback/fontsaving/)(FontSavingArgs) | Вызывается, когда Aspose.Words собирается сохранить ресурс шрифта. |

### Примеры

Показывает, как определить пользовательскую логику для экспорта шрифтов при сохранении в HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Настройте объект SaveOptions для экспорта шрифтов в отдельные файлы.
    // Установите обратный вызов, который будет обрабатывать сохранение шрифта в индивидуальном порядке.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // Обратный вызов экспортирует файлы .ttf и сохранит их вместе с выходным документом.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Печатает информацию об экспортированных шрифтах и сохраняет их в той же локальной системной папке, что и их выходные файлы .html.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // Отсюда мы также можем получить доступ к исходному документу.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Есть два способа сохранить экспортированный шрифт.
        // 1 — сохранить его в локальной файловой системе:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 — Сохранить в поток:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


