---
title: RevisionCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words для .NET
description: RevisionCollection Count свойство. Возвращает количество ревизий в коллекции на С#.
type: docs
weight: 10
url: /ru/net/aspose.words/revisioncollection/count/
---
## RevisionCollection.Count property

Возвращает количество ревизий в коллекции.

```csharp
public int Count { get; }
```

## Примеры

Показывает, как работать с изменениями в документе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Обычное редактирование документа не считается ревизией.
builder.Write("This does not count as a revision. ");

Assert.IsFalse(doc.HasRevisions);

// Чтобы зарегистрировать наши правки как версии, нам нужно объявить автора, а затем начать их отслеживать.
doc.StartTrackRevisions("John Doe", DateTime.Now);

builder.Write("This is revision #1. ");

Assert.IsTrue(doc.HasRevisions);
Assert.AreEqual(1, doc.Revisions.Count);

// Этот флаг соответствует «Обзору» -> «Отслеживание» -> Опция «Отслеживать изменения» в Microsoft Word.
// Метод "StartTrackRevisions" не влияет на его значение,
// и документ отслеживает изменения программно, несмотря на то, что он имеет значение «false».
// Если мы откроем этот документ с помощью Microsoft Word, он не будет отслеживать изменения.
Assert.IsFalse(doc.TrackRevisions);

// Мы добавили текст с помощью построителя документов, поэтому первая редакция является ревизией типа вставки.
Revision revision = doc.Revisions[0];
Assert.AreEqual("John Doe", revision.Author);
Assert.AreEqual("This is revision #1. ", revision.ParentNode.GetText());
Assert.AreEqual(RevisionType.Insertion, revision.RevisionType);
Assert.AreEqual(revision.DateTime.Date, DateTime.Now.Date);
Assert.AreEqual(doc.Revisions.Groups[0], revision.Group);

// Удалить прогон, чтобы создать ревизию типа удаления.
doc.FirstSection.Body.FirstParagraph.Runs[0].Remove();

// Добавление новой ревизии помещает ее в начало коллекции ревизий.
Assert.AreEqual(RevisionType.Deletion, doc.Revisions[0].RevisionType);
Assert.AreEqual(2, doc.Revisions.Count);

// Вставленные версии отображаются в теле документа еще до того, как мы примем/отклоним редакцию.
// Отклонение ревизии приведет к удалению ее узлов из тела. И наоборот, узлы, составляющие ревизию, удаляют.
// также задерживаемся в документе, пока не примем редакцию.
Assert.AreEqual("This does not count as a revision. This is revision #1.", doc.GetText().Trim());

// Принятие удаления ревизии приведет к удалению родительского узла из текста абзаца
// а затем удалить саму ревизию коллекции.
doc.Revisions[0].Accept();

Assert.AreEqual(1, doc.Revisions.Count);
Assert.AreEqual("This is revision #1.", doc.GetText().Trim());

builder.Writeln("");
builder.Write("This is revision #2.");

// Теперь переместим узел, чтобы создать движущийся тип ревизии.
Node node = doc.FirstSection.Body.Paragraphs[1];
Node endNode = doc.FirstSection.Body.Paragraphs[1].NextSibling;
Node referenceNode = doc.FirstSection.Body.Paragraphs[0];

while (node != endNode)
{
    Node nextNode = node.NextSibling;
    doc.FirstSection.Body.InsertBefore(node, referenceNode);
    node = nextNode;
}

Assert.AreEqual(RevisionType.Moving, doc.Revisions[0].RevisionType);
Assert.AreEqual(8, doc.Revisions.Count);
Assert.AreEqual("This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc.GetText().Trim());

// Перемещаемая ревизия теперь имеет индекс 1. Отклоните ревизию, чтобы удалить ее содержимое.
doc.Revisions[1].Reject();

Assert.AreEqual(6, doc.Revisions.Count);
Assert.AreEqual("This is revision #1. \rThis is revision #2.", doc.GetText().Trim());
```

### Смотрите также

* class [RevisionCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
