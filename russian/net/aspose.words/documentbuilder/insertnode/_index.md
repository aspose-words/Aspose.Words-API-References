---
title: DocumentBuilder.InsertNode
linktitle: InsertNode
articleTitle: InsertNode
second_title: Aspose.Words для .NET
description: Улучшите создание документов с помощью метода InsertNode в DocumentBuilder. Легко вставляйте узлы перед курсором для бесперебойного редактирования!
type: docs
weight: 410
url: /ru/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Вставляет узел перед курсором.

```csharp
public void InsertNode(Node node)
```

## Примеры

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
