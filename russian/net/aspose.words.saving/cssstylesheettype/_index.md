---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.CssStyleSheetType перечисление. Указывает как стили CSS каскадная таблица стилей экспортируются в HTML на С#.
type: docs
weight: 4890
url: /ru/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Указывает, как стили CSS (каскадная таблица стилей) экспортируются в HTML.

```csharp
public enum CssStyleSheetType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Inline | `0` | Стили CSS записываются встроенно (как значение**стиль** атрибут каждого элемента). |
| Embedded | `1` | Стили CSS записываются отдельно от содержимого в таблице стилей, встроенной в файл HTML. |
| External | `2` | Стили CSS записываются отдельно от содержимого таблицы стилей во внешнем файле. Файл HTML связывает таблицу стилей. |

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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
