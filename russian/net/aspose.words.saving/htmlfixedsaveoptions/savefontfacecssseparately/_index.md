---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: Aspose.Words для .NET
description: HtmlFixedSaveOptions SaveFontFaceCssSeparately свойство. Флаг указывает следует ли помещать правила CSS fontface в отдельный файл fontFaces.css  когда документ сохраняется с внешней таблицей стилей т. е. когдаExportEmbeddedCss этоЛОЖЬ . Значение по умолчаниюЛОЖЬ  все правила CSS записаны в один файл styles.css на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

Флаг указывает, следует ли помещать правила CSS «@font-face» в отдельный файл «fontFaces.css» , когда документ сохраняется с внешней таблицей стилей (т. е. когда[`ExportEmbeddedCss`](../exportembeddedcss/) это`ЛОЖЬ` ). Значение по умолчанию:`ЛОЖЬ` , все правила CSS записаны в один файл «styles.css».

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## Примечания

Установка этого свойства в`истинный` восстанавливает старое поведение (отдельные файлы) для совместимости с устаревшим кодом.

## Примеры

Показывает, как поместить CSS в отдельный файл и добавить префикс ко всем именам его классов CSS.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
