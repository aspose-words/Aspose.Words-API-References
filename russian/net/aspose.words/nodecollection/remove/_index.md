---
title: NodeCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words для .NET
description: С легкостью удаляйте узлы из документа с помощью метода NodeCollection Remove, оптимизируя управление данными и повышая производительность.
type: docs
weight: 90
url: /ru/net/aspose.words/nodecollection/remove/
---
## NodeCollection.Remove method

Удаляет узел из коллекции и из документа.

```csharp
public void Remove(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел, который необходимо удалить. |

## Примеры

Показывает, как работать с NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте текст в документ, вставив Runs с помощью DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Каждый вызов метода «Write» создает новый Run,
// который затем появляется в RunCollection родительского Paragraph.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Мы также можем вставить узел в RunCollection вручную.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Доступ к отдельным фрагментам и их удаление для удаления их текста из документа.
Run run = runs[1];
runs.Remove(run);

Assert.AreEqual("Run 1. Run 3.", doc.GetText().Trim());
Assert.NotNull(run);
Assert.False(runs.Contains(run));
```

### Смотрите также

* class [Node](../../node/)
* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
