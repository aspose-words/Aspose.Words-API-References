---
title: ImageData.ImageBytes
second_title: Справочник по API Aspose.Words для .NET
description: ImageData свойство. Получает или задает необработанные байты изображения хранящегося в форме.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Получает или задает необработанные байты изображения, хранящегося в форме.

```csharp
public byte[] ImageBytes { get; set; }
```

### Примечания

Установка значения`нулевой` или пустой массив удалит изображение из фигуры.

Возврат`нулевой` если изображение не сохранено в документе (например, в этом случае изображение, вероятно, связано).

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


