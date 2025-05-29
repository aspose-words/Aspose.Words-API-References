---
title: IFontSavingCallback Interface
linktitle: IFontSavingCallback
articleTitle: IFontSavingCallback
second_title: Aspose.Words для .NET
description: Управляйте сохранением шрифтов в Aspose.Words с помощью интерфейса IFontSavingCallback. Получайте уведомления и настраивайте экспорт HTML для оптимального качества документа.
type: docs
weight: 5910
url: /ru/net/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface

Реализуйте этот интерфейс, если вы хотите получать уведомления и контролировать, как Aspose.Words сохраняет шрифты при экспорте документа в формат HTML.

```csharp
public interface IFontSavingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [FontSaving](../../aspose.words.saving/ifontsavingcallback/fontsaving/)(*[FontSavingArgs](../fontsavingargs/)*) | Вызывается, когда Aspose.Words собирается сохранить ресурс шрифта. |

## Примеры

Показывает, как определить пользовательскую логику для экспорта шрифтов при сохранении в HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Настройте объект SaveOptions для экспорта шрифтов в отдельные файлы.
    // Устанавливаем обратный вызов, который будет обрабатывать сохранение шрифта специальным образом.
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

        // Отсюда мы также можем получить доступ к исходному документу.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Существует два способа сохранения экспортированного шрифта.
        // 1 - Сохраните его в локальной файловой системе:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Сохранить в потоке:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
