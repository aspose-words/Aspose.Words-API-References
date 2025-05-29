---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words для .NET
description: Узнайте, как свойство TextBox LayoutFlow улучшает компоновку текста в фигурах, повышая гибкость дизайна и читабельность ваших проектов.
type: docs
weight: 60
url: /ru/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Определяет поток текста в макете фигуры.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## Примечания

Значение по умолчанию:Horizontal.

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

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
