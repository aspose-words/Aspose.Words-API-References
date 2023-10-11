---
title: LoadOptions.BaseUri
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Получает или задает строку которая будет использоваться для преобразования относительных URI найденных в документе в абсолютные URI когда это необходимо. Может бытьнулевой или пустая строка. По умолчаниюнулевой .
type: docs
weight: 20
url: /ru/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть`нулевой` или пустая строка. По умолчанию`нулевой` .

```csharp
public string BaseUri { get; set; }
```

### Примечания

Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1. При загрузке HTML-документа из потока документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
2. При сохранении документа в PDF и других форматах для извлечения изображений, связанных с использованием относительных URI , чтобы изображения можно было сохранить в выходной документ.

### Примеры

Показывает, как открыть документ HTML с изображениями из потока, используя базовый URI.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Передаем URI базовой папки при ее загрузке
    // чтобы можно было найти любые изображения с относительными URI в документе HTML.
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
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


