---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentBase BackgroundShape, легко настройте форму фона вашего документа для улучшения визуальной привлекательности. Максимизируйте свой дизайнерский потенциал!
type: docs
weight: 10
url: /ru/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Получает или задает форму фона документа. Может быть`нулевой` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Примечания

Microsoft Word допускает только ту форму, которая имеет свой[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) свойство equal дляRectangle для использования в качестве фоновой формы для документа.

Microsoft Word поддерживает только свойства заливки фоновой фигуры. Все остальные свойства игнорируются.

Установка этого свойства в ненулевое значение также установит[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) к`истинный`.

## Примеры

Показывает, как задать форму фона для каждой страницы документа.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// Единственный тип фигуры, который мы можем использовать в качестве фона — это прямоугольник.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Есть два способа использовать эту фигуру в качестве фона страницы.
// 1 - Плоский цвет:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Изображение:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Измените внешний вид изображения, чтобы оно больше подходило для использования в качестве водяного знака.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word не поддерживает фигуры с изображениями в качестве фона,
// но мы все еще можем видеть эти фоны в других форматах сохранения, таких как .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Смотрите также

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
