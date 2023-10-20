---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words per .NET
description: ParagraphFormat FarEastLineBreakControl proprietà. Ottiene o imposta un flag che indica se le regole di interruzione riga dellAsia orientale vengono applicate al paragrafo corrente in C#.
type: docs
weight: 110
url: /it/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Ottiene o imposta un flag che indica se le regole di interruzione riga dell'Asia orientale vengono applicate al paragrafo corrente.

```csharp
public bool FarEastLineBreakControl { get; set; }
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
