---
title: SetImage
second_title: Справочник по API Aspose.Words для .NET
description: Устанавливает изображение отображаемое фигурой.
type: docs
weight: 200
url: /ru/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(Image) {#setimage}

Устанавливает изображение, отображаемое фигурой.

```csharp
public void SetImage(Image image)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | Image | Объект изображения. |

### Примеры

Показывает, как отображать изображения из локальной файловой системы в документе.

```csharp
Document doc = new Document();

 // Чтобы отобразить изображение в документе, нам нужно создать shape
 // который будет содержать изображение, а затем добавить его в тело документа.
Shape imgShape;

 // Ниже приведены два способа получения изображения из файла в локальной файловой системе.
 // 1 - Создать объект изображения из файла изображения: 
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

 // 2 - Открыть файл изображения из локальной файловой системы с помощью потока: 
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Смотрите также

* class [ImageData](../../imagedata)
* namespace [Aspose.Words.Drawing](../../imagedata)
* assembly [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Устанавливает изображение, отображаемое фигурой.

```csharp
public void SetImage(Stream stream)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | Stream | Поток, содержащий изображение. |

### Примеры

Показывает, как отображать изображения из локальной файловой системы в документе.

```csharp
Document doc = new Document();

 // Чтобы отобразить изображение в документе, нам нужно создать shape
 // который будет содержать изображение, а затем добавить его в тело документа.
Shape imgShape;

 // Ниже приведены два способа получения изображения из файла в локальной файловой системе.
 // 1 - Создать объект изображения из файла изображения: 
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

 // 2 - Открыть файл изображения из локальной файловой системы с помощью потока: 
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Смотрите также

* class [ImageData](../../imagedata)
* namespace [Aspose.Words.Drawing](../../imagedata)
* assembly [Aspose.Words](../../../)

---

## SetImage(string) {#setimage_2}

Устанавливает изображение, отображаемое фигурой.

```csharp
public void SetImage(string fileName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Файл изображения. Может быть именем файла или URL-адресом. |

### Примеры

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

* class [ImageData](../../imagedata)
* namespace [Aspose.Words.Drawing](../../imagedata)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
