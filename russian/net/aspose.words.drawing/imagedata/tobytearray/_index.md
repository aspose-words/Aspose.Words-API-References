---
title: ImageData.ToByteArray
second_title: Справочник по API Aspose.Words для .NET
description: ImageData метод. Возвращает байты изображения для любого изображения независимо от того сохранено оно или связано с ним.
type: docs
weight: 220
url: /ru/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Возвращает байты изображения для любого изображения независимо от того, сохранено оно или связано с ним.

```csharp
public byte[] ToByteArray()
```

### Примечания

Если изображение связано, загружает изображение при каждом вызове.

### Примеры

Показывает, как создать файл изображения из необработанных данных изображения фигуры.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() возвращает массив, хранящийся в свойстве ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Сохраняем данные изображения фигуры в файл изображения в локальной файловой системе.
using (Stream imgStream = imgShape.ImageData.ToStream())
{
    using (FileStream outStream = new FileStream(ArtifactsDir + "Drawing.GetDataFromImage.png",
        FileMode.Create, FileAccess.ReadWrite))
    {
        imgStream.CopyTo(outStream);
    }
}
```

### Смотрите также

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../imagedata/)
* сборка [Aspose.Words](../../../)


