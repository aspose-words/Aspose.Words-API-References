---
title: ShapeBase.IsInline
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Быстрый способ определить расположена ли эта фигура на одной линии с текстом.
type: docs
weight: 280
url: /ru/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Быстрый способ определить, расположена ли эта фигура на одной линии с текстом.

```csharp
public bool IsInline { get; }
```

### Примечания

Имеет эффект только для фигур верхнего уровня.

### Примеры

Показывает, как определить, является ли фигура встроенной или плавающей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два типа обтекания, которые могут иметь фигуры.
// 1 - Встроенный:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Встроенная фигура находится внутри абзаца среди других элементов абзаца, например фрагментов текста.
// В Microsoft Word мы можем щелкнуть и перетащить фигуру в любой абзац, как если бы это был символ.
// Если фигура большая, это повлияет на расстояние между абзацами по вертикали.
// Мы не можем переместить эту фигуру в место без абзаца.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Плавающий:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Плавающая фигура принадлежит абзацу, в который мы ее вставляем,
// который мы можем определить по символу привязки, который появляется, когда мы щелкаем фигуру.
// Если фигура не имеет видимого символа привязки слева от нее,
// нам нужно включить видимые якоря через "Опции" -> "Дисплей" -> «Якоря объекта».
// В Microsoft Word мы можем щелкнуть левой кнопкой мыши и свободно перетащить эту фигуру в любое место.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


