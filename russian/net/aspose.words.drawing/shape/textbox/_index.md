---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words для .NET
description: Настройте свойства Shape TextBox, чтобы улучшить отображение текста и повысить визуальную привлекательность ваших проектов. Раскройте творческий потенциал сегодня!
type: docs
weight: 230
url: /ru/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Определяет атрибуты, которые указывают, как текст отображается в форме.

```csharp
public TextBox TextBox { get; }
```

## Примеры

Показывает, как задать ориентацию текста внутри текстового поля.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Переместите конструктор документов внутрь TextBox и добавьте текст.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Установите свойство "LayoutFlow", чтобы задать ориентацию текстового содержимого этого текстового поля.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Смотрите также

* class [TextBox](../../textbox/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
