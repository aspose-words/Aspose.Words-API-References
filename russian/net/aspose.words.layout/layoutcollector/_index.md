---
title: LayoutCollector Class
linktitle: LayoutCollector
articleTitle: LayoutCollector
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.LayoutCollector сорт. Этот класс позволяет вычислять номера страниц узлов документа на С#.
type: docs
weight: 3320
url: /ru/net/aspose.words.layout/layoutcollector/
---
## LayoutCollector class

Этот класс позволяет вычислять номера страниц узлов документа.

Чтобы узнать больше, посетите[Преобразование в формат фиксированной страницы](https://docs.aspose.com/words/net/converting-to-fixed-page-format/) статья документации.

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
| [Document](../../aspose.words.layout/layoutcollector/document/) { get; set; } | Получает или задает документ, к которому прикреплен этот экземпляр сборщика. |

## Методы

| Имя | Описание |
| --- | --- |
| [Clear](../../aspose.words.layout/layoutcollector/clear/)() | Очищает все собранные данные макета. Вызовите этот метод после обновления документа вручную или перестройки макета. |
| [GetEndPageIndex](../../aspose.words.layout/layoutcollector/getendpageindex/)(*[Node](../../aspose.words/node/)*) | Получает индекс страницы, отсчитываемый от 1, на которой заканчивается узел. Возвращает 0, если узел не может быть сопоставлен со страницей. |
| [GetEntity](../../aspose.words.layout/layoutcollector/getentity/)(*[Node](../../aspose.words/node/)*) | Возвращает непрозрачную позицию[`LayoutEnumerator`](../layoutenumerator/) который соответствует указанному узлу. Вы можете использовать возвращаемое значение в качестве аргумента[`Current`](../layoutenumerator/current/) учитывая, что документ, являющийся , и документ узла одинаковы. |
| [GetNumPagesSpanned](../../aspose.words.layout/layoutcollector/getnumpagesspanned/)(*[Node](../../aspose.words/node/)*) | Получает количество страниц, охватываемых указанным узлом. 0, если узел находится на одной странице. Это то же самое, что[`GetEndPageIndex`](./getendpageindex/) -[`GetStartPageIndex`](./getstartpageindex/) . |
| [GetStartPageIndex](../../aspose.words.layout/layoutcollector/getstartpageindex/)(*[Node](../../aspose.words/node/)*) | Получает индекс страницы, отсчитываемый от 1, где начинается узел. Возвращает 0, если узел не может быть сопоставлен со страницей. |

## Примечания

Когда вы создаете`LayoutCollector` и укажите[`Document`](../../aspose.words/document/) объект документа, к которому нужно прикрепить, сборщик запишет сопоставление узлов документа с объектами макета, когда документ форматируется на страницы.

Вы сможете узнать, на какой странице находится конкретный узел документа (например, прогон, абзац или ячейка таблицы) с помощью[`GetStartPageIndex`](./getstartpageindex/) ,[`GetEndPageIndex`](./getendpageindex/) и[`GetNumPagesSpanned`](./getnumpagesspanned/)методы. Эти методы автоматически создают модель макета страницы документа и при необходимости обновляют поля.

Если вам больше не нужно собирать информацию о макете, лучше всего установить[`Document`](./document/) собственность`нулевой` , чтобы избежать ненужного сбора дополнительных сопоставлений макета.

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
