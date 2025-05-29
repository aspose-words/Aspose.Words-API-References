---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.CommentCollection для легкого доступа к узлам комментариев, улучшения редактирования документов и совместной работы над вашими проектами.
type: docs
weight: 430
url: /ru/net/aspose.words/commentcollection/
---
## CommentCollection class

Предоставляет типизированный доступ к коллекции[`Comment`](../comment/) узлы.

Чтобы узнать больше, посетите[Работа с комментариями](https://docs.aspose.com/words/net/working-with-comments/) документальная статья.

```csharp
public class CommentCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Извлекает[`Comment`](../comment/) по данному индексу. (2 indexers) |

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
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Копирует все узлы из коллекции в новый массив узлов. |

## Примеры

Показывает, как отметить комментарий как «завершенный».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Вставьте комментарий, чтобы указать на ошибку.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Комментарии имеют флаг «Готово», который по умолчанию установлен на «false».
// Если комментарий предполагает, что мы должны внести изменения в документ,
// мы можем применить изменение, а затем установить флаг «Готово», чтобы обозначить исправление.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Комментарии, которые «готовы», будут отличаться друг от друга
// из тех, которые не «закончены» с выцветшим цветом текста.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
