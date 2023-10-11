---
title: FontSavingArgs.FontFileName
second_title: Справочник по API Aspose.Words для .NET
description: FontSavingArgs свойство. Получает или задает имя файла без пути в котором будет сохранен шрифт.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Получает или задает имя файла (без пути), в котором будет сохранен шрифт.

```csharp
public string FontFileName { get; set; }
```

### Примечания

Это свойство позволяет переопределить способ создания имен файлов шрифтов во время экспорта в HTML.

Когда событие запускается, это свойство содержит имя файла , созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить шрифт в другом файле . Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного шрифта при экспорте в формат HTML. Способ создания имени файла шрифта зависит от того, сохраняете ли вы документ в файл или в поток.

При сохранении документа в файл имя сгенерированного файла шрифта выглядит как .&lt;имя файла базы документов&gt;.&lt;исходное имя файла&gt;&lt;необязательный суффикс&gt;.&lt;расширение&gt;.

При сохранении документа в поток имя сгенерированного файла шрифта выглядит как .Aspose.Words.&lt;руководство документа&gt;.&lt;исходное имя файла&gt;&lt;необязательный суффикс&gt;.&lt;расширение&gt;.

`FontFileName` должно содержать только имя файла без пути. Aspose.Words определяет путь для сохранения, используя имя файла документа, [`FontsFolder`](../../htmlsaveoptions/fontsfolder/) and [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) характеристики.

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

* class [FontSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../fontsavingargs/)
* сборка [Aspose.Words](../../../)


