---
title: Class CommentCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.CommentCollection сорт. Обеспечивает типизированный доступ к коллекцииComment узлы.
type: docs
weight: 240
url: /ru/net/aspose.words/commentcollection/
---
## CommentCollection class

Обеспечивает типизированный доступ к коллекции[`Comment`](../comment/) узлы.

Чтобы узнать больше, посетите[Работа с комментариями](https://docs.aspose.com/words/net/working-with-comments/) статья документации.

```csharp
public class CommentCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Получает[`Comment`](../comment/) по данному индексу. (2 indexers) |

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
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Копирует все узлы из коллекции в новый массив узлов. |

### Примеры

Показывает, как пометить комментарий как «готовый».

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Вставляем комментарий, указывающий на ошибку.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Комментарии имеют флаг «Готово», для которого по умолчанию установлено значение «false».
// Если комментарий предлагает внести изменения в документ,
// мы можем применить изменение, а затем также установить флаг «Готово», чтобы указать на исправление.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// Комментарии, которые «готовы», будут отличаться друг от друга
// из тех, которые еще не «готовы» с блеклым цветом текста.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


