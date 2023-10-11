---
title: HtmlSaveOptions.ResolveFontNames
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает разрешаются ли и заменяются ли имена семейств шрифтов используемые в документе в соответствии с .FontSettings при записи в форматы на основе HTML.
type: docs
weight: 410
url: /ru/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Указывает, разрешаются ли и заменяются ли имена семейств шрифтов, используемые в документе, в соответствии с .[`FontSettings`](../../../aspose.words/document/fontsettings/) при записи в форматы на основе HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

### Примечания

По умолчанию для этой опции установлено значение`ЛОЖЬ` а имена семейств шрифтов записываются в HTML как указано в исходных документах. То есть,[`FontSettings`](../../../aspose.words/document/fontsettings/) игнорируются, и никакое разрешение или замена имен семейств шрифтов не выполняется.

Если для этой опции установлено значение`истинный` , Aspose.Words использует[`FontSettings`](../../../aspose.words/document/fontsettings/) разрешить каждое имя семейства шрифтов, указанное в исходном документе, в имя доступного семейства шрифтов, выполняя при необходимости замену шрифта .

### Примеры

Показывает, как разрешить все имена шрифтов перед их записью в HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Этот документ содержит текст с именем шрифта, которого у нас нет.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Если у нас нет возможности получить этот шрифт, и мы хотим иметь возможность отображать весь текст
// в этом документе в выходном HTML мы можем заменить его другим шрифтом.
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
    // По умолчанию для этой опции установлено значение «False», и Aspose.Words записывает имена шрифтов, указанные в исходном документе.
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
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


