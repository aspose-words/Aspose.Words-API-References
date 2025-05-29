---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words для .NET
description: Откройте для себя метод SetText — удобный инструмент, который упрощает добавление комментариев, улучшает ваш рабочий процесс и повышает производительность без особых усилий.
type: docs
weight: 190
url: /ru/net/aspose.words/comment/settext/
---
## Comment.SetText method

Это удобный метод, позволяющий легко задать текст комментария.

```csharp
public void SetText(string text)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | String | Новый текст комментария. |

## Примечания

Этот метод позволяет быстро задать текст комментария из строки. Строка может содержать разрывы абзацев, это соответственно создаст абзацы текста в комментарии. Если вы хотите вставить в комментарий более сложные элементы, например закладки или таблицы или применить расширенное форматирование, то вам нужно использовать соответствующие классы узлов для построения текста комментария.

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
