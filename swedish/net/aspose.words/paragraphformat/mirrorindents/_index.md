---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ParagraphFormat MirrorIndents förbättrar formateringen av ditt dokument genom att säkerställa konsekventa vänster- och högerindrag för ett elegant utseende.
type: docs
weight: 240
url: /sv/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Hämtar eller ställer in en flagga som anger om vänster och höger indrag har samma bredd.

```csharp
public bool MirrorIndents { get; set; }
```

## Exempel

Visa hur man gör vänster- och högerindrag likadana.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
