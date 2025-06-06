---
title: ImageData.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words для .NET
description: Конвертируйте любое изображение в массив байтов без усилий с помощью метода ImageData ToByteArray. Легко получайте доступ к байтам изображения из сохраненных или связанных источников!
type: docs
weight: 220
url: /ru/net/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData.ToByteArray method

Возвращает байты изображения для любого изображения независимо от того, сохранено ли изображение или связано с ним.

```csharp
public byte[] ToByteArray()
```

## Примечания

Если изображение связано, загружает его при каждом вызове.

## Примеры

Показывает, как создать файл изображения из необработанных данных изображения фигуры.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape imgShape = (Shape) imgSourceDoc.GetChild(NodeType.Shape, 0, true);

Assert.True(imgShape.HasImage);

// ToByteArray() возвращает массив, хранящийся в свойстве ImageBytes.
Assert.AreEqual(imgShape.ImageData.ImageBytes, imgShape.ImageData.ToByteArray());

// Сохраняем данные изображения фигуры в файле изображения в локальной файловой системе.
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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
