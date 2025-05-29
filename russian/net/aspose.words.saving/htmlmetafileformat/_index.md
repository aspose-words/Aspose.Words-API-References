---
title: HtmlMetafileFormat Enum
linktitle: HtmlMetafileFormat
articleTitle: HtmlMetafileFormat
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Saving.HtmlMetafileFormat для бесшовного сохранения метафайлов в документах HTML. Улучшите свой опыт преобразования документов сегодня!
type: docs
weight: 5840
url: /ru/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

Указывает формат, в котором метафайлы сохраняются в HTML-документах.

```csharp
public enum HtmlMetafileFormat
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Png | `0` | Метафайлы преобразуются в растровые изображения PNG. |
| Svg | `1` | Метафайлы преобразуются в векторные изображения SVG. |
| EmfOrWmf | `2` | Метафайлы сохраняются как есть, без преобразования. |

## Примеры

Показывает, как преобразовать объекты SVG в другой формат при сохранении HTML-документов.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Используйте 'ConvertSvgToEmf', чтобы вернуть старое поведение
// где все изображения SVG, загруженные из HTML-документа, были преобразованы в EMF.
// Теперь SVG-изображения загружаются без конвертации
// если версия MS Word, указанная в параметрах загрузки, изначально поддерживает изображения SVG.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Этот документ содержит элемент <svg> в виде текста.
// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions
// чтобы определить, как операция сохранения обрабатывает этот объект.
// Устанавливаем свойство "MetafileFormat" на "HtmlMetafileFormat.Png", чтобы преобразовать его в изображение PNG.
// Установка свойства "MetafileFormat" в "HtmlMetafileFormat.Svg" сохранит его как объект SVG.
// Устанавливаем свойство "MetafileFormat" в значение "HtmlMetafileFormat.EmfOrWmf", чтобы преобразовать его в метафайл.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" версия=\"1.1\" ширина=\"499\" высота=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Смотрите также

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
