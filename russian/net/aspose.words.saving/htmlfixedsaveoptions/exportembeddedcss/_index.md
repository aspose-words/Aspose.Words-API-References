---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
second_title: Справочник по API Aspose.Words для .NET
description: HtmlFixedSaveOptions свойство. Указывает следует ли внедрять CSS каскадную таблицу стилей в HTMLдокумент.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Указывает, следует ли внедрять CSS (каскадную таблицу стилей) в HTML-документ.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

### Примеры

Показывает, как определить, где хранить таблицы стилей CSS при экспорте документа в Html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Когда мы экспортируем документ в HTML, Aspose.Words также создаст таблицу стилей CSS для форматирования документа.
// Установка флага «ExportEmbeddedCss» в значение «true» сохраняет таблицу стилей CSS в файл .css,
// и ссылка на файл из html-документа с помощью <link> элемент.
// Установка флага в значение «false» встроит таблицу стилей CSS в документ Html,
// который создаст только один файл вместо двух.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* сборка [Aspose.Words](../../../)


