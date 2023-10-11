---
title: Class ParagraphCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.ParagraphCollection сорт. Обеспечивает типизированный доступ к коллекцииParagraph узлы.
type: docs
weight: 4410
url: /ru/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Обеспечивает типизированный доступ к коллекции[`Paragraph`](../paragraph/) узлы.

Чтобы узнать больше, посетите[Работа с абзацами](https://docs.aspose.com/words/net/working-with-paragraphs/) статья документации.

```csharp
public class ParagraphCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Получает[`Paragraph`](../paragraph/) по данному индексу. (2 indexers) |

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
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Копирует все абзацы из коллекции в новый массив абзацев. (2 methods) |

### Примеры

Показывает, как проверить, является ли абзац измененной версией.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Этот документ содержит редакции «Переместить», которые появляются, когда мы выделяем текст курсором,
// а затем перетащите его, чтобы переместить в другое место
// при отслеживании изменений в Microsoft Word через «Просмотр» -> gt; "Отслеживать изменения".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Перемещение ревизий состоит из пар ревизий «Переместить из» и «Переместить в».
// Эти поправки представляют собой потенциальные изменения в документе, которые мы можем принять или отклонить.
// Прежде чем мы примем/отклоним редакцию перемещения, документ
// должен отслеживать пункты отправления и прибытия текста.
// Второй и четвертый абзацы определяют одну такую ревизию и, следовательно, оба имеют одинаковое содержание.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Редакция «Переместить из» — это абзац, из которого мы перетащили текст.
// Если мы примем редакцию, этот абзац исчезнет,
// а другой останется и больше не будет ревизией.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Редакция «Переместить в» — это абзац, в который мы перетащили текст.
// Если мы отклоним ревизию, этот абзац исчезнет, а другой останется.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


