---
title: LayoutCollector.GetEntity
linktitle: GetEntity
articleTitle: GetEntity
second_title: Aspose.Words для .NET
description: LayoutCollector GetEntity метод. Возвращает непрозрачную позициюLayoutEnumerator который соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргументаCurrent учитывая что документ являющийся  и документ узла одинаковы на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.layout/layoutcollector/getentity/
---
## LayoutCollector.GetEntity method

Возвращает непрозрачную позицию[`LayoutEnumerator`](../../layoutenumerator/) который соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргумента[`Current`](../../layoutenumerator/current/) учитывая, что документ, являющийся , и документ узла одинаковы.

```csharp
public object GetEntity(Node node)
```

## Примечания

Этот метод работает только[`Paragraph`](../../../aspose.words/paragraph/) узлы, а также неделимые встроенные узлы, например[`BookmarkStart`](../../../aspose.words/bookmarkstart/) или[`Shape`](../../../aspose.words.drawing/shape/) . Это не работает для[`Run`](../../../aspose.words/run/) ,[`Cell`](../../../aspose.words.tables/cell/)[`Row`](../../../aspose.words.tables/row/) или[`Table`](../../../aspose.words.tables/table/) узлы и узлы в верхнем/нижнем колонтитуле.

Обратите внимание, что сущность вернулась за[`Paragraph`](../../../aspose.words/paragraph/) node — это интервал разрыва абзаца. Используйте соответствующий метод для перехода к родительской линии.

Если вам нужно перейти к[`Run`](../../../aspose.words/run/) текста, то вы можете вставить закладку прямо перед it , а затем вместо этого перейти к закладке.

Если вам нужно перейти к[`Cell`](../../../aspose.words.tables/cell/) узел, то вы можете перейти к[`Paragraph`](../../../aspose.words/paragraph/) в этой ячейке, а затем перейти к родительскому объекту. Тот же подход можно использовать для[`Row`](../../../aspose.words.tables/row/) и[`Table`](../../../aspose.words.tables/table/) узлы.

## Примеры

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
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
