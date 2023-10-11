---
title: ImageData.ToImage
second_title: Справочник по API Aspose.Words для .NET
description: ImageData метод. Получает изображение хранящееся в фигуре в видеImage объект.
type: docs
weight: 230
url: /ru/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Получает изображение, хранящееся в фигуре в видеImage объект.

```csharp
public Image ToImage()
```

### Примечания

новыйImage объект создается каждый раз при вызове этого метода.

Ответственность за удаление объекта изображения лежит на вызывающем объекте.

### Примеры

Показывает, как сохранить все изображения из документа в файловую систему.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Фигуры с установленным флагом HasImage хранят и отображают все изображения документа.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Проходим каждую фигуру и сохраняем ее изображение.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### Смотрите также

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../imagedata/)
* сборка [Aspose.Words](../../../)


