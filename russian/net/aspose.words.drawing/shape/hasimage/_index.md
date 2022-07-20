---
title: HasImage
second_title: Справочник по API Aspose.Words для .NET
description: Возвращает true если фигура содержит байты изображения или ссылается на изображение.
type: docs
weight: 80
url: /ru/net/aspose.words.drawing/shape/hasimage/
---
## Shape.HasImage property

Возвращает true, если фигура содержит байты изображения или ссылается на изображение.

```csharp
public bool HasImage { get; }
```

### Примеры

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

// Получить набор фигур из документа,
// и сохранить данные изображения каждой фигуры с изображением в виде файла в локальной файловой системе.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // Данные изображения фигур могут содержать изображения многих возможных форматов изображений. 
        // Мы можем определить расширение файла для каждого изображения автоматически, исходя из его формата.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Смотрите также

* class [Shape](../../shape)
* пространство имен [Aspose.Words.Drawing](../../shape)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->