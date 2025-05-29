---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ParagraphFormat MirrorIndents migliora la formattazione del tuo documento garantendo rientri sinistri e destri uniformi per un aspetto curato.
type: docs
weight: 240
url: /it/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Ottiene o imposta un flag che indica se i rientri sinistro e destro hanno la stessa larghezza.

```csharp
public bool MirrorIndents { get; set; }
```

## Esempi

Mostra come rendere uguali i rientri sinistro e destro.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
