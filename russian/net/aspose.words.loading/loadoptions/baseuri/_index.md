---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LoadOptions BaseUri, чтобы легко преобразовать относительные URI в абсолютные в ваших документах. Улучшите управление URI сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Возвращает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` .

```csharp
public string BaseUri { get; set; }
```

## Примечания

Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1. При загрузке HTML-документа из потока, если документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
2. При сохранении документа в PDF и других форматах для извлечения изображений, связанных с использованием относительных URI , чтобы изображения можно было сохранить в выходном документе.

## Примеры

Показывает, как открыть HTML-документ с изображениями из потока, используя базовый URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Передать URI базовой папки при ее загрузке
    // чтобы можно было найти любые изображения с относительными URI в HTML-документе.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Убедитесь, что первая фигура документа содержит допустимое изображение.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
