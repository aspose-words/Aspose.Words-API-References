---
title: HtmlFixedSaveOptions.FontFormat
linktitle: FontFormat
articleTitle: FontFormat
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlFixedSaveOptions FontFormat для настройки экспорта шрифтов. Легко установите и оптимизируйте свой формат по умолчанию на Woff для лучшей производительности.
type: docs
weight: 90
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/fontformat/
---
## HtmlFixedSaveOptions.FontFormat property

Получает или устанавливает[`ExportFontFormat`](../../exportfontformat/) используется для экспорта шрифтов. Значение по умолчанию:Woff .

```csharp
public ExportFontFormat FontFormat { get; set; }
```

## Примеры

Показывает, как использовать шрифты только с целевого компьютера при сохранении документа в формате HTML.

```csharp
Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = true,
    UseTargetMachineFonts = useTargetMachineFonts,
    FontFormat = ExportFontFormat.Ttf,
    ExportEmbeddedFonts = false,
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
    Assert.False(Regex.Match(outDocContents, "@font-face").Success);
else
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], " +
        "url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }").Success);
```

### Смотрите также

* enum [ExportFontFormat](../../exportfontformat/)
* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
