---
title: NodeList.Item
second_title: Справочник по API Aspose.Words для .NET
description: NodeList свойство. Извлекает узел по заданному индексу.
type: docs
weight: 20
url: /ru/net/aspose.words/nodelist/item/
---
## NodeList indexer

Извлекает узел по заданному индексу.

```csharp
public Node this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс в списке узлов. |

### Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается пустая ссылка.

Если индекс отрицательный и его абсолютное значение больше, чем количество элементов в списке, возвращается пустая ссылка.

### Примеры

Показывает, как использовать XPath для навигации по NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем несколько узлов с помощью DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// Наш документ содержит три узла Run.
NodeList nodeList = doc.SelectNodes("//Бежать");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Используйте двойную косую черту, чтобы выбрать все узлы Run
// которые являются непрямыми потомками узла Table, которые будут прогонами внутри двух вставленных ячеек.
nodeList = doc.SelectNodes("//Table//Бежать");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Одиночная косая черта указывает прямые отношения потомков,
// который мы пропустили, когда использовали двойную косую черту.
Assert.AreEqual(doc.SelectNodes(" //Таблица//Выполнить"),
    doc.SelectNodes("//Таблица/Строка/Ячейка/Абзац/Выполнить");

// Доступ к фигуре, содержащей вставленное изображение.
nodeList = doc.SelectNodes("//Форма");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Смотрите также

* class [Node](../../node/)
* class [NodeList](../)
* пространство имен [Aspose.Words](../../nodelist/)
* сборка [Aspose.Words](../../../)


