---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Layout.LayoutCollector для эффективного вычисления номеров страниц узлов документа, что улучшит ваш опыт управления документами.
type: docs
weight: 3770
url: /ru/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Этот класс позволяет вычислять номера страниц узлов документа.

Чтобы узнать больше, посетите[Преобразование в формат с фиксированным размером страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) документальная статья.

```csharp
public class LayoutCollector
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LayoutCollector](layoutcollector/)(*[Document](../../aspose.words/document/)*) | Инициализирует экземпляр этого класса. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Возвращает или задает документ, к которому прикреплен этот экземпляр коллектора. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Очищает все собранные данные макета. Вызывайте этот метод после того, как документ был вручную обновлен или макет был перестроен. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Получает индекс страницы, на которой заканчивается узел, начиная с 1. Возвращает 0, если узел не может быть сопоставлен со страницей. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Возвращает непрозрачную позицию[`LayoutEnumerator`](../layoutenumerator/) который соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргумента для[`Current`](../layoutenumerator/current/) учитывая, что документ being перечислен и документ узла одинаковы. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Получает количество страниц, которые охватывает указанный узел. 0, если узел находится на одной странице. Это то же самое, что[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Получает индекс страницы, начинающейся с 1, где начинается узел. Возвращает 0, если узел не может быть сопоставлен со страницей. |

## Примечания

Когда вы создаете`LayoutCollector` и укажите[`Document`](../../aspose.words/document/)объект документа для присоединения, сборщик запишет сопоставление узлов документа с объектами макета, когда документ форматируется на страницы.

Вы сможете узнать, на какой странице находится определенный узел документа (например, блок, абзац или ячейка таблицы) с помощью[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) и[`GetNumPagesSpanned`](./getnumpagesspanned/) методы. Эти методы автоматически строят модель макета страницы документа и обновляют поля при необходимости.

Когда вам больше не нужно собирать информацию о макете, лучше всего установить[`Document`](./document/) собственность`нулевой` , чтобы избежать ненужного сбора дополнительных сопоставлений макетов.

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
