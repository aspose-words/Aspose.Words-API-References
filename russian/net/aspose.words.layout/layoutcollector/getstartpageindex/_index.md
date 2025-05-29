---
title: LayoutCollector.GetStartPageIndex
linktitle: GetStartPageIndex
articleTitle: GetStartPageIndex
second_title: Aspose.Words для .NET
description: Откройте для себя метод LayoutCollector GetStartPageIndex, чтобы легко найти индекс начальной страницы узла, начинающийся с 1. Упростите процесс сопоставления сегодня!
type: docs
weight: 70
url: /ru/net/aspose.words.layout/layoutcollector/getstartpageindex/
---
## LayoutCollector.GetStartPageIndex method

Получает индекс страницы, начинающейся с 1, где начинается узел. Возвращает 0, если узел не может быть сопоставлен со страницей.

```csharp
public int GetStartPageIndex(Node node)
```

## Примеры

Показывает, как просмотреть диапазоны страниц, охватываемые узлом.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Вызываем метод «GetNumPagesSpanned», чтобы подсчитать, сколько страниц занимает содержимое нашего документа.
// Поскольку документ пуст, количество страниц в данный момент равно нулю.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Заполните документ 5 страницами контента.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Перед сборщиком макетов нам нужно вызвать метод "UpdatePageLayout", чтобы получить
// точная цифра для любой метрики, связанной с макетом, например, количество страниц.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Мы можем видеть номера начальной и конечной страниц любого узла и их общее количество страниц.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Мы можем перебирать сущности макета, используя LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator может обходить коллекцию сущностей макета как дерево.
// Мы также можем применить его к соответствующей сущности макета любого узла.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Смотрите также

* class [Node](../../../aspose.words/node/)
* class [LayoutCollector](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
