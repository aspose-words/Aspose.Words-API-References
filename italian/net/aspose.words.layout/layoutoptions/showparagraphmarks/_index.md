---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words per .NET
description: LayoutOptions ShowParagraphMarks proprietà. Ottiene o imposta lindicazione se viene eseguito il rendering dei segni di paragrafo. Limpostazione predefinita èfalso  in C#.
type: docs
weight: 90
url: /it/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Ottiene o imposta l'indicazione se viene eseguito il rendering dei segni di paragrafo. L'impostazione predefinita è`falso` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Esempi

Mostra come visualizzare i segni di paragrafo in un documento di output sottoposto a rendering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare la fine dei paragrafi
// con il simbolo pilcrow (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
