---
title: Shape.LastParagraph
second_title: Справочник по API Aspose.Words для .NET
description: Shape свойство. Получает последний абзац фигуры.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Получает последний абзац фигуры.

```csharp
public Paragraph LastParagraph { get; }
```

### Примеры

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

// Установите свойство LayoutFlow, чтобы задать ориентацию текстового содержимого этого текстового поля.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Смотрите также

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


