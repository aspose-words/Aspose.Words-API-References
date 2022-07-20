---
title: CropTop
second_title: Справочник по API Aspose.Words для .NET
description: Определяет долю удаления изображения с верхней стороны.
type: docs
weight: 90
url: /ru/net/aspose.words.drawing/imagedata/croptop/
---
## ImageData.CropTop property

Определяет долю удаления изображения с верхней стороны.

```csharp
public double CropTop { get; set; }
```

### Примечания

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию равно 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки формы ). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто на , чтобы соответствовать форме.

Значение по умолчанию — 0.

### Примеры

Показывает, как редактировать данные изображения фигуры.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Импорт фигуры из исходного документа и добавление ее к первому абзацу.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// Импортированная фигура содержит изображение. Мы можем получить доступ к свойствам изображения и необработанным данным через объект ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Если изображение не имеет границ, его объект ImageData определит цвет границы как пустой.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Это изображение не связано с другим файлом фигуры или изображения в локальной файловой системе.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Свойства "Яркость" и "Контрастность" определяют яркость и контрастность изображения
// по шкале от 0 до 1 со значением по умолчанию 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Указанные выше значения яркости и контрастности создали изображение с большим количеством белого.
// Мы можем выбрать цвет с помощью свойства ChromaKey, чтобы заменить его прозрачностью, например, белым.
imageData.ChromaKey = Color.White;

// Снова импортируем исходную форму и делаем изображение монохромным.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Снова импортируйте исходную форму, чтобы создать третье изображение, и установите для него значение BiLevel.
// BiLevel устанавливает для каждого пикселя черный или белый цвет, в зависимости от того, какой из них ближе к исходному цвету.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Обрезка определяется по шкале 0-1. Обрезка стороны на 0,3
// обрезает 30% изображения с обрезанной стороны.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Смотрите также

* class [ImageData](../../imagedata)
* пространство имен [Aspose.Words.Drawing](../../imagedata)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->