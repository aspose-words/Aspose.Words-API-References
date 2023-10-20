---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words per .NET
description: ParagraphFormat WordWrap proprietà. Se questa proprietà lo èfalso  il testo latino nel mezzo di una parola può essere mandato a capo per il paragrafo corrente. Altrimenti il testo latino viene avvolto da parole intere in C#.
type: docs
weight: 410
url: /it/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Se questa proprietà lo è`falso` , il testo latino nel mezzo di una parola può essere mandato a capo per il paragrafo corrente. Altrimenti il testo latino viene avvolto da parole intere.

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
