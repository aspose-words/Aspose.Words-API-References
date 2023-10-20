---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words per .NET
description: ParagraphFormat HangingPunctuation proprietà. Ottiene o imposta un flag che indica se la punteggiatura sporgente è abilitata per il paragrafo corrente in C#.
type: docs
weight: 130
url: /it/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Ottiene o imposta un flag che indica se la punteggiatura sporgente è abilitata per il paragrafo corrente.

```csharp
public bool HangingPunctuation { get; set; }
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
