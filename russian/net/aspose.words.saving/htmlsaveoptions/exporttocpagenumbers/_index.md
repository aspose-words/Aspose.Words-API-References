---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words для .NET
description: HtmlSaveOptions ExportTocPageNumbers свойство. Указывает записывать ли номера страниц в оглавление при сохранении HTML MHTML и EPUB. Значение по умолчаниюЛОЖЬ  на С#.
type: docs
weight: 270
url: /ru/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Указывает, записывать ли номера страниц в оглавление при сохранении HTML, MHTML и EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Примеры

Показывает, как отображать номера страниц при сохранении документа с оглавлением в формате .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем оглавление, а затем заполняем документ абзацами, отформатированными с использованием «Заголовка»
// стиль, который оглавление будет воспринимать как записи. Для каждой записи слева будет отображаться абзац заголовка.
// и номер страницы, содержащей заголовок справа.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// HTML-документы не имеют страниц. Если мы сохраним этот документ в HTML,
// номера страниц, отображаемые нашим оглавлением, не будут иметь значения.
// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions, чтобы исключить эти номера страниц из оглавления.
// Если мы установим флаг «ExportTocPageNumbers» в значение «true»,
// каждая запись оглавления будет отображать заголовок, разделитель и номер страницы, сохраняя свой внешний вид в Microsoft Word.
// Если мы установим флаг «ExportTocPageNumbers» в значение «false»,
// операция сохранения пропустит разделитель и номер страницы и оставит заголовок для каждой записи нетронутым.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
