---
title: Story.LastParagraph
second_title: Справочник по API Aspose.Words для .NET
description: Story свойство. Получает последний абзац истории.
type: docs
weight: 20
url: /ru/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Получает последний абзац истории.

```csharp
public Paragraph LastParagraph { get; }
```

### Примеры

Показывает, как переместить позицию курсора DocumentBuilder в указанный узел.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// В конструкторе документов есть курсор, который действует как часть документа
// где построитель добавляет новые узлы, когда мы используем его методы построения документа.
// Этот курсор работает так же, как мигающий курсор Microsoft Word,
// и он также всегда заканчивается сразу после любого узла, который только что вставил построитель.
// Чтобы добавить контент в другую часть документа,
// мы можем переместить курсор в другой узел с помощью метода «MoveTo».
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Курсор теперь находится перед узлом, в который мы его переместили.
// Добавление второго запуска вставит его перед первым запуском.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Переместите курсор в конец документа, чтобы продолжить добавление текста в конец, как и раньше.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Смотрите также

* class [Paragraph](../../paragraph/)
* class [Story](../)
* пространство имен [Aspose.Words](../../story/)
* сборка [Aspose.Words](../../../)


