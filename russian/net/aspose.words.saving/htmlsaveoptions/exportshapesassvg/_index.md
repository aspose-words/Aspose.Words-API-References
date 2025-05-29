---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
articleTitle: ExportShapesAsSvg
second_title: Aspose.Words для .NET
description: Узнайте, как использовать HtmlSaveOptions ExportShapesAsSvg для преобразования узлов Shape в изображения SVG при сохранении в форматах HTML, MHTML, EPUB или AZW3.
type: docs
weight: 250
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

Управляет тем,[`Shape`](../../../aspose.words.drawing/shape/)узлы преобразуются в изображения SVG при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## Примечания

Если эта опция установлена на`истинный` ,[`Shape`](../../../aspose.words.drawing/shape/) Узлы экспортируются как элементы &lt;svg&gt;. В противном случае они преобразуются в растровые изображения и экспортируются как элементы &lt;img&gt;.

## Примеры

Показывает, как экспортировать форму в виде масштабируемой векторной графики.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// Когда мы сохраняем документ в HTML, мы можем передать объект SaveOptions
// чтобы определить, как операция сохранения будет экспортировать формы текстовых полей.
// Если мы установим флаг "ExportTextBoxAsSvg" на "true",
// операция сохранения преобразует фигуры с текстом в объекты SVG.
// Если мы установим флаг "ExportTextBoxAsSvg" на "false",
// операция сохранения преобразует фигуры с текстом в изображения.
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" версия=\"1.1\" ширина=\"133\" высота=\"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
