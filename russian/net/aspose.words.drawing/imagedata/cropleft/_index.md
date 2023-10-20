---
title: ImageData.CropLeft
linktitle: CropLeft
articleTitle: CropLeft
second_title: Aspose.Words для .NET
description: ImageData CropLeft свойство. Определяет долю удаления изображения с левой стороны на С#.
type: docs
weight: 70
url: /ru/net/aspose.words.drawing/imagedata/cropleft/
---
## ImageData.CropLeft property

Определяет долю удаления изображения с левой стороны.

```csharp
public double CropLeft { get; set; }
```

## Примечания

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, , что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезанного края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры ). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто на , чтобы соответствовать форме.

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

// Импортированная фигура содержит изображение. Мы можем получить доступ к свойствам изображения и необработанным данным через объект ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Если изображение не имеет границ, его объект ImageData определит цвет границы как пустой.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Это изображение не связано с другим файлом формы или изображения в локальной файловой системе.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Свойства «Яркость» и «Контрастность» определяют яркость и контрастность изображения.
// по шкале от 0 до 1 со значением по умолчанию 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Приведенные выше значения яркости и контрастности создали изображение с большим количеством белого цвета.
// С помощью свойства ChromaKey мы можем выбрать цвет для замены на прозрачность, например белый.
imageData.ChromaKey = Color.White;

// Снова импортируем исходную форму и установим монохромное изображение.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Снова импортируйте исходную форму, чтобы создать третье изображение, и установите для него значение BiLevel.
// BiLevel устанавливает для каждого пикселя черный или белый цвет, в зависимости от того, какой цвет ближе к исходному.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Обрезка определяется по шкале от 0 до 1. Обрезка стороны на 0,3
// обрежет 30% изображения с обрезанной стороны.
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
