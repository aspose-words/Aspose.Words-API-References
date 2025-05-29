---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words для .NET
description: Воспользуйтесь свойством LastParagraph, чтобы легко извлечь последний абзац в форме, улучшив макет и читабельность документа.
type: docs
weight: 130
url: /ru/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Получает последний абзац в форме.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
