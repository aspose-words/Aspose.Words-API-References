---
title: ExportRoundtripInformation
second_title: Справочник по API Aspose.Words для .NET
description: Указывает следует ли записывать информацию о пути туда и обратно при сохранении в HTML MHTML или EPUB. Значение по умолчанию true для HTML и false для MHTML и EPUB.
type: docs
weight: 250
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Указывает, следует ли записывать информацию о пути туда и обратно при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:` true` для HTML и` false` для MHTML и EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

### Примечания

Сохранение информации об обходе позволяет восстановить свойства документа, такие как позиции табуляции, комментарии, верхние и нижние колонтитулы во время загрузки документов HTML обратно в объект[`Document`](../../../aspose.words/document).

Когда` true` , информация о пути туда и обратно экспортируется как -aw-* свойства CSS соответствующих элементов HTML.

Когда` false` , в создаваемые файлы не выводится информация о циклическом обходе.

### Примеры

Показывает, как сохранить скрытые элементы при преобразовании в .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// При преобразовании документа в .html некоторые элементы, такие как скрытые закладки, исходные положения фигур,
// или сноски будут либо удалены, либо преобразованы в обычный текст и фактически потеряны.
// Сохранение с помощью объекта HtmlSaveOptions с параметром ExportRoundtripInformation, для которого задано значение true, сохранит эти элементы.

// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions, чтобы определить
// как операция сохранения будет экспортировать элементы документа, которые HTML не поддерживает или не использует,
// такие как скрытые закладки и исходные позиции фигур.
// Если мы установим флаг "ExportRoundtripInformation" в значение "true", операция сохранения сохранит эти элементы.
// Если мы установим флаг "ExportRoundTripInformation" в "false", операция сохранения отбросит эти элементы.
// Нам нужно сохранить такие элементы, если мы собираемся загрузить сохраненный HTML с помощью Aspose.Words,
// так как они могут быть полезны еще раз.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRoundtripInformation = exportRoundtripInformation };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");
doc = new Document(ArtifactsDir + "HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    Assert.True(outDocContents.Contains("<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    Assert.True(outDocContents.Contains("<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
        "-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" " +
        "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number </span>" +
        "<span style=\"-aw-field-start:true\"></span>" +
        "<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
        "<span style=\"-aw-field-separator:true\"></span>" +
        "<span>1</span>" +
        "<span style=\"-aw-field-end:true\"></span>"));

    Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
else
{
    Assert.True(outDocContents.Contains("<div style=\"clear:both\">"));
    Assert.True(outDocContents.Contains("<span>&#xa0;</span>"));

    Assert.True(outDocContents.Contains(
        "<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; " +
        "padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    Assert.True(outDocContents.Contains(
        "<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    Assert.True(outDocContents.Contains(
        "<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    Assert.True(outDocContents.Contains(
        "<span>Page number 1</span>"));

    Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldPage));
}
```

### Смотрите также

* class [HtmlSaveOptions](../../htmlsaveoptions)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
