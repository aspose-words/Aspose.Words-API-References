---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.CssSavingArgs, разработанный для улучшения обработки документов с помощью настраиваемых данных событий CssSaving для достижения оптимальных результатов.
type: docs
weight: 5620
url: /ru/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Предоставляет данные для[`CssSaving`](../icsssavingcallback/csssaving/) событие.

Чтобы узнать больше, посетите[Сохранить документ](https://docs.aspose.com/words/net/save-a-document/) документальная статья.

```csharp
public class CssSavingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Позволяет указать поток, в котором будет сохранена информация CSS. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Получает объект документа, который в данный момент сохраняется. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Позволяет указать, будет ли CSS экспортирован в файл и встроен в HTML-документ. По умолчанию`истинный` . Когда это свойство`ЛОЖЬ` , информация CSS не будет сохранена в файле CSS и не будет встроена в документ HTML. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Указывает, должен ли Aspose.Words держать поток открытым или закрывать его после сохранения информации CSS. |

## Примечания

По умолчанию, когда Aspose.Words сохраняет документ в формате HTML, он сохраняет информацию CSS inline (как значение**стиль** атрибут для каждого элемента).

`CssSavingArgs` позволяет сохранять CSS-информацию в файл, предоставляя собственный потоковый объект.

Чтобы сохранить CSS в поток, используйте[`CssStream`](./cssstream/) свойство.

Чтобы запретить сохранение CSS в файл и встраивание в HTML-документ, используйте[`IsExportNeeded`](./isexportneeded/) свойство.

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
