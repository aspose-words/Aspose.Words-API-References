---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà CommentDisplayMode di LayoutOptions per personalizzare il rendering dei commenti. Impostala facilmente per migliorare l'esperienza utente con opzioni come ShowInBalloons.
type: docs
weight: 30
url: /it/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Ottiene o imposta il modo in cui vengono visualizzati i commenti. Il valore predefinito è ShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## Osservazioni

Nota che le revisioni non vengono visualizzate nei fumetti perShowInAnnotations .

## Esempi

Mostra come visualizzare i commenti quando si salva un documento in un formato renderizzato.

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

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
