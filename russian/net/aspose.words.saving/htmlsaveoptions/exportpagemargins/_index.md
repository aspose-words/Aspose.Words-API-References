---
title: HtmlSaveOptions.ExportPageMargins
second_title: Справочник по API Aspose.Words для .NET
description: HtmlSaveOptions свойство. Указывает экспортируются ли поля страницы в HTML MHTML или EPUB. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 210
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportPageMargins { get; set; }
```

### Примечания

Aspose.Words по умолчанию не отображает область полей страницы. Если какие-либо элементы полностью или частично обрезаны краем документа, отображаемую область можно расширить с помощью этой опции.

### Примеры

Показывает, как отображать объекты, находящиеся за пределами границ, в выходных HTML-документах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор, чтобы вставить фигуру без переноса.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Отрицательные значения положения фигуры могут привести к тому, что фигура окажется за пределами границ страницы.
// Если мы экспортируем это в HTML, фигура будет выглядеть усеченной.
shape.Left = -150;

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы решить, нужно ли настроить страницу для полного отображения объектов, находящихся за пределами границ.
// Если мы установим для флага «ExportPageMargins» значение «true», фигура будет полностью видна в выходном HTML.
// Если мы установим флаг «ExportPageMargins» в значение «false»,
// наш документ будет отображать усеченную форму, как мы видим ее в Microsoft Word.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageMargins = exportPageMargins };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageMargins.html");

if (exportPageMargins)
{
    Assert.True(outDocContents.Contains("<style type=\"text/css\">div.Section_1 { margin:70.85pt }</style>"));
    Assert.True(outDocContents.Contains("<div class=\"Section_1\"><p style=\"margin-top:0pt; margin-left:150pt; margin-bottom:0pt\">"));
}
else
{
    Assert.False(outDocContents.Contains("style type=\"text/css\">"));
    Assert.True(outDocContents.Contains("<div><p style=\"margin-top:0pt; margin-left:220.85pt; margin-bottom:0pt\">"));
}
```

### Смотрите также

* class [HtmlSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlsaveoptions/)
* сборка [Aspose.Words](../../../)


