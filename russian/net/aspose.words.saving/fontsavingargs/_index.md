---
title: FontSavingArgs Class
linktitle: FontSavingArgs
articleTitle: FontSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Saving.FontSavingArgs — улучшите обработку документов с помощью подробных данных о событиях FontSaving для превосходной настройки и контроля.
type: docs
weight: 5780
url: /ru/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Предоставляет данные для[`FontSaving`](../ifontsavingcallback/fontsaving/) событие.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class FontSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Указывает, является ли текущий шрифт полужирным. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Получает объект документа, который сохраняется. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Указывает текущее имя семейства шрифтов. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Возвращает или задает имя файла (без пути), в котором будет сохранен шрифт. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Позволяет указать поток, в который будет сохранен шрифт. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Позволяет указать, будет ли текущий шрифт экспортироваться как ресурс шрифта. По умолчанию`истинный` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Позволяет указать, будет ли текущий шрифт разделен на подмножества перед экспортом в качестве ресурса шрифта. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Указывает, является ли текущий шрифт курсивом. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Указывает, должен ли Aspose.Words держать поток открытым или закрыть его после сохранения шрифта. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Получает исходное имя файла шрифта с расширением . |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Получает исходный размер файла шрифта. |

## Примечания

Когда Aspose.Words сохраняет документ в HTML или связанных форматах и[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) установлен на`истинный`, он сохраняет каждую тему шрифта для экспорта в отдельный файл.

`FontSavingArgs` контролирует, следует ли экспортировать определенный ресурс шрифта и каким образом.

`FontSavingArgs`также позволяет переопределить способ генерации имен файлов шрифтов или полностью обойти сохранение шрифтов в файлы, предоставив собственные потоковые объекты.

Чтобы решить, следует ли сохранять определенный ресурс шрифта, используйте[`IsExportNeeded`](./isexportneeded/) свойство.

Чтобы сохранить шрифты в потоки, а не в файлы, используйте[`FontStream`](./fontstream/) свойство.

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
