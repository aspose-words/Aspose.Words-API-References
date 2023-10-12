---
title: LayoutCollector.GetEndPageIndex
second_title: Справочник по API Aspose.Words для .NET
description: LayoutCollector метод. Получает индекс страницы отсчитываемый от 1 на которой заканчивается узел. Возвращает 0 если узел не может быть сопоставлен со страницей.
type: docs
weight: 40
url: /ru/net/aspose.words.layout/layoutcollector/getendpageindex/
---
## LayoutCollector.GetEndPageIndex method

Получает индекс страницы, отсчитываемый от 1, на которой заканчивается узел. Возвращает 0, если узел не может быть сопоставлен со страницей.

```csharp
public int GetEndPageIndex(Node node)
```

### Примеры

Показывает, как просмотреть диапазоны страниц, охватываемые узлом.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Вызовите метод GetNumPagesSpanned, чтобы подсчитать, сколько страниц занимает содержимое нашего документа.
// Поскольку документ пуст, то количество страниц в данный момент равно нулю.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Заполняем документ 5 страницами контента.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Перед сборщиком макетов нам нужно вызвать метод «UpdatePageLayout», чтобы получить
// точная цифра для любого показателя, связанного с макетом, например количества страниц.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Мы можем видеть номера начальной и конечной страниц любого узла и их общие диапазоны страниц.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Мы можем перебирать объекты макета, используя LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator может перемещаться по коллекции объектов макета, как по дереву.
// Мы также можем применить его к соответствующему объекту макета любого узла.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Смотрите также

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* пространство имен [Aspose.Words.Layout](../../layoutcollector/)
* сборка [Aspose.Words](../../../)


