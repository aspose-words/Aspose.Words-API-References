---
title: ImageData
second_title: Справочник по API Aspose.Words для .NET
description: Определяет изображение для формы.
type: docs
weight: 930
url: /ru/net/aspose.words.drawing/imagedata/
---
## ImageData class

Определяет изображение для формы.

```csharp
public class ImageData
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel) { get; set; } | Определяет, будет ли изображение отображаться черно-белым. |
| [Borders](../../aspose.words.drawing/imagedata/borders) { get; } | Получает набор границ изображения. Границы действуют только для встроенных изображений. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness) { get; set; } | Получает или устанавливает яркость изображения. Значение этого свойства должно быть числом от 0,0 (самый тусклый) до 1,0 (самый яркий). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey) { get; set; } | Определяет значение цвета изображения, которое будет считаться прозрачным. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast) { get; set; } | Получает или задает контраст для указанного изображения. Значение для этого свойства должно быть числом от 0,0 (наименьший контраст) до 1,0 (наибольший контраст). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom) { get; set; } | Определяет долю удаления изображения с нижней стороны. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft) { get; set; } | Определяет долю удаления изображения с левой стороны. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright) { get; set; } | Определяет долю удаления изображения с правой стороны. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop) { get; set; } | Определяет долю удаления изображения с верхней стороны. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale) { get; set; } | Определяет, будет ли изображение отображаться в оттенках серого. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage) { get; } | Возвращает true, если фигура содержит байты изображения или связывает изображение. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes) { get; set; } | Получает или задает необработанные байты изображения, хранящиеся в форме. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize) { get; } | Получает информацию о размере и разрешении изображения. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype) { get; } | Получает тип изображения. |
| [IsLink](../../aspose.words.drawing/imagedata/islink) { get; } | Возвращает true, если изображение связано с фигурой (когда указано[`SourceFullName`](./sourcefullname)). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly) { get; } | Возвращает true, если изображение связано и не хранится в документе. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname) { get; set; } | Получает или задает путь и имя исходного файла для связанного изображения. |
| [Title](../../aspose.words.drawing/imagedata/title) { get; set; } | Определяет заголовок изображения. |

## Методы

| Имя | Описание |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save#save)(Stream) | Сохраняет изображение в указанный поток. |
| [Save](../../aspose.words.drawing/imagedata/save#save_1)(string) | Сохраняет изображение в файл. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage#setimage)(Image) | Устанавливает изображение, отображаемое фигурой. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage#setimage_1)(Stream) | Устанавливает изображение, отображаемое фигурой. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage#setimage_2)(string) | Устанавливает изображение, отображаемое фигурой. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray)() | Возвращает байты изображения для любого изображения, независимо от того, сохранено ли изображение или связано. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage)() | Получает изображение, хранящееся в форме как объектImage. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream)() | Создает и возвращает поток, содержащий байты изображения. |

### Примечания

Используйте[`ImageData`](../shape/imagedata)свойство для доступа и изменения изображения внутри фигуры. Вы не создаете экземпляры класса[`ImageData`](../imagedata)напрямую.

Изображение может быть сохранено внутри формы, связано с внешним файлом или и то, и другое (связано и сохранено в документе).

Независимо от того, хранится ли изображение внутри формы или связано, вы всегда можете получить доступ к фактическому изображению с помощью[`ToByteArray`](./tobytearray),[`ToStream`](./tostream),[`ToImage`](./toimage)или[`Save`](./save)методы. Если изображение хранится внутри фигуры, вы также можете получить к нему прямой доступ с помощью свойства[`ImageBytes`](./imagebytes).

Чтобы сохранить изображение внутри фигуры, используйте метод[`SetImage`](./setimage). Чтобы связать изображение с фигурой, задайте свойство[`SourceFullName`](./sourcefullname).

### Примеры

Показывает, как извлекать изображения из документа и сохранять их в локальной файловой системе в виде отдельных файлов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Ниже приведены два способа применения изображения к фигуре, чтобы она могла ее отображать.
// 1 - Устанавливаем фигуру для изображения.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Каждое изображение, которое мы храним в форме, увеличивает размер нашего документа.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Установите форму для ссылки на файл изображения в локальной файловой системе.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Ссылка на изображения сэкономит место и приведет к уменьшению размера документа.
// Однако документ может правильно отображать изображение только тогда, когда
// файл изображения находится в месте, на которое указывает свойство SourceFullName фигуры.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

Показывает, как вставить связанное изображение в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Ниже приведены два способа применения изображения к фигуре, чтобы она могла ее отображать.
// 1 - Устанавливаем фигуру для изображения.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Каждое изображение, которое мы храним в форме, увеличивает размер нашего документа.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Установите форму для ссылки на файл изображения в локальной файловой системе.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Ссылка на изображения сэкономит место и приведет к уменьшению размера документа.
// Однако документ может правильно отображать изображение только тогда, когда
// файл изображения находится в месте, на которое указывает свойство SourceFullName фигуры.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
