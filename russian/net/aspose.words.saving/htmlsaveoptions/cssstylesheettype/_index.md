---
title: HtmlSaveOptions.CssStyleSheetType
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words для .NET
description: Узнайте, как свойство CssStyleSheetType в HtmlSaveOptions оптимизирует экспорт CSS в форматы HTML, MHTML и EPUB для бесшовной интеграции.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/htmlsaveoptions/cssstylesheettype/
---
## HtmlSaveOptions.CssStyleSheetType property

Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию:Inline для HTML/MHTML и External для EPUB.

```csharp
public CssStyleSheetType CssStyleSheetType { get; set; }
```

## Примечания

Сохранение таблицы стилей CSS во внешний файл поддерживается только при сохранении в HTML. При экспорте в один из форматов контейнера (EPUB или MHTML) и указании External, CSS-файл будет инкапсулирован в выходной пакет.

## Примеры

Показывает, как работать с таблицами стилей CSS, создаваемыми при преобразовании HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Создаем объект "HtmlFixedSaveOptions", который можно передать методу "Save" документа
    // чтобы изменить способ преобразования документа в HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Установите свойство "CssStylesheetType" на "CssStyleSheetType.External" для
    // сопроводить сохраненный HTML-документ внешним файлом таблицы стилей CSS.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Ниже приведены два способа указания каталогов и имен файлов для выходных таблиц стилей CSS.
    // 1 - Используйте свойство "CssStyleSheetFileName", чтобы назначить имя файла нашей таблице стилей:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Используйте пользовательский обратный вызов для присвоения имени нашей таблице стилей:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Задает пользовательское имя файла, а также другие параметры для внешней таблицы стилей CSS.
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

* property [CssStyleSheetFileName](../cssstylesheetfilename/)
* enum [CssStyleSheetType](../../cssstylesheettype/)
* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
