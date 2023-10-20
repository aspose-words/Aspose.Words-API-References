---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words для .NET
description: ImageData ImageType свойство. Получает тип изображения на С#.
type: docs
weight: 140
url: /ru/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Получает тип изображения.

```csharp
public ImageType ImageType { get; }
```

## Примеры

Показывает, как извлечь изображения из документа и сохранить их в локальной файловой системе как отдельные файлы.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Получаем коллекцию фигур из документа,
// и сохраняем данные изображения каждой формы с изображением в виде файла в локальной файловой системе.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Данные изображений фигур могут содержать изображения многих возможных форматов изображений.
        // Мы можем автоматически определить расширение файла для каждого изображения в зависимости от его формата.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Смотрите также

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
