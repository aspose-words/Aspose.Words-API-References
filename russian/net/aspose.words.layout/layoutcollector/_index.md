---
title: LayoutCollector
second_title: Справочник по API Aspose.Words для .NET
description: Этот класс позволяет вычислять номера страниц узлов документа.
type: docs
weight: 3120
url: /ru/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Этот класс позволяет вычислять номера страниц узлов документа.

```csharp
public class LayoutCollector
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LayoutCollector](layoutcollector)(Document) | Инициализирует экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document) { get; set; } | Получает или задает документ, к которому прикреплен этот экземпляр сборщика. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear)() | Очищает все собранные данные макета. Вызовите этот метод после обновления документа вручную или перестроения макета. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex)(Node) | Получает отсчитываемый от 1 индекс страницы, на которой заканчивается узел. Возвращает 0, если узел не может быть сопоставлен со страницей. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity)(Node) | Возвращает непрозрачную позицию[`LayoutEnumerator`](../layoutenumerator) который соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргумента для[`Current`](../layoutenumerator/current) учитывая, что перечисляемый документ be и документ узла совпадают. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned)(Node) | Получает количество страниц, которые охватывает указанный узел. 0, если узел находится на одной странице. Это то же самое, что и[`GetEndPageIndex`](./getendpageindex) -[`GetStartPageIndex`](./getstartpageindex) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex)(Node) | Получает отсчитываемый от 1 индекс страницы, с которой начинается узел. Возвращает 0, если узел не может быть сопоставлен со страницей. |

### Примечания

Когда вы создаете[`LayoutCollector`](../layoutcollector) и указать[`Document`](../../aspose.words/document)объект документа для присоединения, сборщик запишет сопоставление узлов документа с объектами макета, когда документ отформатирован в страницы.

Вы сможете узнать, на какой странице находится тот или иной узел документа (например, серия, абзац или ячейка таблицы) с помощью[`GetStartPageIndex`](./getstartpageindex) ,[`GetEndPageIndex`](./getendpageindex) а также[`GetNumPagesSpanned`](./getnumpagesspanned) методы. Эти методы автоматически создают модель макета страницы документа и при необходимости обновляют поля.

Когда вам больше не нужно собирать информацию о макете, лучше всего установить[`Document`](./document) свойство на null , чтобы избежать ненужного сбора дополнительных сопоставлений макета.

### Примеры

Показывает, как просмотреть диапазоны страниц, которые охватывает узел.

```csharp
Document doc = new Document();
LayoutCollector layoutCollector = new LayoutCollector(doc);

// Вызовите метод «GetNumPagesSpanned», чтобы подсчитать, сколько страниц занимает содержимое нашего документа.
// Поскольку документ пуст, это количество страниц в настоящее время равно нулю.
Assert.AreEqual(doc, layoutCollector.Document);
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

// Заполнить документ 5 страницами содержимого.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Section 1");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Перед сборщиком макетов нам нужно вызвать метод «UpdatePageLayout», чтобы получить
// точная цифра для любой метрики, связанной с макетом, например, для количества страниц.
Assert.AreEqual(0, layoutCollector.GetNumPagesSpanned(doc));

layoutCollector.Clear();
doc.UpdatePageLayout();

Assert.AreEqual(5, layoutCollector.GetNumPagesSpanned(doc));

// Мы можем видеть номера начальной и конечной страниц любого узла и их общий диапазон страниц.
NodeCollection nodes = doc.GetChildNodes(NodeType.Any, true);
foreach (Node node in nodes)
{
    Console.WriteLine($"->  NodeType.{node.NodeType}: ");
    Console.WriteLine(
        $"\tStarts on page {layoutCollector.GetStartPageIndex(node)}, ends on page {layoutCollector.GetEndPageIndex(node)}," +
        $" spanning {layoutCollector.GetNumPagesSpanned(node)} pages.");
}

// Мы можем перебирать объекты макета с помощью LayoutEnumerator.
LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

Assert.AreEqual(LayoutEntityType.Page, layoutEnumerator.Type);

// LayoutEnumerator может перемещаться по коллекции сущностей макета, как по дереву.
// Мы также можем применить его к соответствующему объекту макета любого узла.
layoutEnumerator.Current = layoutCollector.GetEntity(doc.GetChild(NodeType.Paragraph, 1, true));

Assert.AreEqual(LayoutEntityType.Span, layoutEnumerator.Type);
Assert.AreEqual("¶", layoutEnumerator.Text);
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
