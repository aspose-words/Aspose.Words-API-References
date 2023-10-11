---
title: FileFormatUtil.ImageTypeToExtension
second_title: Справочник по API Aspose.Words для .NET
description: FileFormatUtil метод. Преобразует перечислимое значение типа изображения Aspose.Words в расширение файла. Возвращаемое расширение представляет собой строку в нижнем регистре с начальной точкой.
type: docs
weight: 50
url: /ru/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Преобразует перечислимое значение типа изображения Aspose.Words в расширение файла. Возвращаемое расширение представляет собой строку в нижнем регистре с начальной точкой.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Выдает, когда невозможно преобразовать. |

### Примеры

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

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../fileformatutil/)
* сборка [Aspose.Words](../../../)


