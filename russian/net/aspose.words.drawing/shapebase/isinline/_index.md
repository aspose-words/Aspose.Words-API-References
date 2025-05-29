---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase IsInline, которое позволит легко проверить, совпадает ли ваша фигура с текстом, улучшив ваш дизайн и повысив эффективность макета.
type: docs
weight: 310
url: /ru/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Быстрый способ определить, расположена ли эта фигура в одной строке с текстом.

```csharp
public bool IsInline { get; }
```

## Примечания

Действует только для фигур верхнего уровня.

## Примеры

Показывает, как определить, является ли фигура встроенной или плавающей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа обтекания, которые могут быть у фигур.
// 1 - Встроенный:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Встроенная фигура располагается внутри абзаца среди других элементов абзаца, таких как фрагменты текста.
// В Microsoft Word мы можем щелкнуть и перетащить фигуру в любой абзац, как будто это символ.
// Если форма большая, это повлияет на вертикальный интервал между абзацами.
// Мы не можем переместить эту фигуру в место без абзаца.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Плавающий:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Плавающая фигура принадлежит абзацу, в который мы ее вставляем,
// который мы можем определить по символу привязки, появляющемуся при щелчке по фигуре.
// Если слева от фигуры нет видимого символа привязки,
// нам нужно будет включить видимые якоря через «Параметры» -> «Отображение» -> «Якоря объектов».
// В Microsoft Word мы можем щелкнуть левой кнопкой мыши и свободно перетащить эту фигуру в любое место.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
