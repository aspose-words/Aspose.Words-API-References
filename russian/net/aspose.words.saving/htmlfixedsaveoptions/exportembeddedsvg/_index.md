---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ExportEmbeddedSvg HtmlFixedSaveOptions, легко встраивайте ресурсы SVG в свои HTML-документы для улучшения визуальных эффектов. По умолчанию — true.
type: docs
weight: 70
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Указывает, следует ли встраивать ресурсы SVG в документ HTML. Значение по умолчанию:`истинный` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Примеры

Показывает, как определить, где хранить объекты SVG при экспорте документа в HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Когда мы экспортируем документ с объектами SVG в .html,
// Aspose.Words может размещать эти объекты в двух возможных местах.
// Установка флага «ExportEmbeddedSvg» в значение «true» приведет к внедрению всех необработанных данных объекта SVG
// внутри выходного HTML, внутри тегов <image>.
// Установка этого флага в значение «false» создаст файл в локальной файловой системе для каждого объекта SVG.
// HTML будет ссылаться на каждый файл, используя атрибут «data» тега <object>.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
