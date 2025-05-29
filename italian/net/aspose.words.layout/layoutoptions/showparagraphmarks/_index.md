---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ShowParagraphMarks di LayoutOptions migliora la formattazione del testo attivando e disattivando la visibilità dei segni di paragrafo. Migliora la chiarezza del tuo documento oggi stesso!
type: docs
weight: 90
url: /it/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Ottiene o imposta l'indicazione se i segni di paragrafo sono renderizzati. Il valore predefinito è`falso` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Esempi

Mostra come visualizzare i segni di paragrafo in un documento di output renderizzato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare la fine dei paragrafi
// con un simbolo pilcrow (¶) quando eseguiamo il rendering del documento.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Guarda anche

* class [LayoutOptions](../)
* spazio dei nomi [Aspose.Words.Layout](../../../aspose.words.layout/)
* assemblea [Aspose.Words](../../../)
