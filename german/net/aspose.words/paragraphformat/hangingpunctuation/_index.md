---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Ihr Textlayout mit der Eigenschaft „Hängende Interpunktion“ in ParagraphFormat verbessern. Optimieren Sie mühelos Lesbarkeit und Stil!
type: docs
weight: 130
url: /de/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Ruft ein Flag ab oder legt es fest, das angibt, ob hängende Interpunktion für den aktuellen Absatz aktiviert ist.

```csharp
public bool HangingPunctuation { get; set; }
```

## Beispiele

Zeigt, wie spezielle Eigenschaften für asiatische Typografie festgelegt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
