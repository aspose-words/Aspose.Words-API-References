---
title: FontSavingArgs.OriginalFileSize
linktitle: OriginalFileSize
articleTitle: OriginalFileSize
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontSavingArgs OriginalFileSize, которое позволяет эффективно получать исходный размер файла шрифта и расширяет возможности управления шрифтами.
type: docs
weight: 110
url: /ru/net/aspose.words.saving/fontsavingargs/originalfilesize/
---
## FontSavingArgs.OriginalFileSize property

Получает исходный размер файла шрифта.

```csharp
public int OriginalFileSize { get; }
```

## Примечания

Это свойство содержит исходный размер файла текущего шрифта, если он известен. В противном случае он может быть равен нулю.

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

* class [FontSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
