---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „LayoutOptions CommentDisplayMode“, um die Kommentardarstellung anzupassen. Passen Sie sie einfach an, um die Benutzerfreundlichkeit mit Optionen wie „ShowInBalloons“ zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Ruft die Art und Weise ab, wie Kommentare gerendert werden. Der Standardwert istShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## Bemerkungen

Beachten Sie, dass Revisionen nicht in Sprechblasen dargestellt werden fürShowInAnnotations .

## Beispiele

Zeigt, wie Kommentare beim Speichern eines Dokuments in einem gerenderten Format angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations ist nur in den Formaten Pdf1.7 und Pdf1.5 verfügbar.
// In anderen Formaten funktioniert es ähnlich wie „Ausblenden“.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Beachten Sie, dass das Seitenlayout des Dokuments neu erstellt werden muss (über die Methode Document.UpdatePageLayout()).
// nach dem Ändern der Document.LayoutOptions-Werte.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Siehe auch

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
