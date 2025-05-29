---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ShapeBase Font для легкого доступа к форматированию шрифтов. Улучшите свои проекты с помощью настраиваемых стилей текста и уникальных параметров типографики.
type: docs
weight: 190
url: /ru/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Предоставляет доступ к форматированию шрифта этого объекта.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
