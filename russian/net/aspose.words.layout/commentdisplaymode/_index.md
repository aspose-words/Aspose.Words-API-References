---
title: Enum CommentDisplayMode
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Layout.CommentDisplayMode перечисление. Определяет режим отображения комментариев к документу.
type: docs
weight: 3090
url: /ru/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Определяет режим отображения комментариев к документу.

```csharp
public enum CommentDisplayMode
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Hide | `0` | Комментарии к документу не отображаются. |
| ShowInBalloons | `1` | Отображает комментарии к документу во всплывающих подсказках на полях. Это значение по умолчанию. |
| ShowInAnnotations | `2` | Визуализирует комментарии к документам в аннотациях. Это доступно только для формата Pdf. |

### Примеры

Показывает, как отображать комментарии при сохранении документа в подготовленном формате.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations доступно только в форматах Pdf1.7 и Pdf1.5.
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


