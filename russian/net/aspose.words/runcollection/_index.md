---
title: RunCollection Class
linktitle: RunCollection
articleTitle: RunCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.RunCollection для бесперебойного доступа к узлам Run. Улучшите обработку документов с помощью мощных типизированных функций!
type: docs
weight: 5570
url: /ru/net/aspose.words/runcollection/
---
## RunCollection class

Предоставляет типизированный доступ к коллекции[`Run`](../run/) узлы.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public class RunCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/runcollection/item/) { get; } | Извлекает[`Run`](../run/) по данному индексу. (2 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию в стиле «foreach» по коллекции узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного узла, отсчитываемый от нуля. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [ToArray](../../aspose.words/runcollection/toarray/#toarray_1)() | Копирует все прогоны из коллекции в новый массив прогонов. (2 methods) |

## Примеры

Показывает, как определить тип ревизии встроенного узла.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Когда мы редактируем документ, используя опцию «Отслеживать изменения», которую можно найти в Обзор -> Отслеживание,
// включен в Microsoft Word, то применяемые нами изменения считаются правками.
// При редактировании документа с помощью Aspose.Words мы можем начать отслеживать изменения,
// вызов метода "StartTrackRevisions" документа и остановка отслеживания с помощью метода "StopTrackRevisions".
// Мы можем либо принять изменения, чтобы включить их в документ
// или отклонить их, чтобы эффективно изменить предлагаемое изменение.
Assert.AreEqual(6, doc.Revisions.Count);

// Родительский узел ревизии — это прогон, к которому относится ревизия. Прогон — это встроенный узел.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Ниже приведены пять типов ревизий, которые могут пометить встроенный узел.
// 1 - «Вставная» редакция:
// Эта редакция происходит, когда мы вставляем текст во время отслеживания изменений.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Изменение «формата»:
// Эта редакция происходит, когда мы меняем форматирование текста во время отслеживания изменений.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - «Переход от» пересмотра:
// Когда мы выделяем текст в Microsoft Word, а затем перетаскиваем его в другое место документа
// при отслеживании изменений появляются две ревизии.
// Редакция «перемещения» — это копия текста, который был изначально до того, как мы его переместили.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Пересмотр «перехода к»:
// Редакция «переместить в» — это текст, который мы переместили на новое место в документе.
// Ревизии «Переместить из» и «Переместить в» появляются парами для каждой выполняемой нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию «перемещения из» и ее текст,
// и сохраняет текст из ревизии «перейти в».
// Отклонение перенесенной версии, наоборот, сохраняет перенесенную версию и удаляет перенесенную версию.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - «удаленная» ревизия:
// Эта ревизия происходит, когда мы удаляем текст во время отслеживания изменений. Когда мы удаляем текст таким образом,
// он останется в документе как исправление, пока мы не примем исправление,
// что удалит текст навсегда или отклонит изменение, что оставит удаленный нами текст там, где он был.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
