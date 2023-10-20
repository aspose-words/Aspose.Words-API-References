---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.CommentDisplayMode opsomming. Gibt den RenderingModus für Dokumentkommentare an in C#.
type: docs
weight: 3290
url: /de/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Gibt den Rendering-Modus für Dokumentkommentare an.

```csharp
public enum CommentDisplayMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Hide | `0` | Es werden keine Dokumentkommentare gerendert. |
| ShowInBalloons | `1` | Rendert Dokumentkommentare in Sprechblasen am Rand. Dies ist der Standardwert. |
| ShowInAnnotations | `2` | Rendert Dokumentkommentare in Anmerkungen. Dies ist nur für das PDF-Format verfügbar. |

## Beispiele

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
