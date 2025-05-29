---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ParagraphFormat WordWrap influisce sul ritorno a capo del testo in Word. Impara a controllare il flusso del testo in latino per migliorare la leggibilità dei documenti.
type: docs
weight: 420
url: /it/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Se questa proprietà è`falso` , il testo latino nel mezzo di una parola può essere suddiviso per il paragrafo corrente. In caso contrario, il testo latino viene suddiviso in parole intere.

```csharp
public bool WordWrap { get; set; }
```

## Esempi

Mostra come impostare proprietà speciali per la tipografia asiatica.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
