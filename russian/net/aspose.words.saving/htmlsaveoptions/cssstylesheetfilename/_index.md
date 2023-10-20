---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words для .NET
description: HtmlSaveOptions CssStyleSheetFileName свойство. Указывает путь и имя файла каскадной таблицы стилей CSS записываемого при экспорте документа в HTML. По умолчанию  пустая строка на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Указывает путь и имя файла каскадной таблицы стилей (CSS), записываемого при экспорте документа в HTML. По умолчанию — пустая строка.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Примечания

Это свойство действует только при сохранении документа в формате HTML и внешней таблице стилей CSS, запрашиваемой с помощью[`CssStyleSheetType`](../cssstylesheettype/).

Если это свойство пусто, файл CSS будет сохранен в той же папке и с тем же именем, что и документ HTML , но с расширением «.css».

Если в этом свойстве указан только путь, но не имя файла, файл CSS будет сохранен в папке указанной и будет иметь то же имя, что и документ HTML, но с расширением «.css».

Если папка, указанная этим свойством, не существует, она будет создана автоматически перед сохранением файла CSS file .

Другой способ указать папку, в которой сохраняется внешний файл CSS, — использовать[`ResourceFolder`](../resourcefolder/) .

## Примеры

Показывает, как работать с таблицами стилей CSS, создаваемыми преобразованием HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Создаем объект HtmlFixedSaveOptions, который мы можем передать методу Save документа.
    // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Установите для свойства «CssStylesheetType» значение «CssStyleSheetType.External», чтобы
    // сопровождаем сохраненный HTML-документ внешним файлом таблицы стилей CSS.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Ниже приведены два способа указания каталогов и имен файлов для выходных таблиц стилей CSS.
    // 1 — используйте свойство «CssStyleSheetFileName», чтобы присвоить имя файла нашей таблице стилей:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 — Используйте собственный обратный вызов для присвоения имени нашей таблице стилей:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Устанавливает собственное имя файла вместе с другими параметрами для внешней таблицы стилей CSS.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // Мы можем получить доступ ко всему исходному документу через свойство «Документ».
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
