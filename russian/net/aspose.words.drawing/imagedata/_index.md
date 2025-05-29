---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.ImageData — ваше решение для определения и управления изображениями в фигурах. Улучшите дизайн вашего документа без усилий!
type: docs
weight: 1390
url: /ru/net/aspose.words.drawing/imagedata/
---
## ImageData class

Определяет изображение для фигуры.

Чтобы узнать больше, посетите[Работа с изображениями](https://docs.aspose.com/words/net/working-with-images/) документальная статья.

```csharp
public class ImageData
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Определяет, будет ли изображение отображаться в черно-белом варианте. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Получает коллекцию границ изображения. Границы действуют только для встроенных изображений. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Возвращает или задает яркость изображения. Значение этого свойства должно быть числом от 0,0 (самый тусклый) до 1,0 (самый яркий). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Определяет значение цвета изображения, которое будет считаться прозрачным. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Возвращает или задает контрастность для указанного изображения. Значение для этого свойства должно быть числом от 0,0 (наименьший контраст) до 1,0 (наибольший контраст). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Определяет долю удаления изображения с нижней стороны. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Определяет долю удаления изображения с левой стороны. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Определяет долю удаления изображения с правой стороны. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Определяет долю удаления изображения с верхней стороны. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Определяет, будет ли изображение отображаться в оттенках серого. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Возврат`истинный` если форма имеет байты изображения или ссылается на изображение. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Возвращает или задает необработанные байты изображения, сохраненного в форме. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Получает информацию о размере и разрешении изображения. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Получает тип изображения. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Возврат`истинный` если изображение связано с формой (когда[`SourceFullName`](./sourcefullname/) указано). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Возврат`истинный` если изображение связано и не сохранено в документе. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Возвращает или задает путь и имя исходного файла для связанного изображения. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Определяет заголовок изображения. |

## Методы

| Имя | Описание |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | Подгоняет данные изображения под фрейм Shape таким образом, чтобы соотношение сторон данных изображения соответствовало соотношению сторон фрейма Shape. |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Сохраняет изображение в указанный поток. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Сохраняет изображение в файл. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Устанавливает изображение, которое отображает фигура. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Устанавливает изображение, которое отображает фигура. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Устанавливает изображение, которое отображает фигура. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Возвращает байты изображения для любого изображения независимо от того, сохранено ли изображение или связано с ним. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Получает изображение, сохраненное в форме какImage объект. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Создает и возвращает поток, содержащий байты изображения. |

## Примечания

Используйте[`ImageData`](../shape/imagedata/)свойство для доступа и изменения изображения внутри фигуры. Вы не создаете экземпляры`ImageData` класс напрямую.

Изображение может храниться внутри фигуры, быть связано с внешним файлом или иметь и то, и другое (связано и сохранено в документе).

Независимо от того, хранится ли изображение внутри фигуры или связано с ней, вы всегда можете получить доступ к изображению actual с помощью[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) или[`Save`](./save/) methods. Если изображение хранится внутри фигуры, вы также можете получить к нему прямой доступ с помощью[`ImageBytes`](./imagebytes/) свойство.

Чтобы сохранить изображение внутри фигуры, используйте[`SetImage`](./setimage/) метод. Чтобы связать изображение с фигурой, установите[`SourceFullName`](./sourcefullname/) свойство.

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

Показывает, как вставить связанное изображение в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Ниже приведены два способа применения изображения к фигуре, чтобы она могла его отобразить.
// 1 — Установить форму, содержащую изображение.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Каждое изображение, которое мы сохраняем в форме, увеличит размер нашего документа.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Установить форму для ссылки на файл изображения в локальной файловой системе.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Ссылки на изображения сэкономят место и приведут к уменьшению размера документа.
// Однако документ может корректно отображать изображение только пока
// файл изображения находится в месте, на которое указывает свойство "SourceFullName" фигуры.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
