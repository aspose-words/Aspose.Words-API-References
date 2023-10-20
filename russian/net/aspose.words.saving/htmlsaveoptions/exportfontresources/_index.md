---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ExportFontResources свойство. Указывает следует ли экспортировать ресурсы шрифтов в HTML MHTML или EPUB. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 140
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Указывает, следует ли экспортировать ресурсы шрифтов в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportFontResources { get; set; }
```

## Примечания

Экспорт ресурсов шрифтов позволяет обеспечить единообразную визуализацию документов независимо от доступных шрифтов в среде конкретного пользователя.

Если`ExportFontResources` установлено на`истинный` , основной HTML-документ будет ссылаться на каждый шрифт через CSS 3.**@font-face** at-rule и шрифты будут выводиться как отдельные файлы. При экспорте в форматы IDPF EPUB или MHTML шрифты будут встроены в соответствующий пакет вместе с другими вспомогательными файлами.

Если[`ExportFontsAsBase64`](../exportfontsasbase64/) установлено на`истинный` шрифты не будут сохраняться в отдельные файлы. Вместо этого они будут встроены в**@font-face** at-правила в кодировке Base64.

**Важный!** При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, которые хотят использовать определенные шрифты с помощью механизма шрифтов downloadable , должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии на шрифт. Многие коммерческие шрифты в настоящее время не позволяют загружать их через Интернет в любой форме. В лицензионных соглашениях, охватывающих некоторые шрифты, особо отмечается, что их использование через**@font-face** Rules в таблицах стилей CSS не допускается. Подмножество шрифтов также может нарушать условия лицензии.

## Примеры

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

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
