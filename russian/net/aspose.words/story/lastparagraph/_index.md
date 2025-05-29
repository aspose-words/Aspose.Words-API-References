---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words для .NET
description: Свойство Story LastParagraph позволяет легко получить доступ к последнему абзацу вашей истории, что расширяет возможности управления повествованием и его редактирования.
type: docs
weight: 20
url: /ru/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Получает последний абзац в истории.

```csharp
public Paragraph LastParagraph { get; }
```

## Примеры

Показывает, как переместить позицию курсора DocumentBuilder на указанный узел.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Конструктор документов имеет курсор, который действует как часть документа
// где конструктор добавляет новые узлы, когда мы используем его методы построения документа.
// Этот курсор функционирует так же, как мигающий курсор Microsoft Word,
// и он также всегда оказывается сразу после любого узла, который только что вставил строитель.
// Чтобы добавить содержимое в другую часть документа,
// мы можем переместить курсор на другой узел с помощью метода «MoveTo».
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
