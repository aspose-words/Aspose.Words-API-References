---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words для .NET
description: Откройте для себя метод LayoutCollector GetEntity, легко извлеките позицию LayoutEnumerator для бесперебойной навигации по документу и повышения производительности.
type: docs
weight: 50
url: /ru/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Возвращает непрозрачную позицию[`LayoutEnumerator`](../../layoutenumerator/) который соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргумента для[`Current`](../../layoutenumerator/current/) учитывая, что документ being перечислен и документ узла одинаковы.

```csharp
public object GetEntity(Node node)
```

## Примечания

Этот метод работает только для[`Paragraph`](../../../aspose.words/paragraph/) узлы, а также неделимые линейные узлы, например[`BookmarkStart`](../../../aspose.words/bookmarkstart/) или[`Shape`](../../../aspose.words.drawing/shape/) . Это не работает для[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) или[`Table`](../../../aspose.words.tables/table/) узлы и узлы в верхнем/нижнем колонтитуле.

Обратите внимание, что сущность вернулась для[`Paragraph`](../../../aspose.words/paragraph/)узел — это разрыв абзаца. Используйте соответствующий метод для перехода к родительской строке

Если вам нужно перейти к[`Run`](../../../aspose.words/run/) текста, то вы можете вставить закладку прямо перед it , а затем перейти к закладке.

Если вам нужно перейти к[`Cell`](../../../aspose.words.tables/cell/) узел, затем вы можете перейти к[`Paragraph`](../../../aspose.words/paragraph/) узел в этой ячейке, а затем восходит к родительской сущности. Тот же подход может быть использован для[`Row`](../../../aspose.words.tables/row/) и[`Table`](../../../aspose.words.tables/table/) узлы.

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
