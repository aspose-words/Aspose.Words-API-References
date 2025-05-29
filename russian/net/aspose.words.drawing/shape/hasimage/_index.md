---
title: Shape.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words для .NET
description: Узнайте, содержит ли фигура данные изображения или ссылки на изображение с помощью свойства HasImage. Улучшайте свои проекты без усилий!
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/shape/hasimage/
---
## Shape.HasImage property

Возврат`истинный` если форма имеет байты изображения или ссылается на изображение.

```csharp
public bool HasImage { get; }
```

## Примеры

Показывает, как удалить все фигуры с изображениями из документа.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Показывает, как извлекать изображения из документа и сохранять их в локальной файловой системе в виде отдельных файлов.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Получить коллекцию фигур из документа,
// и сохранить данные изображения каждой фигуры с изображением в виде файла в локальной файловой системе.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Данные изображений фигур могут содержать изображения многих возможных форматов изображений.
        // Мы можем автоматически определить расширение файла для каждого изображения на основе его формата.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Смотрите также

* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
