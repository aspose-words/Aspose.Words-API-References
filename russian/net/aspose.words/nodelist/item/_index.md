---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words для .NET
description: Получите доступ к определенным узлам без усилий с помощью свойства NodeList Item. Извлеките узлы по индексу для упрощенной обработки данных и эффективного кодирования.
type: docs
weight: 20
url: /ru/net/aspose.words/nodelist/item/
---
## NodeList indexer

Извлекает узел по указанному индексу.

```csharp
public Node this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс в списке узлов. |

## Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ с конца коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и т. д.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше количества элементов в списке, возвращается пустая ссылка.

## Примеры

Показывает, как использовать XPath для навигации по NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте несколько узлов с помощью DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Наш документ содержит три узла Run.
NodeList nodeList = doc.SelectNodes("//Бегать");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Используйте двойную косую черту, чтобы выбрать все узлы Run
// которые являются косвенными потомками узла Table, которые будут участками внутри двух вставленных нами ячеек.
nodeList = doc.SelectNodes("//Table//Бегать");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Одинарные косые черты указывают прямые потомственные отношения,
// который мы пропустили, когда использовали двойные слеши.
Assert.AreEqual(doc.SelectNodes(" //Таблица//Выполнить"),
    doc.SelectNodes("//Таблица/Строка/Ячейка/Абзац/Выполнить"));

// Доступ к форме, содержащей вставленное нами изображение.
nodeList = doc.SelectNodes("//Форма");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Смотрите также

* class [Node](../../node/)
* class [NodeList](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
