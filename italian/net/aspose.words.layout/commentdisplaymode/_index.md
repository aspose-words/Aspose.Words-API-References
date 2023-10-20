---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words per .NET
description: Aspose.Words.Layout.CommentDisplayMode enum. Specifica la modalità di rendering per i commenti del documento in C#.
type: docs
weight: 3290
url: /it/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

Specifica la modalità di rendering per i commenti del documento.

```csharp
public enum CommentDisplayMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Hide | `0` | Nessun commento al documento viene visualizzato. |
| ShowInBalloons | `1` | Rende i commenti del documento in fumetti a margine. Questo è il valore predefinito. |
| ShowInAnnotations | `2` | Rende i commenti del documento nelle annotazioni. Disponibile solo per il formato PDF. |

## Esempi

Mostra come mostrare i commenti quando si salva un documento in un formato sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations è disponibile solo nei formati Pdf1.7 e Pdf1.5.
// In altri formati, funzionerà in modo simile a Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// Nota che è necessario ricostruire il layout della pagina del documento (tramite il metodo Document.UpdatePageLayout())
// dopo aver modificato i valori di Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Layout](../../aspose.words.layout/)
* assemblea [Aspose.Words](../../)
