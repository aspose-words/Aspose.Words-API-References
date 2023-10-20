---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words для .NET
description: Comment AddReply метод. Добавляет ответ на этот комментарий на С#.
type: docs
weight: 120
url: /ru/net/aspose.words/comment/addreply/
---
## Comment.AddReply method

Добавляет ответ на этот комментарий.

```csharp
public Comment AddReply(string author, string initial, DateTime dateTime, string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| author | String | Имя автора ответа. |
| initial | String | Инициалы автора ответа. |
| dateTime | DateTime | Дата и время ответа. |
| text | String | Текст ответа. |

### Возвращаемое значение

Созданный[`Comment`](../) узел для ответа.

## Примечания

В связи с существующими ограничениями MS Office в документе разрешен только 1 уровень ответов. Исключение типаInvalidOperationException будет вызван, если этот метод вызывается для существующего комментария ответа.

## Примеры

Показывает, как добавить комментарий к документу и затем ответить на него.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Размещаем комментарий в узле тела документа.
// Этот комментарий появится в том месте, где находится его абзац,
// за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

// Добавляем ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Комментарии, которые не отвечают на другие комментарии, относятся к «верхнему уровню». У них нет комментариев предков.
Assert.Null(comment.Ancestor);

// Ответы содержат комментарий верхнего уровня предка.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Смотрите также

* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
