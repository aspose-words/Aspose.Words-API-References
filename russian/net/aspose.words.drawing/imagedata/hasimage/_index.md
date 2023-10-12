---
title: ImageData.HasImage
second_title: Справочник по API Aspose.Words для .NET
description: ImageData свойство. Возвращаетистинный если фигура содержит байты изображения или связывает изображение.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Возвращает`истинный` если фигура содержит байты изображения или связывает изображение.

```csharp
public bool HasImage { get; }
```

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


