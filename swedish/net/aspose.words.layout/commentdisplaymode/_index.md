---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Layout.CommentDisplayMode-enum för optimerad rendering av dokumentkommentarer. Förbättra ditt dokuments tydlighet och presentation idag!
type: docs
weight: 3740
url: /sv/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Anger renderingsläge för dokumentkommentarer.

```csharp
public enum CommentDisplayMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Hide | `0` | Inga dokumentkommentarer återges. |
| ShowInBalloons | `1` | Återger dokumentkommentarer i bubblor i marginalen. Detta är standardvärdet. |
| ShowInAnnotations | `2` | Återger dokumentkommentarer i anteckningar. Detta är endast tillgängligt för PDF-format. |

## Exempel

Visar hur man visar kommentarer när man sparar ett dokument i ett renderat format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations är endast tillgängligt i formaten Pdf1.7 och Pdf1.5.
// I andra format fungerar det på liknande sätt som Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Observera att det krävs att dokumentets sidlayout ombyggs (via Document.UpdatePageLayout()-metoden)
// efter att ha ändrat värdena för Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
