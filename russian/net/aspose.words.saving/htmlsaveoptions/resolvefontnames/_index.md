---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ResolveFontNames улучшает форматирование документа, обеспечивая точную замену шрифтов в выходных данных HTML.
type: docs
weight: 430
url: /ru/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Указывает, разрешаются ли и заменяются ли имена семейств шрифтов, используемые в документе, в соответствии с [`FontSettings`](../../../aspose.words/document/fontsettings/) при записи в форматы на основе HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

## Примечания

По умолчанию эта опция установлена на`ЛОЖЬ` и имена семейств шрифтов записываются в HTML как указано в исходных документах. То есть,[`FontSettings`](../../../aspose.words/document/fontsettings/) игнорируются и не выполняется разрешение или замена имен семейств шрифтов.

Если эта опция установлена на`истинный` , Aspose.Words использует[`FontSettings`](../../../aspose.words/document/fontsettings/) для преобразования каждого имени семейства шрифтов, указанного в исходном документе, в имя доступного семейства шрифтов, выполняя замену шрифта по мере необходимости.

## Примеры

Показывает, как разрешить все имена шрифтов перед записью их в HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Этот документ содержит текст, в котором упоминается шрифт, которого у нас нет.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Если у нас нет возможности получить этот шрифт, а мы хотим иметь возможность отобразить весь текст
// в этом документе в выходном HTML-коде мы можем заменить его другим шрифтом.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // По умолчанию этот параметр имеет значение «False», и Aspose.Words записывает имена шрифтов, как указано в исходном документе.
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
