---
title: CssSavingArgs.KeepCssStreamOpen
linktitle: KeepCssStreamOpen
articleTitle: KeepCssStreamOpen
second_title: Aspose.Words для .NET
description: Откройте для себя свойство KeepCssStreamOpen в CssSavingArgs. Управляйте поведением потока Aspose.Words для эффективного сохранения CSS и повышения производительности.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/csssavingargs/keepcssstreamopen/
---
## CssSavingArgs.KeepCssStreamOpen property

Указывает, должен ли Aspose.Words держать поток открытым или закрывать его после сохранения информации CSS.

```csharp
public bool KeepCssStreamOpen { get; set; }
```

## Примечания

По умолчанию`ЛОЖЬ` и Aspose.Words закроет предоставленный вами поток в[`CssStream`](../cssstream/) свойство после записи в него CSS-информации. Укажите`истинный` чтобы поток оставался открытым.

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

* class [CssSavingArgs](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
