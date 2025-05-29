---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ParagraphFormat-Eigenschaft „MirrorIndents“ die Formatierung Ihres Dokuments verbessert, indem sie konsistente linke und rechte Einzüge für ein elegantes Erscheinungsbild gewährleistet.
type: docs
weight: 240
url: /de/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Ruft ein Flag ab oder legt es fest, das angibt, ob der linke und der rechte Einzug die gleiche Breite haben.

```csharp
public bool MirrorIndents { get; set; }
```

## Beispiele

Zeigen Sie, wie Sie linke und rechte Einrückungen gleich machen.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
