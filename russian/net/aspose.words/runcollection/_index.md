---
title: Class RunCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.RunCollection сорт. Обеспечивает типизированный доступ к коллекцииRun узлы.
type: docs
weight: 4830
url: /ru/net/aspose.words/runcollection/
---
## RunCollection class

Обеспечивает типизированный доступ к коллекции[`Run`](../run/) узлы.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

```csharp
public class RunCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Получает[`Run`](../run/) по данному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию стиля foreach по коллекции узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Возвращает индекс указанного узла, начинающийся с нуля. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Копирует все прогоны из коллекции в новый массив прогонов. (2 methods) |

### Примеры

Показывает, как определить тип редакции встроенного узла.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Когда мы редактируем документ, в то время как опция «Отслеживать изменения», которую можно найти в разделе «Просмотр» -> Отслеживание,
// включен в Microsoft Word, вносимые нами изменения считаются исправлениями.
// При редактировании документа с помощью Aspose.Words мы можем начать отслеживать изменения,
// вызываем метод StartTrackRevisions документа и прекращаем отслеживание с помощью метода StopTrackRevisions.
// Мы можем принять изменения, чтобы включить их в документ
// или отклонить их, чтобы эффективно изменить предлагаемое изменение.
Assert.AreEqual(6, doc.Revisions.Count);

// Родительским узлом ревизии является прогон, к которому относится ревизия. Run — это встроенный узел.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Ниже приведены пять типов ревизий, которые могут пометить встроенный узел.
// 1 - «Вставка» ревизии:
// Эта редакция происходит, когда мы вставляем текст во время отслеживания изменений.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Версия "формата":
// Эта редакция происходит, когда мы меняем форматирование текста при отслеживании изменений.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - переход от ревизии:
// Когда мы выделяем текст в Microsoft Word, а затем перетаскиваем его в другое место документа
// при отслеживании изменений появляются две ревизии.
// Ревизия «переместить из» — это копия исходного текста до того, как мы его переместили.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 — «перейти на» ревизию:
// Ревизия «переместить в» — это текст, который мы переместили в новую позицию в документе.
// Ревизии «Переместить из» и «Перейти в» появляются парами для каждой выполняемой нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию «переместить из» и ее текст,
// и сохраняет текст из версии «перейти в».
// Отклонение ревизии перемещения, наоборот, сохраняет ревизию «перейти из» и удаляет ревизию «перейти в».
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - "Удалить" ревизию:
// Эта редакция возникает, когда мы удаляем текст во время отслеживания изменений. Когда мы удаляем такой текст,
// она останется в документе как редакция, пока мы либо не примем редакцию,
// который удалит текст навсегда или отклонит редакцию, что сохранит удаленный нами текст там, где он был.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


