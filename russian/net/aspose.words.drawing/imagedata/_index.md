---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.ImageData сорт. Определяет изображение для фигуры на С#.
type: docs
weight: 1060
url: /ru/net/aspose.words.drawing/imagedata/
---
## ImageData class

Определяет изображение для фигуры.

Чтобы узнать больше, посетите[Работа с изображениями](https://docs.aspose.com/words/net/working-with-images/) статья документации.

```csharp
public class ImageData
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Определяет, будет ли изображение отображаться в черно-белом режиме. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Получает коллекцию границ изображения. Границы действуют только для встроенных изображений. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Получает или задает яркость изображения. Значение этого свойства должно быть числом от 0,0 (самый тусклый) до 1,0 (самый яркий). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Определяет значение цвета изображения, которое будет считаться прозрачным. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Получает или задает контрастность указанного изображения. Значение для этого свойства должно быть числом от 0,0 (наименьший контраст) до 1,0 (наибольший контраст). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Определяет долю удаления изображения с нижней стороны. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Определяет долю удаления изображения с левой стороны. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Определяет долю удаления изображения с правой стороны. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Определяет долю удаления изображения с верхней стороны. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Определяет, будет ли изображение отображаться в режиме оттенков серого. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Возвращает`истинный` если фигура содержит байты изображения или связывает изображение. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Получает или задает необработанные байты изображения, хранящегося в форме. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Получает информацию о размере и разрешении изображения. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Получает тип изображения. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Возвращает`истинный` если изображение связано с фигурой (когда[`SourceFullName`](./sourcefullname/) указан). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Возвращает`истинный` если изображение связано и не сохранено в документе. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Получает или задает путь и имя исходного файла связанного изображения. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Определяет заголовок изображения. |

## Методы

| Имя | Описание |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Сохраняет изображение в указанный поток. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Сохраняет изображение в файл. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Устанавливает изображение, отображаемое фигурой. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Устанавливает изображение, отображаемое фигурой. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Устанавливает изображение, отображаемое фигурой. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Возвращает байты изображения для любого изображения независимо от того, сохранено оно или связано с ним. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Получает изображение, хранящееся в фигуре в видеImage объект. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Создает и возвращает поток, содержащий байты изображения. |

## Примечания

Использовать[`ImageData`](../shape/imagedata/) свойство для доступа и изменения изображения внутри фигуры. Вы не создаете экземпляры`ImageData` класс напрямую.

Изображение может храниться внутри фигуры, быть связано с внешним файлом или и то, и другое (связано и сохранено в документе).

Независимо от того, хранится ли изображение внутри фигуры или связано с ним, вы всегда можете получить доступ к изображению fact , используя метод[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) или[`Save`](./save/) методы. Если изображение хранится внутри фигуры, вы также можете получить к нему прямой доступ с помощью[`ImageBytes`](./imagebytes/) свойство.

Чтобы сохранить изображение внутри фигуры, используйте[`SetImage`](./setimage/) метод. Чтобы связать изображение с фигурой, установите[`SourceFullName`](./sourcefullname/) свойство.

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
