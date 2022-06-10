---
title: FontSavingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Предоставляет данные для событияFontSaving./ifontsavingcallback/fontsaving.
type: docs
weight: 4720
url: /ru/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Предоставляет данные для события[`FontSaving`](../ifontsavingcallback/fontsaving).

```csharp
public class FontSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold) { get; } | Указывает, является ли текущий шрифт полужирным. |
| [Document](../../aspose.words.saving/fontsavingargs/document) { get; } | Получает сохраняемый объект документа. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname) { get; } | Указывает текущее имя семейства шрифтов. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename) { get; set; } | Получает или задает имя файла (без пути), в котором будет сохранен шрифт. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream) { get; set; } | Позволяет указать поток, в который будет сохранен шрифт. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded) { get; set; } | Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. Значение по умолчанию:` true` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded) { get; set; } | Позволяет указать, будет ли текущий шрифт подмножаться перед экспортом в качестве ресурса шрифта. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic) { get; } | Указывает, является ли текущий шрифт курсивным. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen) { get; set; } | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения шрифта. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename) { get; } | Получает исходное имя файла шрифта с расширением. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize) { get; } | Получает исходный размер файла шрифта. |

### Примечания

Когда Aspose.Words сохраняет документ в HTML или родственных форматах и[`ExportFontResources`](../htmlsaveoptions/exportfontresources) имеет значение **true** , он сохраняет каждую тему шрифта для экспорта в отдельный файл.

[`FontSavingArgs`](../fontsavingargs)определяет, следует ли экспортировать определенный ресурс шрифта и каким образом.

[`FontSavingArgs`](../fontsavingargs)также позволяет переопределить способ генерации имен файлов шрифтов или полностью обойти сохранение шрифтов в файлы, предоставив свои собственные потоковые объекты.

Чтобы решить, сохранять ли конкретный ресурс шрифта, используйте свойство[`IsExportNeeded`](./isexportneeded).

Для сохранения шрифтов в потоки вместо файлов используйте свойство[`FontStream`](./fontstream).

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
