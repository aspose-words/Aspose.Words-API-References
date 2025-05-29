---
title: FontSavingArgs.FontFileName
linktitle: FontFileName
articleTitle: FontFileName
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FontSavingArgs FontFileName, легко управляйте именами файлов шрифтов и улучшите свой рабочий процесс проектирования с помощью удобных возможностей сохранения.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Возвращает или задает имя файла (без пути), в котором будет сохранен шрифт.

```csharp
public string FontFileName { get; set; }
```

## Примечания

Это свойство позволяет переопределить способ генерации имен файлов шрифтов во время экспорта в HTML.

При запуске события это свойство содержит имя файла, сгенерированное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить шрифт в другом файле. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного шрифта при экспорте в формат HTML. То, как генерируется имя файла шрифта , зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл сгенерированное имя файла шрифта выглядит как &lt;имя файла базы документа&gt;.&lt;исходное имя файла&gt;&lt;необязательный суффикс&gt;.&lt;расширение&gt;.

При сохранении документа в потоке сгенерированное имя файла шрифта выглядит как Aspose.Words.&lt;guid документа&gt;.&lt;исходное имя файла&gt;&lt;необязательный суффикс&gt;.&lt;расширение&gt;.

`FontFileName` должно содержать только имя файла без пути. Aspose.Words определяет путь для сохранения, используя имя файла документа, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) и [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) характеристики.

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
