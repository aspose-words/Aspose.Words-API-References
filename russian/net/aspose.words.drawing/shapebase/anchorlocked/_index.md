---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words для .NET
description: ShapeBase AnchorLocked свойство. Указывает заблокирована ли привязка фигуры на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Указывает, заблокирована ли привязка фигуры.

```csharp
public bool AnchorLocked { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

Имеет эффект только для фигур верхнего уровня.

Это свойство влияет на поведение привязки фигуры в Microsoft Word. Если привязка не заблокирована, перемещение фигуры в Microsoft Word может также переместить привязку фигуры.

## Примеры

Показывает, как заблокировать или разблокировать привязку абзаца фигуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Установите для свойства «AnchorLocked» значение «true», чтобы предотвратить привязку фигуры
// от перемещения при перемещении фигуры в Microsoft Word.
// Установите для свойства «AnchorLocked» значение «false», чтобы разрешить любое перемещение фигуры
// чтобы также переместить привязку к любому другому абзацу, к которому приближается фигура.
shape.AnchorLocked = anchorLocked;

// Если слева от фигуры нет видимого символа привязки,
// нам нужно будет включить видимые привязки через «Параметры» -> gt; «Дисплей» -> «Якоря объекта».
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Смотрите также

* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
