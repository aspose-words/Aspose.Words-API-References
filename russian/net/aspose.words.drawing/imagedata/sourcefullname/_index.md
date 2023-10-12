---
title: ImageData.SourceFullName
second_title: Справочник по API Aspose.Words для .NET
description: ImageData свойство. Получает или задает путь и имя исходного файла связанного изображения.
type: docs
weight: 170
url: /ru/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Получает или задает путь и имя исходного файла связанного изображения.

```csharp
public string SourceFullName { get; set; }
```

### Примечания

Значение по умолчанию — пустая строка.

Если`SourceFullName` не пустая строка, изображение связано.

### Примеры

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

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../imagedata/)
* сборка [Aspose.Words](../../../)


