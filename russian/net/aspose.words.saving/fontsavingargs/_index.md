---
title: Class FontSavingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.FontSavingArgs сорт. Предоставляет данные дляFontSaving событие.
type: docs
weight: 5030
url: /ru/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Предоставляет данные для[`FontSaving`](../ifontsavingcallback/fontsaving/) событие.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) статья документации.

```csharp
public class FontSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Указывает, является ли текущий шрифт полужирным. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Получает сохраняемый объект документа. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Указывает текущее имя семейства шрифтов. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Получает или задает имя файла (без пути), в котором будет сохранен шрифт. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Позволяет указать поток, в котором будет сохранен шрифт. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. По умолчанию`истинный` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Позволяет указать, будет ли текущий шрифт подмножеством перед экспортом в качестве ресурса шрифта. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Указывает, является ли текущий шрифт курсивом. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Указывает, должен ли Aspose.Words сохранять поток открытым или закрывать его после сохранения шрифта. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Получает исходное имя файла шрифта с расширением. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Получает исходный размер файла шрифта. |

### Примечания

Когда Aspose.Words сохраняет документ в HTML или родственных форматах и[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) установлено на`истинный`, он сохраняет каждую тему шрифта для экспорта в отдельный файл.

`FontSavingArgs` контролирует, следует ли экспортировать конкретный ресурс шрифта и каким образом.

`FontSavingArgs`также позволяет переопределить способ создания имен файлов шрифтов или полностью обойти сохранение шрифтов в файлах, предоставив свои собственные объекты потока.

Чтобы решить, сохранять ли конкретный ресурс шрифта, используйте команду[`IsExportNeeded`](./isexportneeded/) свойство.

Чтобы сохранить шрифты в потоки, а не в файлы, используйте команду[`FontStream`](./fontstream/) свойство.

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


