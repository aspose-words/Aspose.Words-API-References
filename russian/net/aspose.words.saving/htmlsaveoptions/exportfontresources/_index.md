---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions ExportFontResources для управления экспортом ресурсов шрифтов для HTML, MHTML или EPUB. Увеличьте визуальную привлекательность вашего документа!
type: docs
weight: 140
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportFontResources { get; set; }
```

## Примечания

Экспорт ресурсов шрифтов обеспечивает единообразную визуализацию документов независимо от доступных шрифтов в среде конкретного пользователя.

Если`ExportFontResources` установлен на`истинный` , основной HTML-документ будет ссылаться на каждый шрифт via CSS 3**@шрифт-face** at-rule и шрифты будут выводиться как отдельные файлы. При экспорте в форматы IDPF EPUB или MHTML шрифты будут встроены в соответствующий пакет вместе с другими вспомогательными файлами.

Если[`ExportFontsAsBase64`](../exportfontsasbase64/) установлен на`истинный` , шрифты не будут сохранены в отдельных файлах. Вместо этого они будут встроены в**@шрифт-face** at-правила в кодировке Base64.

**Важный!**При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, желающие использовать определенные шрифты через механизм загружаемых шрифтов, должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии шрифта. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. Лицензионные соглашения, охватывающие некоторые шрифты, специально отмечают, что использование через**@шрифт-face** rules в таблицах стилей CSS не допускается. Подмножество шрифтов также может нарушать условия лицензии.

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

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
