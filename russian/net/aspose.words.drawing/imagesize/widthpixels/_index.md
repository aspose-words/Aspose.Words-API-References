---
title: ImageSize.WidthPixels
linktitle: WidthPixels
articleTitle: WidthPixels
second_title: Aspose.Words для .NET
description: ImageSize WidthPixels свойство. Получает ширину изображения в пикселях на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/imagesize/widthpixels/
---
## ImageSize.WidthPixels property

Получает ширину изображения в пикселях.

```csharp
public int WidthPixels { get; }
```

## Примеры

Показывает, как читать свойства изображения в фигуре.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем в документ фигуру, содержащую изображение, взятое из нашей локальной файловой системы.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Если фигура содержит изображение, ее свойство ImageData будет действительным,
// и он будет содержать объект ImageSize.
ImageSize imageSize = shape.ImageData.ImageSize; 

// Объект ImageSize содержит доступную только для чтения информацию об изображении внутри фигуры.
Assert.AreEqual(400, imageSize.HeightPixels);
Assert.AreEqual(400, imageSize.WidthPixels);

const double delta = 0.05;
Assert.AreEqual(95.98d, imageSize.HorizontalResolution, delta);
Assert.AreEqual(95.98d, imageSize.VerticalResolution, delta);

// Мы можем основывать размер фигуры на размере ее изображения, чтобы избежать растягивания изображения.
shape.Width = imageSize.WidthPoints * 2;
shape.Height = imageSize.HeightPoints * 2;

doc.Save(ArtifactsDir + "Drawing.ImageSize.docx");
```

### Смотрите также

* class [ImageSize](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
