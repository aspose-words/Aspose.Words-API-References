---
title: HtmlFixedSaveOptions.PageMargins
second_title: Справочник по API Aspose.Words для .NET
description: HtmlFixedSaveOptions свойство. Определяет поля вокруг страниц в документе HTML. Значение полей измеряется в пунктах и должно быть равно или больше 0. Значение по умолчанию  10 пунктов.
type: docs
weight: 120
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Определяет поля вокруг страниц в документе HTML. Значение полей измеряется в пунктах и должно быть равно или больше 0. Значение по умолчанию — 10 пунктов.

```csharp
public double PageMargins { get; set; }
```

### Примечания

Зависит от значения[`PageHorizontalAlignment`](../pagehorizontalalignment/) имущество:

* Определяет верхнее, нижнее и левое поля страницы, если значениеLeft .
* Определяет верхнее, нижнее и правое поля страницы, если значениеRight .
* Определяет верхнее и нижнее поля страницы, если значениеCenter .

### Примеры

Показывает, как настроить поля страницы при сохранении документа в формате HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### Смотрите также

* class [HtmlFixedSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* сборка [Aspose.Words](../../../)


