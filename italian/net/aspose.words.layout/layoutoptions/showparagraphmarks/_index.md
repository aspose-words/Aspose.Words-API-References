---
title: LayoutOptions.ShowParagraphMarks
second_title: Aspose.Words per .NET API Reference
description: LayoutOptions proprietà. Ottiene o imposta lindicazione del rendering dei segni di paragrafo. Limpostazione predefinita è False.
type: docs
weight: 80
url: /it/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Ottiene o imposta l'indicazione del rendering dei segni di paragrafo. L'impostazione predefinita è False.

```csharp
public bool ShowParagraphMarks { get; set; }
```

### Esempi

Mostra come mostrare i segni di paragrafo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi attiva i segni di paragrafo per mostrare le estremità dei paragrafi
// con il simbolo di una crocetta (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../layoutoptions/)
* assemblea [Aspose.Words](../../../)


