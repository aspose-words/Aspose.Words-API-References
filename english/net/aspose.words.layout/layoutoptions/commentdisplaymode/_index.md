---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
second_title: Aspose.Words for .NET API Reference
description: LayoutOptions CommentDisplayMode property. Gets or sets the way comments are rendered. Default value is ShowInBalloons in C#.
type: docs
weight: 30
url: /net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Gets or sets the way comments are rendered. Default value is ShowInBalloons.

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## Remarks

Note that revisions are not rendered in balloons for ShowInAnnotations.

## Examples

Shows how to show comments when saving a document to a rendered format.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
// In other formats, it will work similarly to Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
// after changing the Document.LayoutOptions values.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### See Also

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* namespace [Aspose.Words.Layout](../../layoutoptions/)
* assembly [Aspose.Words](../../../)
