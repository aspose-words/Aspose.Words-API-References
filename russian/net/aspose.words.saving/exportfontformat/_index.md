---
title: Enum ExportFontFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Saving.ExportFontFormat перечисление. Указывает формат используемый для экспорта шрифтов при отображении в фиксированный формат HTML.
type: docs
weight: 4730
url: /ru/net/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enumeration

Указывает формат, используемый для экспорта шрифтов при отображении в фиксированный формат HTML.

```csharp
public enum ExportFontFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Woff | `0` | WOFF (формат открытого веб-шрифта). |
| Ttf | `1` | TTF (формат шрифта TrueType). |

### Примеры

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

* property [FontFormat](../htmlfixedsaveoptions/fontformat/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)


