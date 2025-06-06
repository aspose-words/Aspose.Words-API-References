---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlSaveOptions ExportRelativeFontSize для настройки размеров шрифтов в форматах HTML, MHTML или EPUB. Улучшите читаемость с легкостью!
type: docs
weight: 230
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Указывает, следует ли выводить размеры шрифта в относительных единицах при сохранении в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Примечания

Во многих существующих документах (HTML, IDPF EPUB) размеры шрифтов указаны в относительных единицах. Это позволяет приложениям настраивать размер текста при просмотре/обработке документов. Например, Microsoft Internet Explorer имеет подменю "Вид-&gt;Размер текста", Adobe Digital Editions имеет две кнопки: Увеличить/Уменьшить размер текста. Если вы ожидаете, что эта функция будет работать, то установите`ExportRelativeFontSize` собственность`истинный` .

Модель документа Aspose Words содержит и оперирует только абсолютными единицами размера шрифта. Относительные единицы требуют дополнительной логики для пересчета из некоторого начального (стандартного) размера. Размер шрифта**Нормальный** Документ style принимается как стандарт. Например, если**Нормальный** имеет шрифт 12pt, а какой-то текст имеет размер 18pt, то он будет выведен как output как**1,5 см.** в HTML.

Если эта опция включена, элементы документа, отличные от текста, по-прежнему будут иметь абсолютные размеры. Также некоторые атрибуты, связанные с текстом, могут быть выражены абсолютно. В частности, указанный с помощью "exactly" rule интервал между строками может привести к нежелательным результатам при масштабировании текста. Поэтому исходные документы должны быть правильно спроектированы и проверены при экспорте с помощью`ExportRelativeFontSize` установлен на`истинный`.

## Примеры

Показывает, как использовать относительные размеры шрифта при сохранении в формате .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions
// чтобы определить, следует ли использовать относительные или абсолютные размеры шрифта.
// Установите флаг "ExportRelativeFontSize" в значение "true", чтобы объявить размеры шрифта
 // с использованием единицы измерения «em», которая является коэффициентом, умножающим текущий размер шрифта.
// Установите флаг "ExportRelativeFontSize" на "false", чтобы объявить размеры шрифта
// с использованием единицы измерения «pt», которая представляет собой абсолютный размер шрифта в пунктах.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
