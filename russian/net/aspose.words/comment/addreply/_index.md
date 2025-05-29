---
title: Comment.AddReply
linktitle: AddReply
articleTitle: AddReply
second_title: Aspose.Words для .NET
description: Улучшите свои обсуждения с помощью метода Comment AddReply — легко добавляйте ответы на комментарии и повышайте вовлеченность на своей платформе!
type: docs
weight: 160
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
| initial | String | Автор ставит инициалы в ответе. |
| dateTime | DateTime | Дата и время ответа. |
| text | String | Текст ответа. |

### Возвращаемое значение

Созданный[`Comment`](../) узел для ответа.

### Исключения

| исключение | условие |
| --- | --- |
| InvalidOperationException | Вызывает ошибку, если этот метод вызывается для существующего комментария Reply. |

## Примечания

В связи с существующими ограничениями MS Office в документе допускается только 1 уровень ответов.

## Примеры

Показывает, как добавить комментарий к документу, а затем ответить на него.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Разместите комментарий в узле тела документа.
// Этот комментарий будет отображаться на месте своего абзаца,
// за пределами правого поля страницы и с пунктирной линией, соединяющей его с абзацем.
builder.CurrentParagraph.AppendChild(comment);

// Добавьте ответ, который будет отображаться под родительским комментарием.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Комментарии и ответы являются узлами комментариев.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Комментарии, которые не отвечают на другие комментарии, являются "верхнего уровня". У них нет предков.
Assert.Null(comment.Ancestor);

// Ответы имеют родительский комментарий верхнего уровня.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Смотрите также

* class [Comment](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
