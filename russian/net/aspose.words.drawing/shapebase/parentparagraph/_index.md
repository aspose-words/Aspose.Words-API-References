---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase ParentParagraph — получите эффективный доступ к непосредственному родительскому абзацу для оптимизированного управления содержимым и улучшенной организации.
type: docs
weight: 430
url: /ru/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Возвращает непосредственный родительский абзац.

```csharp
public Paragraph ParentParagraph { get; }
```

## Примечания

Для дочерних фигур групповой фигуры и дочерних фигур объекта Office Math всегда возвращается`нулевой`.

## Примеры

Показывает, как вставить текстовое поле и задать шрифт его содержимого.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Установите свойство «Скрытый» объекта «Шрифт» фигуры на «истина», чтобы скрыть текстовое поле из виду
// и свернуть пространство, которое он обычно занимает.
// Установите свойство «Скрытый» объекта «Шрифт» фигуры на «ложь», чтобы оставить текстовое поле видимым.
shape.Font.Hidden = hideShape;

// Если фигура видима, мы изменим ее внешний вид с помощью объекта шрифта.
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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
