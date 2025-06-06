---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ConvertSvgToEmf HtmlLoadOptions. Легко управляйте преобразованием SVG в EMF для оптимального качества изображения. Значение по умолчанию — false; сохраняйте SVG нетронутыми!
type: docs
weight: 30
url: /ru/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Возвращает или задает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. Значение по умолчанию:`ЛОЖЬ` и, если возможно, загруженные SVG-изображения сохраняются как есть без конвертации.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Примечания

Более новые версии MS Word поддерживают изображения SVG изначально. Если версия MS Word, указанная в параметрах загрузки, поддерживает SVG, Aspose.Words сохранит изображения SVG как есть, без преобразования. Если SVG не поддерживается, загруженные изображения SVG будут преобразованы в формат EMF.

Однако, если эта опция установлена на`истинный` Aspose.Words преобразует загруженные изображения SVG в EMF, даже если изображения SVG поддерживаются указанной версией MS Word.

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

* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
