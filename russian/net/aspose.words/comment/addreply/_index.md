---
title: Comment.AddReply
second_title: Справочник по API Aspose.Words для .NET
description: Comment метод. Добавляет ответ на этот комментарий.
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
| initial | String | Автор инициалов для ответа. |
| dateTime | DateTime | Дата и время ответа. |
| text | String | Текст ответа. |

### Возвращаемое значение

Созданный[`Comment`](../) узел для ответа.

### Примечания

Из-за существующих ограничений MS Office в документе допускается только 1 уровень ответов. Исключение типаInvalidOperationException будет вызвано, если этот метод вызывается для существующего комментария ответа.

### Примеры

Показывает, как добавить комментарий к документу, а затем ответить на него.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Разместите комментарий в узле в теле документа.
// Этот комментарий будет отображаться в месте своего абзаца,
// за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

// Добавляем ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Комментарии, которые не отвечают на другие комментарии, относятся к "верхнему уровню". У них нет комментариев предков.
Assert.Null(comment.Ancestor);

// Ответы имеют родительский комментарий верхнего уровня.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Смотрите также

* class [Comment](../)
* пространство имен [Aspose.Words](../../comment/)
* сборка [Aspose.Words](../../../)


