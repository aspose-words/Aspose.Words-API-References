---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words для .NET
description: NodeCollection Insert метод. Вставляет узел в коллекцию по указанному индексу на С#.
type: docs
weight: 80
url: /ru/net/aspose.words/nodecollection/insert/
---
## NodeCollection.Insert method

Вставляет узел в коллекцию по указанному индексу.

```csharp
public void Insert(int index, Node node)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс узла начинается с нуля. Отрицательные индексы разрешены и указывают на доступ с конца списка. Например, -1 означает последний узел, -2 означает предпоследний узел и так далее. |
| node | Node | Узел для вставки. |

### Исключения

| исключение | условие |
| --- | --- |
| NotSupportedException | [`NodeCollection`](../) это «глубокая» коллекция. |

## Примечания

Узел вставляется как дочерний в объект узла, из которого была создана коллекция.

Если индекс равен или больше[`Count`](../count/), узел добавляется в конец коллекции.

Если индекс отрицательный и его абсолютное значение больше[`Count`](../count/), узел добавляется в конец коллекции.

Если вставляемый узел был создан из другого документа, вам следует использовать [`ImportNode`](../../documentbase/importnode/) для импорта узла в текущий документ. Импортированный узел можно затем вставить в текущий документ.

## Примеры

Показывает, как работать с NodeCollection.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте текст в документ, вставив прогоны с помощью DocumentBuilder.
builder.Write("Run 1. ");
builder.Write("Run 2. ");

// Каждый вызов метода Write создает новый Run,
// который затем появляется в RunCollection родительского абзаца.
RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.AreEqual(2, runs.Count);

// Мы также можем вставить узел в RunCollection вручную.
Run newRun = new Run(doc, "Run 3. ");
runs.Insert(3, newRun);

Assert.True(runs.Contains(newRun));
Assert.AreEqual("Run 1. Run 2. Run 3.", doc.GetText().Trim());

// Доступ к отдельным запускам и удаление их, чтобы удалить их текст из документа.
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
