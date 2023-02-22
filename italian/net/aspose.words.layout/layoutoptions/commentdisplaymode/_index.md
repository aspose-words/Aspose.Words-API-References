---
title: LayoutOptions.CommentDisplayMode
second_title: Aspose.Words per .NET API Reference
description: LayoutOptions proprietà. Ottiene o imposta il modo in cui vengono visualizzati i commenti. Il valore predefinito èShowInBalloons .
type: docs
weight: 30
url: /it/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

Ottiene o imposta il modo in cui vengono visualizzati i commenti. Il valore predefinito èShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

### Osservazioni

Si noti che le revisioni non vengono visualizzate in fumetti perShowInAnnotations .

### Esempi

Mostra come mostrare i commenti quando si salva un documento in un formato renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations è disponibile solo nei formati Pdf1.7 e Pdf1.5.
// In altri formati funzionerà in modo simile a Nascondi.
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
* spazio dei nomi [Aspose.Words.Layout](../../layoutoptions/)
* assemblea [Aspose.Words](../../../)


