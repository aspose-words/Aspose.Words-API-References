---
title: LayoutOptions.CommentDisplayMode
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutOptions eigendom. Ruft ab oder legt fest wie Kommentare gerendert werden. Der Standardwert istShowInBalloons .
type: docs
weight: 30
url: /de/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Ruft ab oder legt fest, wie Kommentare gerendert werden. Der Standardwert istShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

### Bemerkungen

Beachten Sie, dass Revisionen nicht in Sprechblasen gerendert werdenShowInAnnotations .

### Beispiele

Zeigt, wie Kommentare angezeigt werden, wenn ein Dokument in einem gerenderten Format gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations ist nur in den Formaten Pdf1.7 und Pdf1.5 verfügbar.
// In anderen Formaten funktioniert es ähnlich wie „Hide“.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Beachten Sie, dass das Seitenlayout des Dokuments neu erstellt werden muss (über die Methode Document.UpdatePageLayout())
// nach dem Ändern der Document.LayoutOptions-Werte.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Siehe auch

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../layoutoptions/)
* Montage [Aspose.Words](../../../)


