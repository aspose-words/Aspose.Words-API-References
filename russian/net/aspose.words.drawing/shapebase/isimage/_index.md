---
title: ShapeBase.IsImage
linktitle: IsImage
articleTitle: IsImage
second_title: Aspose.Words для .NET
description: Узнайте, является ли фигура изображением, с помощью свойства IsImage ShapeBase. Легко определяйте формы изображения для повышения гибкости и функциональности дизайна.
type: docs
weight: 300
url: /ru/net/aspose.words.drawing/shapebase/isimage/
---
## ShapeBase.IsImage property

Возврат`истинный` если эта форма является формой изображения.

```csharp
public bool IsImage { get; }
```

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

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
