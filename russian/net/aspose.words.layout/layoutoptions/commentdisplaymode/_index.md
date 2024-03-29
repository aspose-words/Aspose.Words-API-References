---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words для .NET
description: LayoutOptions CommentDisplayMode свойство. Получает или задает способ отображения комментариев. Значение по умолчаниюShowInBalloons  на С#.
type: docs
weight: 30
url: /ru/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Получает или задает способ отображения комментариев. Значение по умолчанию:ShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## Примечания

Обратите внимание, что изменения не отображаются в выносках дляShowInAnnotations .

## Примеры

Показывает, как отображать комментарии при сохранении документа в визуализированном формате.

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

// Обратите внимание, что необходимо перестроить макет страницы документа (с помощью метода Document.UpdatePageLayout())
// после изменения значений Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Смотрите также

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
