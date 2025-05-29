---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words для .NET
description: Откройте для себя мощь метода ToImage в ImageData, чтобы легко извлекать изображения, хранящиеся в фигурах, как объекты Image. Улучшайте свои проекты без усилий!
type: docs
weight: 230
url: /ru/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Получает изображение, сохраненное в форме какImage объект.

```csharp
public Image ToImage()
```

## Примечания

НовыйImage объект создается каждый раз при вызове этого метода.

Ответственность за утилизацию объекта изображения лежит на вызывающем объекте.

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
