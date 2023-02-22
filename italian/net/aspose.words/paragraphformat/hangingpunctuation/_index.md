---
title: ParagraphFormat.HangingPunctuation
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Ottiene o imposta un flag che indica se la punteggiatura in sospeso è abilitata per il paragrafo corrente.
type: docs
weight: 120
url: /it/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Ottiene o imposta un flag che indica se la punteggiatura in sospeso è abilitata per il paragrafo corrente.

```csharp
public bool HangingPunctuation { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


