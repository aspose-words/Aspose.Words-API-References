---
title: HtmlSaveOptions.ExportRoundtripInformation
linktitle: ExportRoundtripInformation
articleTitle: ExportRoundtripInformation
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ExportRoundtripInformation HtmlSaveOptions для управления данными о круговой передаче в форматах HTML, MHTML и EPUB. Оптимизируйте свой экспорт сегодня!
type: docs
weight: 240
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportroundtripinformation/
---
## HtmlSaveOptions.ExportRoundtripInformation property

Указывает, следует ли записывать информацию о цикле передачи при сохранении в формате HTML, MHTML или EPUB. Значение по умолчанию:`истинный` для HTML и`ЛОЖЬ` для MHTML и EPUB.

```csharp
public bool ExportRoundtripInformation { get; set; }
```

## Примечания

Сохранение информации о цикле позволяет восстанавливать свойства документа, такие как позиции табуляции, комментарии , верхние и нижние колонтитулы во время загрузки HTML-документов обратно в[`Document`](../../../aspose.words/document/) объект.

Когда`истинный`, информация о круговом пути экспортируется как -aw-* CSS properties соответствующих HTML-элементов.

Когда`ЛОЖЬ`, приводит к тому, что в создаваемые файлы не выводится информация о круговом пути.

## Примеры

Показывает, как сохранить скрытые элементы при конвертации в .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// При конвертации документа в .html некоторые элементы, такие как скрытые закладки, исходные положения фигур,
// или сноски будут либо удалены, либо преобразованы в обычный текст и фактически потеряны.
// Сохранение с помощью объекта HtmlSaveOptions, для которого ExportRoundtripInformation установлено значение true, сохранит эти элементы.

// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions, чтобы определить
// как операция сохранения будет экспортировать элементы документа, которые HTML не поддерживает или не использует,
// например, скрытые закладки и исходные положения фигур.
// Если установить флаг «ExportRoundtripInformation» в значение «true», операция сохранения сохранит эти элементы.
// Если установить флаг «ExportRoundTripInformation» в значение «false», операция сохранения отбросит эти элементы.
// Мы захотим сохранить такие элементы, если собираемся загрузить сохраненный HTML с помощью Aspose.Words,
// так как они могут снова пригодиться.
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

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
