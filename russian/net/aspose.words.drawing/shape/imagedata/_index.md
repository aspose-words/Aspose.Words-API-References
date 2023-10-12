---
title: Shape.ImageData
second_title: Справочник по API Aspose.Words для .NET
description: Shape свойство. Предоставляет доступ к изображению фигуры. Возвращаетнулевой если фигура не может иметь изображение.
type: docs
weight: 110
url: /ru/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Предоставляет доступ к изображению фигуры. Возвращает`нулевой` если фигура не может иметь изображение.

```csharp
public ImageData ImageData { get; }
```

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

Показывает, как вставить связанное изображение в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Ниже приведены два способа применения изображения к фигуре для ее отображения.
// 1 — установить форму, в которой будет находиться изображение.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Каждое изображение, которое мы сохраняем в shape, увеличивает размер нашего документа.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 — Установить форму для связи с файлом изображения в локальной файловой системе.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Ссылки на изображения сэкономят место и приведут к уменьшению размера документа.
// Однако документ может правильно отображать изображение только тогда, когда
// файл изображения находится в том месте, на которое указывает свойство SourceFullName фигуры.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Смотрите также

* class [ImageData](../../imagedata/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


