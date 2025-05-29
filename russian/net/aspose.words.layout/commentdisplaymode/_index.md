---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Layout.CommentDisplayMode для оптимизированного отображения комментариев к документам. Улучшите ясность и презентацию вашего документа сегодня!
type: docs
weight: 3740
url: /ru/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Указывает режим отображения комментариев к документу.

```csharp
public enum CommentDisplayMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Hide | `0` | Комментарии к документу не отображаются. |
| ShowInBalloons | `1` | Отображает комментарии документа в виде выносок на полях. Это значение по умолчанию. |
| ShowInAnnotations | `2` | Отображает комментарии к документу в аннотациях. Доступно только для формата PDF. |

## Примеры

Показывает, как отображать комментарии при сохранении документа в визуализированном формате.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations доступен только в форматах Pdf1.7 и Pdf1.5.
// В других форматах это будет работать аналогично Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Обратите внимание, что необходимо перестроить макет страницы документа (через метод Document.UpdatePageLayout())
// после изменения значений Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Смотрите также

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
