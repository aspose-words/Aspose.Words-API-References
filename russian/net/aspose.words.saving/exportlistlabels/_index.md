---
title: ExportListLabels Enum
linktitle: ExportListLabels
articleTitle: ExportListLabels
second_title: Aspose.Words для .NET
description: Узнайте, как перечисление Aspose.Words.Saving.ExportListLabels улучшает экспорт HTML, MHTML и EPUB с помощью настраиваемых параметров меток списков.
type: docs
weight: 5760
url: /ru/net/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enumeration

Указывает, как метки списков экспортируются в HTML, MHTML и EPUB.

```csharp
public enum ExportListLabels
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Auto | `0` | Выводит списки меток в автоматическом режиме. Использует собственные элементы HTML, когда это возможно. |
| AsInlineText | `1` | Выводит все метки списка как встроенный текст. |
| ByHtmlTags | `2` | Выводит все метки списков как собственные элементы HTML. |

## Примеры

Показывает, как настроить экспорт списка в HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Aspose.Words.Lists.List list = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = list;

builder.Writeln("Default numbered list item 1.");
builder.Writeln("Default numbered list item 2.");
builder.ListFormat.ListIndent();
builder.Writeln("Default numbered list item 3.");
builder.ListFormat.RemoveNumbers();

list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
builder.ListFormat.List = list;

builder.Writeln("Outline legal heading list item 1.");
builder.Writeln("Outline legal heading list item 2.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 3.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 4.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 5.");
builder.ListFormat.RemoveNumbers();

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы решить, какие элементы HTML документ будет использовать для представления списков.
// Установка свойства "ExportListLabels" в значение "ExportListLabels.AsInlineText"
// создаст списки путем форматирования интервалов.
// Установка свойства "ExportListLabels" в "ExportListLabels.Auto" будет использовать тег <p>
// для построения списков в случаях, когда использование тегов <ol> и <li> может привести к потере форматирования.
// Установка свойства "ExportListLabels" в "ExportListLabels.ByHtmlTags"
// будет использовать теги <ol> и <li> для построения всех списков.
HtmlSaveOptions options = new HtmlSaveOptions { ExportListLabels = exportListLabels };

doc.Save(ArtifactsDir + "HtmlSaveOptions.List.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.List.html");

switch (exportListLabels)
{
    case ExportListLabels.AsInlineText:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>a.</span>" +
                    "<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Default numbered list item 3.</span>" +
            "</p>"));

        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>2.1.1.1</span>" +
                    "<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Outline legal heading list item 5.</span>" +
            "</p>"));
        break;
    case ExportListLabels.Auto:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));
        break;
    case ExportListLabels.ByHtmlTags:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));
        break;
}
```

### Смотрите также

* property [ExportListLabels](../htmlsaveoptions/exportlistlabels/)
* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
