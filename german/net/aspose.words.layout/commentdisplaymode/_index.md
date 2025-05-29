---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Layout.CommentDisplayMode für optimiertes Rendern von Dokumentkommentaren. Verbessern Sie noch heute die Übersichtlichkeit und Präsentation Ihres Dokuments!
type: docs
weight: 3740
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
| ShowInBalloons | `1` | Dokumentkommentare werden in Sprechblasen am Rand angezeigt. Dies ist der Standardwert. |
| ShowInAnnotations | `2` | Stellt Dokumentkommentare in Anmerkungen dar. Dies ist nur im PDF-Format verfügbar. |

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

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)
