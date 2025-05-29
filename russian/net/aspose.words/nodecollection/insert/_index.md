---
title: NodeCollection.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words для .NET
description: Легко вставляйте узлы в NodeCollection в любом индексе с помощью нашего оптимизированного метода Insert. Улучшите управление данными сегодня!
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
| index | Int32 | Индекс узла, начинающийся с нуля. Отрицательные индексы разрешены и указывают на доступ с конца списка. Например, -1 означает последний узел, -2 означает предпоследний и т. д. |
| node | Node | Узел для вставки. |

### Исключения

| исключение | условие |
| --- | --- |
| NotSupportedException | The[`NodeCollection`](../) «глубокая» коллекция. |

## Примечания

Узел вставляется как дочерний элемент в объект узла, из которого была создана коллекция.

Если индекс равен или больше[`Count`](../count/), узел добавляется в конец коллекции.

Если индекс отрицательный и его абсолютное значение больше[`Count`](../count/), узел добавляется в конец коллекции.

Если вставляемый узел был создан из другого документа, следует использовать [`ImportNode`](../../documentbase/importnode/) для импорта узла в текущий документ. Импортированный узел затем можно вставить в текущий документ.

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
