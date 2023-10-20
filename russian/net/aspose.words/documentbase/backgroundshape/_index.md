---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words для .NET
description: DocumentBase BackgroundShape свойство. Получает или задает форму фона документа. Возможнонулевой  на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Получает или задает форму фона документа. Возможно`нулевой` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Примечания

Microsoft Word допускает только форму, имеющую[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) свойство Equal дляRectangle для использования в качестве фоновой фигуры для документа.

Microsoft Word поддерживает только свойства заливки фоновой фигуры. Все остальные свойства игнорируются.

Установка для этого свойства значения, отличного от NULL, также установит[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) к`истинный`.

## Примеры

Показывает, как установить форму фона для каждой страницы документа.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// Единственный тип фигуры, который мы можем использовать в качестве фона, — это прямоугольник.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Есть два способа использования этой фигуры в качестве фона страницы.
// 1 - Плоский цвет:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Изображение:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Настройте внешний вид изображения, чтобы оно лучше подходило в качестве водяного знака.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word не поддерживает фигуры с изображениями в качестве фона,
// но мы все равно можем увидеть эти фоны в других форматах сохранения, таких как .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
