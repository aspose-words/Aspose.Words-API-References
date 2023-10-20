---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words для .NET
description: HtmlLoadOptions SupportVml свойство. Получает или задает значение указывающее поддерживаются ли изображения VML на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Получает или задает значение, указывающее, поддерживаются ли изображения VML.

```csharp
public bool SupportVml { get; set; }
```

## Примеры

Показывает, как поддерживать условные комментарии при загрузке HTML-документа.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Если значение истинно, то мы учитываем код VML при разборе загруженного документа.
loadOptions.SupportVml = supportVml;

// Этот документ содержит изображение JPEG внутри "<!--[if gte vml 1]>" теги,
// и другое изображение PNG внутри "<![if !vml]>" теги.
// Если мы установим для флага «SupportVml» значение «true», тогда Aspose.Words загрузит JPEG.
// Если мы установим для этого флага значение «false», то Aspose.Words будет загружать только PNG.
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
