---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words для .NET
description: Откройте для себя свойство HtmlFixedSaveOptions PageMargins для настройки полей вашего HTML-документа. Задайте значения в пунктах для точного управления макетом.
type: docs
weight: 130
url: /ru/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Задает поля вокруг страниц в документе HTML. Значение полей измеряется в пунктах и должно быть равно или больше 0. Значение по умолчанию — 10 пунктов.

```csharp
public double PageMargins { get; set; }
```

## Примечания

Зависит от стоимости[`PageHorizontalAlignment`](../pagehorizontalalignment/) свойство:

* Определяет верхнее, нижнее и левое поля страницы, если значение равноLeft .
* Определяет верхнее, нижнее и правое поля страницы, если значение равноRight .
* Определяет верхнее и нижнее поля страницы, если значение равноCenter .

## Примеры

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
