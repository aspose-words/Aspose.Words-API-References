---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words для .NET
description: Узнайте, как Aspose.Words.Saving.HtmlOfficeMathOutputMode улучшает экспорт OfficeMath в HTML, MHTML и EPUB для бесшовного преобразования документов.
type: docs
weight: 5850
url: /ru/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

Указывает, как Aspose.Words экспортирует OfficeMath в HTML, MHTML и EPUB.

```csharp
public enum HtmlOfficeMathOutputMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Image | `0` | OfficeMath преобразуется в HTML как изображение, указанное тегом &lt;img&gt;. |
| MathML | `1` | OfficeMath преобразуется в HTML с помощью MathML. |
| Text | `2` | OfficeMath преобразуется в HTML как последовательность запусков, указанных тегами &lt;span&gt;. |

## Примеры

Показывает, как указать способ экспорта объектов Microsoft OfficeMath в HTML.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions
// чтобы определить, как операция сохранения обрабатывает объекты OfficeMath.
// Устанавливаем свойство "OfficeMathOutputMode" на "HtmlOfficeMathOutputMode.Image"
// преобразует каждый объект OfficeMath в изображение.
// Устанавливаем свойство "OfficeMathOutputMode" в "HtmlOfficeMathOutputMode.MathML"
// преобразует каждый объект OfficeMath в MathML.
// Устанавливаем свойство "OfficeMathOutputMode" в значение "HtmlOfficeMathOutputMode.Text"
// будет представлять каждую формулу OfficeMath с помощью обычного HTML-текста.
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                "-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.MathML:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">" +
                "<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" +
                    "<mi>i</mi>" +
                    "<mo>[+]</mo>" +
                    "<mi>b</mi>" +
                    "<mo>-</mo>" +
                    "<mi>c</mi>" +
                    "<mo>≥</mo>" +
                    ".*" +
                "</math>" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.Text:
        Assert.True(Regex.Match(outDocContents,
            @"<p style=\""margin-top:0pt; margin-bottom:10pt; text-align:center\"">" +
                @"<span style=\""font-family:'Cambria Math'\"">i[+]b-c≥iM[+]bM-cM </span>" +
            "</p>").Success);
        break;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
