---
title: NodeList.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: NodeList Count свойство. Получает количество узлов в списке на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/nodelist/count/
---
## NodeList.Count property

Получает количество узлов в списке.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как использовать XPaths для навигации по NodeList.

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

// Наш документ содержит три узла «Выполнить».
NodeList nodeList = doc.SelectNodes("//Бегать");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Используйте двойную косую черту, чтобы выбрать все узлы выполнения
// которые являются косвенными потомками узла Таблицы, которые будут проходами внутри двух вставленных нами ячеек.
nodeList = doc.SelectNodes("//Table//Бегать");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Одиночные косые черты указывают прямые отношения потомков,
// который мы пропустили, когда использовали двойные косые черты.
Assert.AreEqual(doc.SelectNodes(" //Таблица//Выполнить"),
    doc.SelectNodes("//Таблица/Строка/Ячейка/Абзац/Выполнить");

// Доступ к фигуре, содержащей вставленное нами изображение.
nodeList = doc.SelectNodes("//Форма");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Смотрите также

* class [NodeList](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
