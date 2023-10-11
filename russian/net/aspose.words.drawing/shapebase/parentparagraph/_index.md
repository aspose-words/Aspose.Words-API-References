---
title: ShapeBase.ParentParagraph
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase свойство. Возвращает непосредственный родительский абзац.
type: docs
weight: 410
url: /ru/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Возвращает непосредственный родительский абзац.

```csharp
public Paragraph ParentParagraph { get; }
```

### Примечания

Для дочерних фигур фигуры группы и дочерних фигур объекта Office Math всегда возвращается`нулевой`.

### Примеры

Показывает, как вставить текстовое поле и установить шрифт его содержимого.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Установите для свойства «Скрытый» объекта «Шрифт» фигуры значение «истина», чтобы скрыть текстовое поле из поля зрения.
// и свернуть пространство, которое он обычно занимает.
// Установите для свойства «Скрытый» объекта «Шрифт» фигуры значение «false», чтобы текстовое поле оставалось видимым.
shape.Font.Hidden = hideShape;

// Если фигура видна, мы изменим ее внешний вид с помощью объекта шрифта.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Перемещаем конструктор из текстового поля обратно в основной документ.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Смотрите также

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


