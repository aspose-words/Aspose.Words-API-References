---
title: ImageData.ToStream
linktitle: ToStream
articleTitle: ToStream
second_title: Aspose.Words для .NET
description: ImageData ToStream метод. Создает и возвращает поток содержащий байты изображения на С#.
type: docs
weight: 230
url: /ru/net/aspose.words.drawing/imagedata/tostream/
---
## ImageData.ToStream method

Создает и возвращает поток, содержащий байты изображения.

```csharp
public Stream ToStream()
```

## Примечания

Если байты изображения сохранены в фигуре, создается и возвращаетMemoryStream объект.

Если изображение связано и сохранено в файле, открывает файл и возвращаетFileStream объект.

Если изображение связано и хранится по внешнему URL-адресу, загружает файл и возвращаетMemoryStream объект.

Ответственность за удаление объекта потока лежит на вызывающей стороне.

## Примеры

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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
