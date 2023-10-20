---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: ImageData Save метод. Сохраняет изображение в указанный поток на С#.
type: docs
weight: 190
url: /ru/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Сохраняет изображение в указанный поток.

```csharp
public void Save(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, в который сохраняется изображение. |

## Примечания

Ответственность за удаление объекта потока лежит на вызывающей стороне.

## Примеры

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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Сохраняет изображение в файл.

```csharp
public void Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла, в котором нужно сохранить изображение. |

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

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
