---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words für .NET
description: ParagraphFormat HangingPunctuation eigendom. Ruft ein Flag ab oder setzt es das angibt ob hängende Satzzeichen für den aktuellen Absatz aktiviert sind in C#.
type: docs
weight: 130
url: /de/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Ruft ein Flag ab oder setzt es, das angibt, ob hängende Satzzeichen für den aktuellen Absatz aktiviert sind.

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
