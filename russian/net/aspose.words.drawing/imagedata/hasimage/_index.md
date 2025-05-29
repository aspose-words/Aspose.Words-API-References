---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageData HasImage. Быстро проверяйте, содержит ли фигура байты изображения или ссылки, что улучшит ваш рабочий процесс проектирования без особых усилий.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Возврат`истинный` если форма имеет байты изображения или ссылается на изображение.

```csharp
public bool HasImage { get; }
```

## Примеры

Показывает, как сохранить все изображения из документа в файловой системе.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Фигуры с установленным флагом «HasImage» хранят и отображают все изображения документа.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Пройдитесь по каждой фигуре и сохраните ее изображение.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Смотрите также

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
