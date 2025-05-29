---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup PageWidth, позволяющее легко настроить ширину страницы в пунктах, улучшая макет документа для оптимального представления.
type: docs
weight: 340
url: /ru/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

Возвращает или задает ширину страницы в пунктах.

```csharp
public double PageWidth { get; set; }
```

## Примеры

Показывает, как вставить изображение и использовать его в качестве водяного знака.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте изображение в заголовок, чтобы оно было видно на каждой странице.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Разместите изображение в центре страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Показывает, как вставить плавающее изображение и указать его положение и размер.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Настройте свойство "RelativeHorizontalPosition" фигуры для обработки значения свойства "Left"
 // как горизонтальное расстояние фигуры в пунктах от левого края страницы.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Установите горизонтальное расстояние фигуры от левого края страницы на 100.
shape.Left = 100;

// Используйте свойство "RelativeVerticalPosition" аналогичным образом, чтобы расположить фигуру на 80 пунктов ниже верхней части страницы.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Задайте высоту фигуры, которая автоматически масштабирует ширину для сохранения размеров.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Свойства «Bottom» и «Right» содержат нижний и правый края изображения.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Смотрите также

* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
