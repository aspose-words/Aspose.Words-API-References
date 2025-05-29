---
title: NodeCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words для .NET
description: Узнайте, как метод NodeCollection Contains эффективно проверяет наличие узла в вашей коллекции, расширяя ваши возможности управления данными.
type: docs
weight: 50
url: /ru/net/aspose.words/nodecollection/contains/
---
## NodeCollection.Contains method

Определяет, находится ли узел в коллекции.

```csharp
public bool Contains(Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | Node | Узел, который необходимо найти. |

### Возвращаемое значение

`истинный`если элемент найден в коллекции; в противном случае,`ЛОЖЬ`.

## Примечания

Этот метод выполняет линейный поиск, поэтому среднее время выполнения пропорционально[`Count`](../count/).

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
