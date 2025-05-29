---
title: ParagraphCollection Class
linktitle: ParagraphCollection
articleTitle: ParagraphCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.ParagraphCollection для бесперебойного доступа к структурированным узлам Paragraph, что улучшает работу с документами и повышает эффективность ваших проектов.
type: docs
weight: 5140
url: /ru/net/aspose.words/paragraphcollection/
---
## ParagraphCollection class

Предоставляет типизированный доступ к коллекции[`Paragraph`](../paragraph/) узлы.

Чтобы узнать больше, посетите[Работа с абзацами](https://docs.aspose.com/words/net/working-with-paragraphs/) документальная статья.

```csharp
public class ParagraphCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/paragraphcollection/item/) { get; } | Извлекает[`Paragraph`](../paragraph/) по данному индексу. (2 indexers) |

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
| [ToArray](../../aspose.words/paragraphcollection/toarray/#toarray_1)() | Копирует все абзацы из коллекции в новый массив абзацев. (2 methods) |

## Примеры

Показывает, как проверить, является ли абзац измененным вариантом.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Этот документ содержит редакции «Перемещение», которые появляются, когда мы выделяем текст курсором,
// а затем перетащите его, чтобы переместить в другое место
// при отслеживании изменений в Microsoft Word через «Рецензирование» -> «Отслеживать изменения».
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Перемещения ревизий состоят из пар ревизий «Переместить из» и «Переместить в».
// Эти правки представляют собой потенциальные изменения документа, которые мы можем либо принять, либо отклонить.
// Прежде чем принять/отклонить изменение хода, документ
// необходимо отслеживать как пункты отправления, так и пункты прибытия текста.
// Второй и четвертый абзацы определяют одну такую редакцию, и, таким образом, оба имеют одинаковое содержание.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Редакция «Переместить из» — это абзац, из которого мы перетащили текст.
// Если мы примем изменения, этот абзац исчезнет,
// а другой останется и больше не будет ревизией.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Редакция «Переместить в» — это абзац, в который мы перетащили текст.
// Если мы отклоним изменение, этот абзац исчезнет, а другой останется.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
