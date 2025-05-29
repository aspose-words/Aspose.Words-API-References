---
title: ImageData.ChromaKey
linktitle: ChromaKey
articleTitle: ChromaKey
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ImageData ChromaKey, установите прозрачные цвета для своих изображений и улучшите визуальные эффекты без усилий. Откройте для себя творческие возможности!
type: docs
weight: 40
url: /ru/net/aspose.words.drawing/imagedata/chromakey/
---
## ImageData.ChromaKey property

Определяет значение цвета изображения, которое будет считаться прозрачным.

```csharp
public Color ChromaKey { get; set; }
```

## Примечания

Значение по умолчанию — 0.

## Примеры

Показывает, как редактировать данные изображения фигуры.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Импортируем фигуру из исходного документа и добавляем ее в первый абзац.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// Импортированная форма содержит изображение. Мы можем получить доступ к свойствам изображения и необработанным данным через объект ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Если изображение не имеет границ, его объект ImageData определит цвет границы как пустой.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Это изображение не ссылается на другой файл фигуры или изображения в локальной файловой системе.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Свойства «Яркость» и «Контрастность» определяют яркость и контрастность изображения
// по шкале от 0 до 1, со значением по умолчанию 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Приведенные выше значения яркости и контрастности создали изображение с большим количеством белого цвета.
// Мы можем выбрать цвет с помощью свойства ChromaKey для замены на прозрачность, например белый.
imageData.ChromaKey = Color.White;

// Импортируем исходную форму еще раз и делаем изображение монохромным.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Импортируем исходную форму еще раз, чтобы создать третье изображение и задать для него режим BiLevel.
// BiLevel устанавливает для каждого пикселя либо черный, либо белый цвет, в зависимости от того, какой из них ближе к исходному цвету.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Кадрирование определяется по шкале от 0 до 1. Кадрирование стороны на 0,3
// обрежет 30% изображения по обрезанной стороне.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Смотрите также

* class [ImageData](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
