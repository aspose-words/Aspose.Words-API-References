---
title: FileFormatUtil.ImageTypeToExtension
linktitle: ImageTypeToExtension
articleTitle: ImageTypeToExtension
second_title: Aspose.Words для .NET
description: Конвертируйте типы изображений Aspose.Words в расширения файлов без усилий с помощью метода FileFormatUtil. Получайте точные, строчные расширения за считанные секунды!
type: docs
weight: 50
url: /ru/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Преобразует перечислимое значение типа изображения Aspose.Words в расширение файла. Возвращаемое расширение — это строка в нижнем регистре с точкой в начале.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | Выдает, когда не может конвертировать. |

## Примеры

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

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
