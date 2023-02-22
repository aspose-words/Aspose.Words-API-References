---
title: NodeList.Count
second_title: Справочник по API Aspose.Words для .NET
description: NodeList свойство. Получает количество узлов в списке.
type: docs
weight: 10
url: /ru/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Получает количество узлов в списке.

```csharp
public int Count { get; }
```

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

* class [NodeList](../)
* пространство имен [Aspose.Words](../../nodelist/)
* сборка [Aspose.Words](../../../)


