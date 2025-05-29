---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words для .NET
description: Узнайте, как свойство HtmlLoadOptions SupportVml улучшает работу с веб-сайтами, включая поддержку изображений VML для улучшения качества графики.
type: docs
weight: 70
url: /ru/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Возвращает или задает значение, указывающее, следует ли поддерживать изображения VML.

```csharp
public bool SupportVml { get; set; }
```

## Примеры

Показывает, как поддерживать условные комментарии при загрузке HTML-документа.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Если значение равно true, то мы учитываем код VML при анализе загруженного документа.
loadOptions.SupportVml = supportVml;

// Этот документ содержит изображение JPEG в тегах "<!--[if gte vml 1]>",
// и другое изображение PNG в тегах "<![if !vml]>".
// Если установить флаг «SupportVml» на «true», то Aspose.Words загрузит JPEG.
// Если мы установим этот флаг на «false», то Aspose.Words загрузит только PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Смотрите также

* class [HtmlLoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
