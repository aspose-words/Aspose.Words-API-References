---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words för .NET
description: Aspose.Words.Layout.CommentDisplayMode uppräkning. Anger renderingsläget för dokumentkommentarer i C#.
type: docs
weight: 3290
url: /sv/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Anger renderingsläget för dokumentkommentarer.

```csharp
public enum CommentDisplayMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Hide | `0` | Inga dokumentkommentarer återges. |
| ShowInBalloons | `1` | Återger dokumentkommentarer i ballonger i marginalen. Detta är standardvärdet. |
| ShowInAnnotations | `2` | Återger dokumentkommentarer i annoteringar. Detta är endast tillgängligt för pdf-format. |

## Exempel

Visar hur du visar kommentarer när du sparar ett dokument i ett renderat format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations är endast tillgängligt i formaten Pdf1.7 och Pdf1.5.
// I andra format kommer det att fungera på samma sätt som Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Observera att det krävs för att bygga om dokumentets sidlayout (via metoden Document.UpdatePageLayout())
// efter att ha ändrat värdena för Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Se även

* namnutrymme [Aspose.Words.Layout](../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../)
