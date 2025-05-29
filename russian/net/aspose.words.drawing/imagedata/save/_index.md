---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: Сохраняйте изображения без усилий с помощью метода ImageData Save. Оптимизируйте свой рабочий процесс, легко сохраняя изображения непосредственно в выбранном вами потоке.
type: docs
weight: 200
url: /ru/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Сохраняет изображение в указанный поток.

```csharp
public void Save(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, в который следует сохранить изображение. |

## Примечания

Является ли утилизация потокового объекта обязанностью вызывающей стороны?

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

---

## Save(*string*) {#save_1}

Сохраняет изображение в файл.

```csharp
public void Save(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Имя файла, в котором будет сохранено изображение. |

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

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
