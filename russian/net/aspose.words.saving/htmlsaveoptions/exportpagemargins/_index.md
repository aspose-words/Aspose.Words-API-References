---
title: HtmlSaveOptions.ExportPageMargins
linktitle: ExportPageMargins
articleTitle: ExportPageMargins
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlSaveOptions ExportPageMargins улучшает экспорт HTML, MHTML и EPUB, управляя полями страницы для безупречного представления.
type: docs
weight: 210
url: /ru/net/aspose.words.saving/htmlsaveoptions/exportpagemargins/
---
## HtmlSaveOptions.ExportPageMargins property

Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool ExportPageMargins { get; set; }
```

## Примечания

Aspose.Words по умолчанию не отображает область полей страницы. Если какие-либо элементы полностью или частично обрезаны краем документа, отображаемую область можно расширить с помощью этой опции.

## Примеры

Показывает, как отображать выходящие за пределы области объекты в выходных HTML-документах.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Используйте конструктор для вставки фигуры без обтекания.
Shape shape = builder.InsertShape(ShapeType.Cube, 200, 200);

shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.WrapType = WrapType.None;

// Отрицательные значения положения фигуры могут поместить фигуру за пределы границ страницы.
// Если мы экспортируем это в HTML, форма будет выглядеть обрезанной.
shape.Left = -150;

// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы решить, следует ли настроить страницу для полного отображения объектов, выходящих за пределы экрана.
// Если установить флаг «ExportPageMargins» в значение «true», фигура будет полностью видна в выходном HTML.
// Если мы установим флаг "ExportPageMargins" на "false",
// наш документ будет отображать обрезанную форму, как мы видим ее в Microsoft Word.
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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
