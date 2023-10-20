---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words för .NET
description: LayoutOptions CommentDisplayMode fast egendom. Hämtar eller ställer in hur kommentarer renderas. Standardvärdet ärShowInBalloons  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Hämtar eller ställer in hur kommentarer renderas. Standardvärdet ärShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## Anmärkningar

Observera att revisioner inte återges i ballonger förShowInAnnotations .

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

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
