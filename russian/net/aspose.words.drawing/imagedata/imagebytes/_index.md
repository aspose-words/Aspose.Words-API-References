---
title: ImageData.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageData ImageBytes, позволяющее легко управлять и манипулировать необработанными байтами изображения в ваших фигурах для улучшения визуального контента.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/imagedata/imagebytes/
---
## ImageData.ImageBytes property

Возвращает или задает необработанные байты изображения, сохраненного в форме.

```csharp
public byte[] ImageBytes { get; set; }
```

## Примечания

Установка значения`нулевой` или пустой массив удалит изображение из формы.

Возвраты`нулевой` если изображение не сохранено в документе (например, в этом случае изображение, вероятно, связано).

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
